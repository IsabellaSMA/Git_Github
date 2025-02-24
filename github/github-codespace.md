# ciclo de vida do Codespace

O GitHub Codespaces é configurável, permitindo que você crie um ambiente de desenvolvimento personalizado para seu projeto. Ao configurar um ambiente de desenvolvimento personalizado para o projeto, você pode ter uma configuração reproduzível do Codespace para todos os usuários do projeto.

O ciclo de vida de um Codespace começa quando você cria um Codespace e termina quando você o exclui. Você pode se desconectar e reconectar a um Codespace ativo sem afetar os processos em execução. Você pode parar e reiniciar um Codespace sem perder as alterações feitas no projeto.

Criar um Codespace
Você pode criar um Codespace no GitHub.com, no Visual Studio Code ou usando a CLI do GitHub. Há quatro maneiras de criar um Codespace:

Usando um modelo do GitHub ou qualquer repositório de modelos no GitHub.com para iniciar um novo projeto.
De um branch em seu repositório para um novo trabalho de recursos.
De um pull request aberto para explorar o trabalho em andamento.
Usando um commit no histórico do repositório para investigar um bug em um momento específico.
Você pode usar um Codespace temporariamente para testar o código ou pode voltar ao mesmo Codespace para continuar um trabalho de recursos de longa execução.

Você pode criar mais de um Codespace por repositório ou até mesmo por branch. No entanto, há limites quanto ao número de Codespaces que você pode criar e o que você pode executar ao mesmo tempo. Quando você atinge o número máximo de Codespaces e tenta criar outro, uma mensagem é exibida. A mensagem informa que um Codespace existente precisar ser removido/excluído antes que um novo Codespace possa ser criado.

Você pode criar um Codespace sempre que desenvolver no GitHub Codespaces ou pode manter um Codespace de execução prolongada para um recurso. Se estiver iniciando um novo projeto, crie um Codespace usando um modelo e publique-o em um repositório no GitHub posteriormente.

Ao criar um Codespace sempre que trabalhar em um projeto, você deverá efetuar push das alterações regularmente para garantir que os novos commits estejam no GitHub. Ao usar um Codespace de execução longa para um novo projeto, efetue pull do branch padrão do repositório sempre que começar a trabalhar no Codespace para permitir que seu ambiente obtenha as confirmações mais recentes. O fluxo de trabalho é semelhante a trabalhar com um projeto em um computador local.

Administradores de repositório podem habilitar pré-compilações do GitHub Codespaces para um repositório para acelerar a criação do Codespace.

Para obter orientações detalhadas e diretrizes passo a passo, confira os recursos Guia para iniciantes para aprender a codificar com o GitHub Codespaces e Desenvolver em um Codespace, localizados na unidade Resumo no final deste módulo.

## Processo de criação de um codespace
Ao criar um GitHub Codespace, ocorrem quatro processos:

Uma máquina virtual e um armazenamento são atribuídos ao seu Codespace.
Um contêiner é criado.
É feita uma conexão com o Codespace.
É feita uma configuração pós-criação.

Salvar alterações em um Codespace
Quando você se conecta a um Codespace por meio da Web, o Salvamento Automático é habilitado automaticamente para salvar as alterações após um período específico ter passado. Quando se conecta a um Codespace usando o Visual Studio Code em execução na área de trabalho, você precisa habilitar o salvamento automático.

O trabalho é salvo em uma máquina virtual na nuvem. Você pode fechar e parar um Codespace e voltar ao trabalho salvo posteriormente. Se tiver alterações não salvas, você receberá um prompt para salvá-las antes de sair. No entanto, se o Codespace for excluído, seu trabalho será perdido. Para salvar o trabalho, você precisa fazer commit das alterações e efetuar push delas para seu repositório remoto ou publicar o trabalho em um novo caso você tenha criado seu Codespace usando um modelo.

Abrir um Codespace existente
Você pode reabrir qualquer um de seus Codespaces ativos ou parados no GitHub.com, em um IDE do JetBrains, no Visual Studio Code ou usando a CLI do GitHub.

Para retomar um Codespace existente, acesse o repositório onde o Codespace existe, selecione a chave , e, em seguida, Retomar este codespace. Ou você pode abrir https://github.com/codespaces no navegador, selecionar o repositório e, em seguida, o Codespace existente.

Tempos limite para um Codespace
Se um Codespace estiver inativo ou se você sair dele sem pará-lo explicitamente, o aplicativo atingirá o tempo limite após um período de inatividade e deixará de ser executado. O tempo limite padrão é atingido após 30 minutos de inatividade. Quando um Codespace atinge o tempo limite, seus dados são preservados da última vez em que alterações foram salvas.

Conexão com a Internet usando o GitHub Codespaces
Um Codespace requer uma conexão com a Internet. Se a conexão com a Internet for perdida durante seu trabalho em um Codespace, você não poderá acessar o Codespace. No entanto, as alterações não confirmadas serão salvas. Quando restabelecer a conexão com a Internet, você poderá acessar o Codespace no mesmo estado em que ele foi deixado quando a conexão foi perdida.

Se você tiver uma conexão instável com a Internet, faça commit e efetue push de suas alterações com frequência.

Fechar ou parar um Codespace
Se você sair do Codespace sem executar o comando Parar ou deixar o Codespace em execução sem interação, o Codespace e os processos em execução continuarão durante o período de tempo limite de inatividade. O período de tempo limite de inatividade padrão é de 30 minutos. Você pode definir sua configuração de tempo limite pessoal para os Codespaces que criar, mas isso pode ser anulado por uma política de tempo limite da organização.

Somente Codespaces em execução incorrem em encargos de CPU. Um Codespace parado incorre apenas em custos de armazenamento.

Você pode parar e reiniciar um Codespace para aplicar alterações. Por exemplo, se você alterar o tipo de computador usado no Codespace, precisará parar e reiniciá-lo para que a alteração entre em vigor. Quando você fecha ou para o Codespace, todas as alterações não confirmadas são preservadas até você se conectar novamente ao Codespace.

Você também pode parar o Codespace e optar por reiniciá-lo ou excluí-lo se encontrar um erro ou algo inesperado.


Recompilar um Codespace
Você pode recompilar o Codespace para implementar alterações em sua configuração de contêiner de desenvolvimento. Para a maioria dos usos, você pode criar um Codespace como alternativa à recompilação de um Codespace. Quando você recompila o Codespace, as imagens do cache aceleram o processo de recompilação. Você também pode executar uma recompilação completa para limpar o cache e recompilar o contêiner com imagens novas.

Quando você recompila o contêiner em um Codespace, as alterações feitas fora do diretório /workspaces são limpas. Alterações feitas dentro do diretório /workspaces, incluindo o clone do repositório ou modelo com base no qual você criou o Codespace, são preservadas em uma recompilação.

Excluir um Codespace
Você pode criar um Codespace para uma tarefa específica. Após efetuar push de alterações para um branch remoto, você poderá excluir com segurança esse Codespace.

Se você tentar excluir um Codespace com git commits que não foram enviadas por push, o editor notificará você de que há alterações que não foram enviadas por push para um branch remoto. Você pode efetuar push de qualquer alteração desejada e excluir o Codespace. Você também pode excluir o Codespace e as alterações não confirmadas ou exportar o código para um novo branch sem criar um Codespace.

Codespaces parados que permanecem inativos por um período especificado são excluídos automaticamente. Codespaces inativos são excluídos após 30 dias, mas você pode personalizar os intervalos de retenção do Codespace.

