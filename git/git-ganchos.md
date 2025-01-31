# Ganchos do git

Os ganchos do Git são um mecanismo que permite que o código seja executado antes ou depois de determinados eventos de ciclo de vida do Git.
Por exemplo, é possível conectar-se ao evento commit-msg para validar se a estrutura da mensagem de confirmação segue o formato recomendado.
Os ganchos podem ser qualquer código executável, incluindo Shell, PowerShell, Python ou outros scripts. Eles também podem ser um executável binário.

### Critérios:
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
