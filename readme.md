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

### Controle de versão distribuído
As instâncias anteriores dos VCSs, como o CVS, o Subversion (SVN) e o Perforce, usavam um servidor centralizado para armazenar o histórico de um projeto. Essa centralização significava que o único servidor também era, potencialmente, um ponto único de falha.

O Git é distribuído, o que significa que o histórico completo de um projeto é armazenado no cliente e no servidor. Você pode editar arquivos sem uma conexão de rede, verificá-los localmente e sincronizá-los com o servidor quando uma conexão fica disponível. Se um servidor ficar inativo, você ainda terá uma cópia local do projeto. Tecnicamente, você nem precisa ter um servidor. As alterações podem ser passadas por email ou compartilhadas por uma mídia removível, mas ninguém usa o Git dessa maneira na prática.

### Terminologia

Árvore de trabalho:
Repositório:
Hash:
Objeto:
Commit:
Branch:
Repositório Remoto:
Comandos, Subcomandos e opções:
