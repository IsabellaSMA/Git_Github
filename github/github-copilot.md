<h2 align=center> Integração do GitHub Copilot ao ambiente de desenvolvedor</h2>

O GitHub Copilot integra-se nativamente ao Visual Studio Code, ao Visual Studio e a outros ambientes de desenvolvedor.

O GitHub Copilot é implementado usando duas extensões para o Visual Studio Code: GitHub Copilot e GitHub Copilot Chat.

* A extensão do GitHub Copilot fornece conclusões de código e geração de código a partir de comentários. Ferramentas avançadas que ajudam os desenvolvedores a escrever código de forma mais rápida e inteligente.
* A extensão GitHub Copilot Chat fornece ao editor uma interface de chat habilitada para IA focada em cenários de desenvolvedor. Ela reconhece todo o workspace do projeto, as revisões de código que estão sendo inseridas, mensagens de erro e outros aspectos do ambiente do compilador/runtime. Os desenvolvedores podem usar o Copilot Chat para obter uma análise detalhada de seu código, investigar novos recursos, aprimorar ou refatorar recursos existentes, gerar testes de unidade e até mesmo receber correções propostas para bugs.

<h2 align=center> Limitações do GitHub Copilot Chat</h2>

### Escopo limitado
O GitHub Copilot Chat é treinado em um grande corpo de código, mas ainda tem um escopo limitado. Ele pode não ser capaz de lidar com algumas estruturas de código complexas ou linguagens de programação obscuras. Para cada linguagem de programação, a qualidade das sugestões recebidas pode depender do volume e da diversidade de dados de treinamento para esse idioma. Por exemplo, o JavaScript é bem representado em repositórios públicos e é uma das linguagens com melhor suporte do GitHub Copilot. Linguagens com menos representação em repositórios públicos podem ser mais desafiadoras para o Copilot Chat. Além disso, o Copilot Chat só pode sugerir código com base no contexto do código que está sendo escrito, portanto, ele pode não ser capaz de identificar problemas maiores de design ou arquitetura.

Possíveis desvios
Os dados de treinamento do GitHub Copilot são extraídos de repositórios de código existentes que podem conter desvios e erros. O GitHub Copilot poderá perpetuar os desvios se eles existirem nos dados de treinamento. O GitHub Copilot Chat pode ser tendencioso em relação a determinadas linguagens de programação ou estilos de codificação, o que pode levar a sugestões de código abaixo do ideal ou incompletas.

### Riscos à segurança
O Copilot Chat gera código com base no contexto do código que está sendo escrito, que pode potencialmente expor informações confidenciais ou vulnerabilidades se não for usado com cuidado. Você deve ter cuidado ao usar o Copilot Chat para gerar código para aplicativos sensíveis à segurança e sempre examinar e testar o código gerado minuciosamente.

### Correspondências com código público
O Copilot Chat é capaz de gerar um novo código e faz isso de forma probabilística. A probabilidade de o Copilot Chat produzir um código que corresponda ao código no conjunto de treinamento é baixa, mas não zero. Uma sugestão do Copilot Chat pode conter alguns snippets de código que correspondem ao código no conjunto de treinamento. O Copilot Chat usa filtros que bloqueiam correspondências com código público em repositórios do GitHub, mas você ainda deve tomar precauções. Você deve tratar as sugestões do GitHub Copilot da mesma maneira que trataria qualquer código que use um material que você não criou. Isso inclui precauções para garantir sua adequação. Isso inclui testes rigorosos, verificação de IP e acompanhamento de vulnerabilidades de segurança. Você deve verificar se o IDE ou o editor não compila ou executa automaticamente o código gerado antes de revisá-lo.

### Código impreciso
O GitHub Copilot Chat pode gerar um código que parece ser válido, mas não é. O código pode não estar semanticamente ou sintaticamente correto, ou pode não refletir com precisão a intenção do desenvolvedor. Para atenuar o risco de código impreciso, você deve examinar e testar cuidadosamente o código gerado. Isso é particularmente importante ao lidar com aplicativos críticos ou confidenciais. Você também deve garantir que o código gerado siga práticas recomendadas e os padrões de design e se encaixe na arquitetura geral e no estilo da base de código.

### Respostas imprecisas a tópicos de não codificação
O Copilot Chat não foi projetado para responder a perguntas não codificadas e, portanto, suas respostas podem nem sempre ser precisas ou úteis nesses contextos. Se um usuário fizer uma pergunta de não codificação ao Copilot Chat, ele poderá gerar uma resposta irrelevante ou sem sentido, ou pode simplesmente indicar que não é possível fornecer uma resposta útil.
