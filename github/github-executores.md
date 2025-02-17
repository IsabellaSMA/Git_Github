<h1 align=center>Executores</h1>

Os executores do GitHub são recursos de computação que executam fluxos de trabalho do GitHub Actions. Cada executor pode executar apenas um trabalho de cada vez. Eles permitem que os desenvolvedores executem tarefas de build, de teste e de implantação diretamente nos repositórios do GitHub. 

Há dois tipos principais de executores do GitHub:
* **Hospedados**: recursos de computação virtualizados, fornecidos e gerenciados pelo github;
* **auto-hospedados**: recursos de computação físicos,virualizados ou em containers que os usuários ou organizações do github provisionam por conta própria.

<h2 align=center>Executores hospedados no GitHub</h2>

Os executores hospedados no GitHub oferecem uma solução conveniente para executar fluxos de trabalho no GitHub Actions, eliminando a necessidade de administrar os componentes de hardware e software subjacentes.

São projetados para serem dimensionados automaticamente com base na demanda, garantindo um desempenho ideal durante os períodos de pico de uso. O GitHub fornece vários ambientes pré-configurados para executores hospedados no GitHub, abrangendo diferentes configurações de software e sistemas operacionais, incluindo Ubuntu Linux, Microsoft Windows e macOS.

istema operacional. Por exemplo, os executores do Ubuntu e do macOS incluem grep, find e which. Para identificar todas as outras ferramentas pré-instaladas em executores, os usuários podem examinar a SBOM (lista de materiais de software) para cada build das imagens do executor do Windows e do Ubuntu. Como alternativa, os usuários podem examinar a subseção Imagem do Executor da seção Configurar trabalho nos logs de fluxo de trabalho. O link após a entrada Software Incluído descreve todas as ferramentas pré-instaladas no executor que executou o fluxo de trabalho. Também é possível instalar software adicional em executores hospedados no GitHub criando um trabalho que instala os pacotes como parte do fluxo de trabalho existente.

Os executores hospedados no GitHub são executados na infraestrutura de nuvem do GitHub, aproveitando máquinas virtuais ou contêineres para executar fluxos de trabalho. Cada execução de fluxo de trabalho é isolada em um ambiente próprio, garantindo segurança e reprodutibilidade. Os executores hospedados no GitHub integram-se perfeitamente ao GitHub Actions, permitindo que os usuários os referenciem diretamente nos fluxos de trabalho hospedados nos repositórios do GitHub.

Há alguns limites para o uso do GitHub Actions ao usar os executores hospedados no GitHub. Em particular, cada trabalho em um fluxo de trabalho tem o máximo de seis horas de tempo de execução. Se um trabalho atingir esse limite, o trabalho será terminado e não será completado. Cada execução de fluxo de trabalho é limitada a 35 dias. Se uma execução de fluxo de trabalho atingir esse limite, a execução dela será cancelada. Esse período inclui a duração da execução e o tempo gasto em espera e aprovação.

<h3 align=center>Pré-requisitos</h3>
Antes de implementar os executores hospedados no GitHub, os usuários precisam ter um repositório do GitHub em que possam definir fluxos de trabalho usando o GitHub Actions. Os executores estão disponíveis para todos os usuários do GitHub com acesso ao GitHub Actions.

<h3 align=center>Implementação</h3>
Ao contrário dos executores auto-hospedados, aqueles hospedados no GitHub são provisionados automaticamente como parte de uma execução de fluxo de trabalho individual. Os usuários definem fluxos de trabalho como arquivos formatados em YAML armazenados no diretório .github/workflows em repositórios do GitHub. Dentro da configuração do fluxo de trabalho, os usuários especificam o ambiente desejado do executor, incluindo o sistema operacional e as dependências de software. Os executores com especificações correspondentes são configurados sob demanda sempre que o fluxo de trabalho é disparado, com um executor por trabalho. Os gatilhos podem ser manuais ou automáticos, com base em eventos como pushes de código, solicitações de pull ou eventos de expedição de repositório.
Os executores hospedados no GitHub autenticam-se com o GitHub usando tokens ou credenciais fornecidas pelo GitHub Actions. Eles dependem da conectividade interna para se comunicar com a plataforma GitHub e baixar artefatos de fluxo de trabalho.

<h3 align=center>Manutenção</h3>
O GitHub gerencia atualizações e manutenção de executores hospedados no GitHub, garantindo que eles permaneçam atualizados com as versões de software mais recentes e patches de segurança. As ferramentas de software incluídas nos executores são atualizadas semanalmente. As atividades do executor são monitoradas e registradas em log, facilitando o acompanhamento de execuções de fluxo de trabalho e solução de problemas.

<h3 align=center>Licenciamento e custo</h3>
Os executores hospedados no GitHub estão incluídos nos preços do GitHub Actions, com cobrança baseada em uso para minutos de fluxo de trabalho além da camada gratuita. Os usuários se beneficiam da escala automatizada e econômica, pois o GitHub provisiona e desaloca automaticamente os executores com base na demanda
