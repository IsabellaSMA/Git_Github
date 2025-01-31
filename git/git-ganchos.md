# Ganchos do git

Os ganchos do Git são um mecanismo que permite que o código seja executado antes ou depois de determinados eventos de ciclo de vida do Git.
Por exemplo, é possível conectar-se ao evento commit-msg para validar se a estrutura da mensagem de confirmação segue o formato recomendado.
Os ganchos podem ser qualquer código executável, incluindo Shell, PowerShell, Python ou outros scripts. Eles também podem ser um executável binário.

### Critérios:
Os únicos critérios são que os ganchos devem ser armazenados na pasta .git/hooks na raiz do repositório. Além disso, eles devem ser nomeados para corresponder aos eventos relacionados (Git 2.x):

* applypatch-msg
* pre-applypatch
* post-applypatch
*pre-commit
prepare-commit-msg
commit-msg
post-commit
pre-rebase
post-checkout
post-merge
pre-receive
atualizar
post-receive
post-update
pre-auto-gc
post-rewrite
pre-push
