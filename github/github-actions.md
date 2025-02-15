<h1 align=center> Introdução ao Github Actions </h1>

As GitHub Actions são o mecanismo principal para automação no GitHub.Elas podem ser usadas para uma ampla variedade de finalidades, mas um dos mais comuns é implementar a integração contínua.

As ações são o mecanismo usado para fornecer automação de fluxo de trabalho dentro do ambiente do GitHub.Geralmente, são usadas para criar soluções de CI (integração contínua) e CD (implantação contínua).

No entanto, podem ser usadas para uma ampla variedade de tarefas:
* Teste automatizado.
* Responder automaticamente a novos problemas, menções.
* Disparar revisões de código.
* Tratar solicitações de pull.
* Gerenciamento de branch.

Elas são definidos no YAML e permanecem dentro de repositórios do GitHub. As ações são executadas em "executores", sejam hospedados pelo GitHub ou auto-hospedados. As ações de contribuição podem ser encontradas no GitHub Marketplace.

<h2 align=center> Fluxo do Actions</h2>

O GitHub rastreia eventos que ocorrem. Os eventos podem disparar o início dos fluxos de trabalho. Fluxos de trabalho são a unidade de automação. Eles contêm Trabalhos.Os trabalhos usam Ações para fazer o trabalho.

Os fluxos de trabalho também podem iniciar conforme cronogramas baseados em cron e ser disparados por eventos fora do GitHub ,eles podem ser disparados manualmente.


<h2 align=center> Noções básicas de fluxos de trabalho </h2>

Os fluxos de trabalho definem a automação necessária. Ele detalha os eventos que devem disparar o fluxo de trabalho. Além disso, define os trabalhos que devem ser executados quando o fluxo de trabalho é disparado. O trabalho define o local no qual as ações serão executadas, por exemplo, qual executor usar.

Os fluxos de trabalho são escritos em YAML e ao vivo em um repositório do GitHub no local .github/workflows

Exemplo de um fluxo de trabalho:

`YAML`

    #.github/workflows/build.yml
    name: Node Build.

    on: [push]

    jobs:
    mainbuild: 
 
      runs-on: ${{ matrix.os }}
     
      strategy:
          matrix:
              node-version: [12.x]
              os: [windows-latest]
         
    steps:

    - uses: actions/checkout@v1
    - name: Run node.js on latest Windows.
      uses: actions/setup-node@v1
      with:
        ode-version: ${{ matrix.node-version }}

    - name: Install NPM and build.
      run: |
        npm ci
        npm run build

<h3 align=center>Mais informações</h3>

encontrar um conjunto de fluxos de trabalho de início aqui: [Fluxos de trabalho iniciais.](https://github.com/actions/starter-workflows)

sintaxe acessível para fluxos de trabalho: [sintaxe de fluxo de trabalho para o GitHub Actions](https://docs.github.com/pt/actions/writing-workflows/workflow-syntax-for-github-actions)
