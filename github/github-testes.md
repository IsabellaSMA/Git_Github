<h1 align=center> Testando uma ação</h1>
As ações geralmente produzirão a saída do console

A saída do console das ações está disponível diretamente de dentro da interface do usuário do GitHub.

Selecione Ações no menu do repositório superior para ver uma lista de fluxos de trabalho executados para ver a saída.

Em seguida, clique no nome do trabalho para ver a saída das etapas.![console-output-from-actions-63af6157](https://github.com/user-attachments/assets/a6788057-fad0-4162-a9e0-304ad106f70d)
A saída do console pode ajudar na depuração.

<h2 align=center>Release Management para Actions
É possivel solicitar uma versão específica da ação de várias maneiras:

<h3 align=center>Marcações</h3>
As tags permitem que você especifique as versões com que deseja trabalhar

`YAML`

    steps:
    -uses: actions/install-timer@v2.0.1

<h3 align=center> Hashes baseados em SHA</h3>
Você pode especificar um hash baseado em SHA solicitado para uma ação. Ele garante que a ação não foi alterada. No entanto, a desvantagem disso é que você também não receberá atualizações para a ação automaticamente.

`YAML`

     steps:
    -uses: actions/install-timer@327239021f7cc39fe7327647b213799853a9eb98

<h3 align=center>Branches</h3>
Uma forma comum de solicitar ações é se referir à ramificação com que você quer trabalhar. Em seguida, você obterá a versão mais recente dessa ramificação. Isso significa que você se beneficiará das atualizações, mas também aumentará a chance de interrupção do código.

`YAML`

    steps:
    -uses: actions/install-timer@develop

<h2 align=center>Testar uma ação</h2>
O github usa ferramentas de aprendizado para ações, <a href="https://github.com/skills/hello-github-actions" blank="">acesse essa</a>
