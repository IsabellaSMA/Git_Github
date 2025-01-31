# Comandos Básicos em git

`git --version`
* comando para ver a versão instalada do git


`git config`
* git config define diversos atributos de configuração. Para ver quais são suas configurações sem realizar alterações, liste-as com `git config --list`.A primeira/principal uabilidade deste comando é definir o nome e o endereço de email associados a todas as alterações com:
`git config user.name “<your name>” ` <br>
`git config --global user.name “<your name>”`
<br>

`git --help`
* obter com facilidade informações sobre todos os comandos. É possível pesquisar ajuda sobre um tema específico usando o comando `git <comando> --help`. Por exemplo, `git commit --help` abre uma página que traz mais informações sobre o comando git commit e como usá-lo. 


`git init`
* Se você está começando do zero e deseja criar um repositório, use git init. Com o comando git init, é possível criar um repositório com valores padrão ou especificar valores para ele.


`git status`
* Exibe o estado da árvore de trabalho. Permite ver quais alterações estão sendo controladas pelo Git.

`git add`
* O termo técnico é preparar essas alterações. O git add "adiciona" os arquivos deixando eles em  estado chamado de *staged* - preparo para ser commitados. O comando `git add.`facilita o trabalho de adicionar um arquivo por vez, dessa forma, todos os arquivos do projeto são adicionados de uma vez. 

`git commit -m "mensagem-de-commit"`
* Fazer commit de alterações significa colocar uma cópia (do arquivo, do diretório ou de outros itens) no repositório como uma nova versão. Os dados salvos em um commit incluem o nome e o endereço de email do autor, a data, os comentários sobre o que foi feito (e o motivo), uma assinatura digital opcional e o identificador exclusivo do commit anterior.

`git log`
* Permite que você veja informações sobre commits anteriores pois imprime informações sobre os commits mais recentes, como o carimbo de data/hora, o autor e uma mensagem de commit. Esse comando ajuda a acompanhar o que está sendo feito e quais alterações foram salvas.
  

`git remote add origin`
* algo aqui tbm


`git clone`
* git clone é o comando que copia (ou clona) um repositório para o computador local. Ao executar o comando git clone, você cria uma cópia completa do repositório remoto ou de origem, incluindo branches, histórico e outros metadados. Ao clonar um repositório, é possível especificar o local. Se você não especificar onde colocar o repositório, ele será colocado na pasta de trabalho atual (de onde você está emitindo o comando).

Como clonar um repositório: [github tutorial](https://docs.github.com/pt/repositories/creating-and-managing-repositories/cloning-a-repository)
* Vá até o repositório local do github. Cloque no botão "Code" e copie o caminho https;
* abra o git bash no diretório onde quer que esse local seja clonado (Area de Trabalho, Documentos..etc);
* Digite `git clone <link do repo copiado>` e Enter.
* Pronto. Repositório clonado!
<details>
<summary>Agora se quiser se sentir a(o) programadora(o)..</summary>
  <p> Abra o git bash</p> 
  <p> Digite o comando "cd" e digite o caminho do diretório que deseja clonar o repositório (Exemplo: cd "c:/Users/nome-usuario/OneDrive/Documents")</p> 
  <p>Assim que o git bash mostrar o novo direório(~ /OneDrive/Documents)..</p>
  <p>git clone "https do repositório local"</p>
  <p> Pronto</p>
</details>


`git branch`
* git branch permite criar um branch ou ver quais branches existem atualmente para o repositório. Para ver uma lista dos branches atuais, use o comando git branch ou adicione a opção --list. Exemplo: `git branch --list`

`git push`
* Assim que as atualizações estiverem presentes no repositório local, será necessário decidir se elas também devem ser compartilhadas com o repositório de origem ou remoto. git push “envia” as alterações feitas e a nota que você adicionou para o commit ao repositório remoto.O comando git push envia o branch atual com todo o histórico, os comentários e as alterações de arquivo. **É importante verificar se você está no branch correto antes de executar o comando git push.**

`git checkout -b "nome da branch"`
* git checkout permite mudar rapidamente entre diferentes branches no repositório Git. Quando você está trabalhando “dentro” de um branch, todos os arquivos acessados estarão no estado em que se encontram naquele branch. Quando você muda de branch, o conteúdo dos arquivos no computador muda para corresponder ao branch para o qual você mudou.

<br>

<details>
  <summary>Se você estiver trabalhando em um novo recurso e precisar trabalhar em bugs por um tempo, este comando é util, pois pode-se fazer:</summary> <br>
    <p>Alterar os branches para o branch de bug</p>
    <p>Atualizar os arquivos no branch de bug.</p>
    <p>Atualizar o branch de bug.</p>
    <p>Voltar para o branch de recursos.</p>
    <p>git checkout <branch name></p>
</details>

<br>

### Comandos intermediários:

`git pull` 
* Entra em contato com a ramificação remota e verifica se há atualizações necessárias e, em seguida, atualiza seu repositório local. **É uma boa ideia efetuar pull do Git antes de começar a trabalhar em seus arquivos**. Atualizar seu repositório antes de iniciar o trabalho ajuda a evitar conflitos posteriores caso você não tenha começado a partir da atualização mais recente.


`git merge`
* Permite que você informe ao Git que deseja tirar o arquivo do branch de treinamento, por exemplo, e incorporá-lo ao branch de produção ou principal do código. Se você acabou de trabalhar no código no branch de treinamento e deseja mesclar as alterações no branch principal, será preciso alternar para o branch principal primeiro usando o comando `git checkout main`
* Se você estiver no branch principal, será possível mesclar nele as atualizações feitas no branch de treinamento com `git merge <branch to merge>`

<details>
  <summary>  Possivel mensagem de erro: </summary>
  <p>Se você for a única pessoa que fez atualizações no arquivo que está tentando realizar a mesclagem, o processo deverá ser contínuo (é uma boa ideia executar git pull antes de iniciar o trabalho).</p> <br>
  <p>Se outras alterações tiverem sido feitas, você precisará gerenciar o conflito. Todos os arquivos com um conflito serão atualizados para incluir ambas as versões do conteúdo em um único arquivo. Se você abrir o arquivo, verá as alterações e a versão atual do conteúdo (como ele existe no repositório). É possível atualizar e fazer novamente commit do arquivo de maneira manual, o que efetivamente concluirá a mesclagem.</p>
  <img align="center" alt="git-merge-conflict" width=750px src="https://github.com/user-attachments/assets/41805c0a-42cc-44b6-ad63-2c1322e38f7c">
  <p>Depois de fazer edições no arquivo, você precisará executar o comando git add para preparar o arquivo e, em seguida, git commit -m "<your comment>" para fazer commit do arquivo no branch atual do repositório.</p> 
  <p>Obs:Você não precisa fazer novamente a mesclagem porque, ao concluir git commit, você atualiza o arquivo no branch</p>
</details>
