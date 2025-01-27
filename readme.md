<h1 align=center> Curso de Git </h1>
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
 

### Terminologia

* *Árvore de trabalho*: Conjunto de diretórios e arquivos aninhados que contém o projeto no qual está sendo feito o trabalho;
  
* *Repositório*: O diretório. Mantém todo o histórico e os metadados de um projeto. Repositório Simples: não faz parte de uma árvore de trabalho é usado para compartilhamento ou backup. Geralmente é um diretório que termina com .git (ex. project.git)



* *Hash*: um número produzido por uma Função de Hash[^1] que representa o conteúdo de um arquivo ou de outro objeto como um número fixo de dígitosvantagem de usar hashes é que o Git pode informar se um arquivo foi alterado pelo hash do conteúdo e pela comparação do resultado com o hash anterior. Se o carimbo de data/hora do arquivo for alterado, mas o hash do arquivo não, o Git saberá que o conteúdo do arquivo não foi alterado.
  
* *Objeto*: há quatro tipos dentro de um repositório,cada um identificado por um hash SHA-1. Um objeto de blob contém um arquivo comum. Um objeto de árvore representa um diretório; ele contém nomes, hashes e permissões. Um objeto de commit representa uma versão específica da árvore de trabalho. Uma marca é um nome anexado a um commit.
  
* *Commit*:
  
* *Branch*:
  
* *Repositório Remoto*:
  
* *Comandos, Subcomandos e opções*:

[^1]: função de Hash 
