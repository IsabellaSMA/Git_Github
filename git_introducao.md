<h1 align=center img href=""> Curso de Git </h1>
<br>

<h2 align= center>História</h2>
<p align=center> O autor principal é Linus Torvalds, o criador do Linux. </p>


<h3> O que é controle de Versão? </h3>
VCS (sistema de controle de versão) ou SCM (Gerenciamento de Configuração de Software) é um programa ou um conjunto de programas que controla as alterações feitas em uma coleção de arquivos.

<h3> Funcionalidades </h3> 

* Recuperar com facilidade as versões anteriores de arquivos individuais ou do projeto inteiro.
* Permitir que vários membros da equipe trabalhem em um projeto, até mesmo nos mesmos arquivos, simultaneamente sem afetar uns aos outros.
* Ver todas as alterações feitas no projeto, quando as alterações foram feitas e quem as fez.
* Incluir uma mensagem com cada alteração para explicar o raciocínio por trás dela.
* Criar branches, em que as alterações podem ser feitas de maneira experimental. Esse recurso permite que vários conjuntos diferentes de alterações (por exemplo, recursos ou correções de bug) sejam trabalhados ao mesmo tempo, possivelmente por pessoas diferentes, sem afetar a ramificação principal. Assim como a possibilidade de mesclar as alterações que deseja manter na ramificação principal.
* Anexar uma marca a uma versão, por exemplo, para marcar uma nova versão.

<details>
  <summary> Controle de versão distribuído</summary> <br>
    <p > O Git é distribuído, o que significa que o histórico completo de um projeto é armazenado no cliente e no servidor. Você pode editar arquivos sem uma conexão de rede, verificá-los localmente e sincronizá-los com o servidor quando uma conexão fica disponível. Se um servidor ficar inativo, você ainda terá uma cópia local do projeto. Tecnicamente, você nem precisa ter um servidor. As alterações podem ser passadas por email ou compartilhadas por uma mídia removível, mas ninguém usa o Git dessa maneira na prática
    </p>
</details>
 

<h3>Terminologia </h3>

* #### *Árvore de trabalho*:
   Conjunto de diretórios e arquivos aninhados que contém o projeto no qual está sendo feito o trabalho; 
  
* #### *Repositório*:
   O diretório. Mantém todo o histórico e os metadados de um projeto. Repositório Simples: não faz parte de uma árvore de trabalho é usado para compartilhamento ou backup. Geralmente é um diretório que termina com .git (ex. project.git)

* #### *Hash*:
   Produzido por uma Função de Hash[^1] . Um hash é como uma impressão digital para dados. É um número gerado a partir do conteúdo de um arquivo ou mensagem. Cada pequeno detalhe dos dados produz um hash único. Se qualquer parte do conteúdo muda, o hash também muda. [^2]
  
* #### *Objeto*:
   Há quatro tipos dentro de um repositório,cada um identificado por um hash SHA-1. Um objeto de blob contém um arquivo comum. Um objeto de árvore representa um diretório; ele contém nomes, hashes e permissões. Um objeto de commit representa uma versão específica da árvore de trabalho. Uma marca é um nome anexado a um commit.
  
* #### *Commit*:
    Adicionar uma atualização no projeto e "avisar" aos outros colaboradores através da seção de comentários o que foi feito e/ou a linha de raciocínio usada.
  
* #### *Branch*:
    Uma espécie de linha do tempo editavel. Cada branch representa uma versão separada do seu código onde você pode fazer alterações sem afetar a linha principal (geralmente chamada de main ou master). Isso permite que diferentes funcionalidades sejam desenvolvidas de forma independente e depois unidas novamente à linha principal através de um processo chamado merge.  
  
* #### *Repositório Remoto*:
  Referência nomeada a outro repositório Git. Quando repositório é criado no Github, o Git cria um repositório remoto chamado origin, que é o repositório remoto padrão das operações de push e pull.
  
* #### *Comandos, Subcomandos e opções*:
    As operações do git são realizadas por meio de comandos. git é o comando principal e o que vem depois é o subcomando, especificando a operação que você deseja que o git execute  (ex. git push). Os comandos são frequentemente acompanhados por hífens simples (ex git commit -m "meu commit") ou duplos (git reset-- hard)

## Git vs Github: Qual a diferença? 

**Git** é um DVCS (sistema de controle de versão distribuído) que pode ser usado por vários desenvolvedores e outros colaboradores para trabalhar em um projeto. Ele fornece um modo de trabalhar com um ou mais branches locais e os envia por push para um repositório remoto.

**GitHub** é uma plataforma de nuvem e o repositório remoto que usa o Git como sua tecnologia principal. O GitHub simplifica o processo de colaboração em projetos e fornece um site, mais ferramentas de linha de comando e um fluxo geral que pode ser usado pelos desenvolvedores e pelos usuários para trabalhar juntos.


[^1]: função de Hash: fórmula matemática que pega os dados e gera essa "impressão digital",transformando dados de qualquer tamanho em um código de tamanho fixo (o hash).
[^2]: Exemplo: Imagine um Readme e nele é adicionado a frase "Olá, mundo!", nisto a função de Hash gera um código (ex. 123abc); Voltando no mesmo arquivo e se for feito uma alteração exemplo "Olá, Mundo!", mesmo que seja sutil, a funçã de hash cria um novo código para esta mudança (ex. 456def).
