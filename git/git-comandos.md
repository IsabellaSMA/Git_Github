# Comandos Básicos em git

`git status`
* Exibe o estado da árvore de trabalho. Permite ver quais alterações estão sendo controladas pelo Git.

`git add`
* O termo técnico é preparar essas alterações. O git add "adiciona" os arquivos deixando eles em  estado chamado de *staged* - preparo para ser commitados. O comando `git add.`facilita o trabalho de adicionar um arquivo por vez, dessa forma, todos os arquivos do projeto são adicionados de uma vez. 
  
`git commit -m "mensagem-de-commit"`
* Fazer commit de alterações significa colocar uma cópia (do arquivo, do diretório ou de outros itens) no repositório como uma nova versão. Os dados salvos em um commit incluem o nome e o endereço de email do autor, a data, os comentários sobre o que foi feito (e o motivo), uma assinatura digital opcional e o identificador exclusivo do commit anterior.

`git log`
* Permite que você veja informações sobre commits anteriores pois imprime informações sobre os commits mais recentes, como o carimbo de data/hora, o autor e uma mensagem de commit. Esse comando ajuda a acompanhar o que está sendo feito e quais alterações foram salvas.
  
`git --help`
* obter com facilidade informações sobre todos os comandos. É possível pesquisar ajuda sobre um tema específico usando o comando `git <comando> --help`. Por exemplo, `git commit --help` abre uma página que traz mais informações sobre o comando git commit e como usá-lo. 

`git init`
* Se você está começando do zero e deseja criar um repositório, use git init. Com o comando git init, é possível criar um repositório com valores padrão ou especificar valores para ele.

`git remote add origin`
* algo aqui tbm

`git checkout -b "nome da branch"`
* Comando para criar de uma nova branch

#### Identidade

`git config`
* git config define diversos atributos de configuração. Para ver quais são suas configurações sem realizar alterações, liste-as com `git config --list`
Com git config, é possível definir o nome e o endereço de email associados a todas as alterações com:
`git config user.name “<your name>” ` <br>
`git config --global user.name “<your name>”`

`git clone`
* git clone é o comando que copia (ou clona) um repositório para o computador local. Ao executar o comando git clone, você cria uma cópia completa do repositório remoto ou de origem, incluindo branches, histórico e outros metadados. Ao clonar um repositório, é possível especificar o local. Se você não especificar onde colocar o repositório, ele será colocado na pasta de trabalho atual (de onde você está emitindo o comando).

Comando: `git clone <source repo URL> <path or location to place the clone> `

`git branch`
* git branch permite criar um branch ou ver quais branches existem atualmente para o repositório. Para ver uma lista dos branches atuais, use o comando git branch ou adicione a opção --list. Exemplo: `git branch --list`


`git checkout`
* git checkout permite mudar rapidamente entre diferentes branches no repositório Git. Quando você está trabalhando “dentro” de um branch, todos os arquivos acessados estarão no estado em que se encontram naquele branch. Quando você muda de branch, o conteúdo dos arquivos no computador muda para corresponder ao branch para o qual você mudou.

<details>
  <summary>Se você estiver trabalhando em um novo recurso e precisar trabalhar em bugs por um tempo, talvez seja necessário fazer o seguinte:</summary>
  <p>Alterar os branches para o branch de bug.
Atualizar os arquivos no branch de bug.
Atualizar o branch de bug.
Voltar para o branch de recursos.
git checkout <branch name></p>
</details>


git push
Assim que as atualizações estiverem presentes no repositório local, será necessário decidir se elas também devem ser compartilhadas com o repositório de origem ou remoto. git push “envia” as alterações feitas e a nota que você adicionou para o commit ao repositório remoto.

Quando você usa o comando git push, ele envia o branch atual, com todo o histórico, os comentários e as alterações de arquivo. É importante verificar se você está no branch correto antes de executar o comando git push.

