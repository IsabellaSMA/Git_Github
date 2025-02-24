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
