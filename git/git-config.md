
<h1 align=center> Configurar o git</h1>

<img align="right" alt="" height="130px" src="https://th.bing.com/th/id/R.9768387cf34d18a2ece14af4992e5071?rik=fl%2bZ5MMUtF%2fuCQ&pid=ImgRaw&r=0">


Para verificar novamente se o Git está instalado, digite: *`git --version`*


Para configurar o Git, é necessário definir algumas variáveis globais como *user.name* e *user.email* . As duas são necessárias para fazer commits

<h3 align=center> Definir o nome: </h3>
Git Bash 

`git config --global user.name "<USER_NAME>"` 
* Substitua <USER_NAME> pelo nome de usuário que deseja usar.


<h3 align=center> Definir email:</h3>
`git config --global user.email "<USER_EMAIL>"`
* subistitua  <USER_EMAIL> pelo seu endereço de email
<br>

Para verificar se as alterações funcionaram: `git config --list`

A saída inclui duas linhas semelhantes ao exemplo a seguir: 

`user.name=User Name` <br>
`user.email=user-name@contoso.com`

<h2 align=center> Configurar repositório Git</h2>

O Git funciona verificando a presença de alterações em arquivos de determinada pasta. Criaremos uma pasta para que ela sirva como a árvore de trabalho (diretório do projeto) e indicaremos isso ao Git, de modo que ele possa começar a controlar as alterações. 



1. Criação da pasta Cats: `mkdir Cats`
* Essa pasta será o diretório do projeto, também chamado de árvore de trabalho. O diretório do projeto é o local em que todos os arquivos relacionados ao seu projeto são armazenados. Neste exercício, é o local em que o site e os arquivos que criam o site e o conteúdo são armazenados.


2. Alteração para o diretório do projeto usando o comando cd:
`cd Cats`

4. inicializando o novo repositório e definindo o nome do branch padrão como main:
   * Se estiver usando Git versão 2.28.0 ou posterior: `git init --initial-branch=main` ou `git init -b main`
   * Em versões anteriores: `git init git checkout -b main`
       
6. Agora, use um comando `git status` para mostrar o status da árvore de trabalho

7. Use um comando ls para mostrar o conteúdo da árvore de trabalho:
  `ls -a`
   * Confirme se o diretório contém um subdiretório chamado .git. (O uso da opção -a com ls é importante, porque o Linux normalmente oculta os nomes de arquivos e diretórios que começam com um ponto.) Essa pasta é o repositório Git, o diretório no qual o Git armazena os metadados e o histórico da árvore de trabalho.
Normalmente, você não faz nada com o diretório .git diretamente. O Git atualiza os metadados nele, pois o status da árvore de trabalho é alterado para controlar as alterações nos arquivos. Esse diretório não exige nenhuma intervenção de sua parte, mas é incrivelmente importante para o Git.

* Para obter ajuda do git digite `git --help`




