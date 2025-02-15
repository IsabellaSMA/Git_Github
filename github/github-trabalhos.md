<h1 align=center> Trabalhos </h1>

Um trabalho é um conjunto de etapas que serão executadas em ordem em um executor. As etapas dentro de um trabalho são executadas no mesmo executor e compartilham o mesmo sistema de arquivos. Os logs[^1] produzidos por trabalhos são pesquisáveis e os artefatos produzidos podem ser salvos.

<h2 align=center>Trabalhos com dependências</h2>
Por padrão, se um fluxo de trabalho contiver vários trabalhos, eles serão executados em paralelo. Exemplo:

`YAML`

    jobs:

    startup:
  
    runs-on: ubuntu-latest
    steps:

      - run: ./setup_server_configuration.sh
    build:
    steps:

      - run: ./build_new_server.sh


Às vezes, talvez seja necessário que um trabalho aguarde a conclusão de outro.

Você pode fazer isso definindo dependências entre os trabalhos, como no exemplo abaixo.

`YAML`

    jobs:
      startup:
        runs-on: ubuntu-latest
        steps:

      - run: ./setup_server_configuration.sh
      build:
        needs: startup
        steps:

      - run: ./build_new_server.sh




































[^1]:Um log é um registro detalhado de eventos ou atividades que ocorrem em um sistema, aplicativo, dispositivo ou rede. Ele é usado para acompanhar e documentar informações relevantes, como erros, avisos, transações, alterações de configuração e outras ações importantes.
