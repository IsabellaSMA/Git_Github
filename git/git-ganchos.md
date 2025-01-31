# Ganchos do git

Os ganchos do Git são um mecanismo que permite que o código seja executado antes ou depois de determinados eventos de ciclo de vida do Git.
Por exemplo, é possível conectar-se ao evento commit-msg para validar se a estrutura da mensagem de confirmação segue o formato recomendado.
Os ganchos podem ser qualquer código executável, incluindo Shell, PowerShell, Python ou outros scripts. Eles também podem ser um executável binário.
Os ganchos do Git oferecem uma grande oportunidade. Eles servem como um mecanismo para executar scripts personalizados em resposta a eventos significativos dentro do ciclo de vida do Git, como fazer commits, mesclagens e pushes. Os scripts, localizados no diretório .git\hooks do repositório, fornecem flexibilidade praticamente ilimitada na automatização de tarefas de desenvolvimento de software e na imposição de padrões de desenvolvimento.

## Critérios:
Os únicos critérios são que os ganchos devem ser armazenados na pasta .git/hooks na raiz do repositório. Além disso, eles devem ser nomeados para corresponder aos eventos relacionados (Git 2.x):

* applypatch-msg
* pre-applypatch
* post-applypatch
* pre-commit
* prepare-commit-msg
* commit-msg
* post-commit
* pre-rebase
* post-checkout
* post-merge
* pre-receive
* atualizar
* post-receive
* post-update
* pre-auto-gc
* post-rewrite
* pre-push

### Casos de uso para usar ganchos do Git:

Alguns exemplos de uso de ganchos são impor políticas, garantir a consistência e controlar seu ambiente:

Em Impor pré-condições para mesclagem
Como verificar a associação da ID de item de trabalho na mensagem de commit
Como impedir que você e sua equipe façam commit de código com falha
Enviar notificações para a sala de chat da sua equipe (Teams, Slack, HipChat etc.)

## Como implementar ganchos do Git:

Navegue até o diretório .git\hooks do repositório. Você encontra vários arquivos com a extensão `sample`. Essa extensão não só indica sua finalidade, mas também as impede efetivamente de executar. Os nomes de arquivo designam as ações do Git que disparam sua execução após remover a extensão `sample`.
![git-hook-files-8bce9eb8](https://github.com/user-attachments/assets/81cde6c3-00c9-48d9-99d2-ff99baf07f68) 

Renomeie o arquivo de pré-confirmação sample para pré-confirmação. Como o nome do arquivo indica, o script que ele contém será executado sempre que você invocar a ação de commit do Git. O commit segue somente se o script de pré-confirmação sair com o valor retornado 0.

### Línux:

`#!/bin/sh`
* Nos sistemas operacionais do Linux, o prefixo #! indica ao carregador do programa que o restante do arquivo contém um script a ser interpretado e /bin/sh é o caminho completo para o interpretador que deve ser usado.


### Windows:
 É preciso fornecer o caminho completo para o arquivo sh.exe, começando com a letra da unidade. o Git para Windows, por padrão, é instalado no diretório C:\Arquivos de Programas. Como esse diretório contém um espaço em seu nome, o caminho resultante para o arquivo sh.exe seria interpretado como dois caminhos separados, resultando em uma falha. Para evitá-lo, é necessário adicionar uma única barra invertida (\) na frente do espaço para servir como um caractere de escape. Efetivamente, ao usar a versão de 64 bits do Git para Windows, a primeira linha do script deve ter o seguinte formato:

`#!C:/Program\ Files/Git/usr/bin/sh.exe`

Como é possível usar a funcionalidade recém-descoberta de scripts de pré-confirmação do Git? Que tal impedir que você vaze segredos acidentalmente para o GitHub?

Vamos usar o gancho do Git para verificar o código que está sendo confirmado em seu repositório local em busca de palavras-chave específicas. Substitua o conteúdo do arquivo shell de pré-confirmação pelo seguinte código:

`#!C:/Program\ Files/Git/usr/bin/sh.exe
matches=$(git diff-index --patch HEAD | grep '^+' | grep -Pi 'password|secret')
if [ ! -z "$matches" ]
then
  cat <<\EOT
Error: Words from the blocked list were present in the diff:
EOT
echo $matches
exit 1
fi `

**Este exemplo destina-se a ilustrar o conceito em vez de uma solução completa, portanto, a lista de palavras-chave é intencionalmente trivial.**

#### Como este código funciona: 

Uma vez invocado, o script de gancho de pré-confirmação usa os comandos diff e grep do Git, para identificar palavras-chave ou padrões dentro das alterações incrementais no código que estão sendo confirmadas. Se alguma correspondência for detectada, o script gerará uma mensagem de erro e impedirá que o commit ocorra.

## Outros casos de uso

formatação de código, lint ou execução de testes personalizados para garantir que o commit adere aos padrões do projeto. O prepare-commit-msg é executado antes do editor de mensagens do commit ser iniciado. Ele permite a geração dinâmica de mensagens do commit para impor convenções de nomenclatura, como o uso de prefixos designados, por exemplo, feat: para recursos ou fix: para correções de bug.

Por exemplo, o script prepare-commit-msg a seguir anexa automaticamente o nome do branch atual à mensagem do commit ao criar uma novo commit. Ele modifica o arquivo de mensagem do commit (US$ 1) adicionando o nome do branch seguido por dois-pontos e espaço no início do arquivo.

`Bash`
#!C:/Program\ Files/Git/usr/bin/sh.exe
# Get the current branch name
branch_name=$(git branch --show-current)
# Check if the commit message file exists
if [[ -f "$1" ]]; then
  # Prepend the branch name to the commit message
  sed -i "1s/^/$branch_name: /" "$1" 
fi


Os scripts de pós-confirmação são executados após a conclusão de um commit. Eles podem ser usados para disparar notificações ou gerar documentação.

Por exemplo, o script a seguir envia uma notificação por email para um destinatário designado após cada commit. O script pode ser personalizado modificando o endereço de email do destinatário, o servidor do SMTP e o assunto e o corpo do email. Além disso, talvez seja necessário configurar seu sistema para enviar emails usando o cmdlet Send-MailMessage do PowerShell ou usar um método diferente para enviar notificações, dependendo de seu ambiente e requisitos.

`Bash`
#!C:/Program\ Files/Git/usr/bin/sh.exe
# Set the recipient email address
$recipient="your@email.com"
# Set the subject of the email
$subject="Git Commit Notification"
# Set the body of the email
$body="A new commit has been made to the repository."
# Send the email notification
Send-MailMessage -To $recipient -Subject $subject -Body $body -SmtpServer "your.smtp.server"

Vale a pena observar que a pasta repositório .git\hooks não está confirmada no controle do código-fonte. Você pode se perguntar se há uma maneira de compartilhar os scripts desenvolvidos com outro membro da sua equipe de desenvolvimento. A boa notícia é que, a partir da versão 2.9 do Git, é possível mapear ganchos do Git para uma pasta cujo o commit pode ser feito no controle do código-fonte. Você pode fazer isso atualizando a configuração de definições globais para seu repositório Git:

`Bash`
`Git config --global core.hooksPath '~/.githooks'`

Se você precisar substituir os ganchos do Ggit que configurou no lado do cliente, poderá fazer isso usando a opção sem verificação digitando `Git commit --no-verify`
