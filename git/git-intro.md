<p align= center>
  <img src="https://i1.wp.com/taaism.com/wp-content/uploads/2016/03/git-logo.png?fit=300%2C125">
</p>
<br>

# 

<h3 align= center>História</h3>

<p align=center> Projetado para ser rápido, eficiente e permitir que vários desenvolvedores trabalhassem em diferentes partes do projeto ao mesmo tempo. Git foi criado por Linus Torvalds em 2005, o criador também do Linux. O Git foi desenvolvido para resolver problemas de controle de versão no desenvolvimento do kernel do Linux. Antes do Git, a comunidade do Linux usava um sistema chamado BitKeeper, mas quando a relação entre a comunidade e os desenvolvedores do BitKeeper quebrou, Linus decidiu criar seu próprio sistema de controle de versão. 
</p>

#

<h3 align=center> O que é controle de Versão? </h3>
VCS (sistema de controle de versão) ou SCM (Gerenciamento de Configuração de Software) é um programa ou um conjunto de programas que controla as alterações feitas em uma coleção de arquivos.

<h3> Funcionalidades </h3> 

* Recuperar com facilidade as versões anteriores de arquivos individuais ou do projeto inteiro.
* Permitir que vários membros da equipe trabalhem em um projeto, até mesmo nos mesmos arquivos, simultaneamente sem afetar uns aos outros.
* Ver todas as alterações feitas no projeto, quando as alterações foram feitas e quem as fez.
* Incluir uma mensagem com cada alteração para explicar o raciocínio por trás dela.
* Criar branches, em que as alterações podem ser feitas de maneira experimental. Esse recurso permite que vários conjuntos diferentes de alterações (por exemplo, recursos ou correções de bug) sejam trabalhados ao mesmo tempo, possivelmente por pessoas diferentes, sem afetar a ramificação principal. Assim como a possibilidade de mesclar as alterações que deseja manter na ramificação principal.
* Anexar uma marca a uma versão, por exemplo, para marcar uma nova versão.

<br>

<details>
  <summary> Controle de versão distribuído</summary> <br>
    <p > O Git é distribuído, o que significa que o histórico completo de um projeto é armazenado no cliente e no servidor. Você pode editar arquivos sem uma conexão de rede, verificá-los localmente e sincronizá-los com o servidor quando uma conexão fica disponível. Se um servidor ficar inativo, você ainda terá uma cópia local do projeto. Tecnicamente, você nem precisa ter um servidor. Todos aqueles que estão conectados podem ter uma cópia completa do repositório no momento em que o baixam, incluindo o histórico e as notas associados a ele.
    </p>
</details>
 

<h3 align=center>Terminologia </h3>

* #### *Árvore de trabalho*:
   Conjunto de diretórios e arquivos aninhados que contém o projeto no qual está sendo feito o trabalho; 
  
* #### *Repositório*:
  
  O diretório,é o projeto ou pasta de nível superior em que o código ou os arquivos são organizados. Ele é semelhantes às estruturas de pastas no computador. Mantém todo o histórico e os metadados de um projeto. <br>
**Repositório Simples:** não faz parte de uma árvore de trabalho é usado para compartilhamento ou backup. Geralmente é um diretório que termina com .git (ex. project.git)

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

* #### *Ramificação e mesclagem*:
  Os branches permitem criar cópias do código existente e, em seguida, criar branches para trabalhar em algo que não afete a versão principal ou ativa do código. se você encontrar em um dos branches algo que deseja incorporar à versão principal do código, será possível fazer isso facilmente "mesclando" o código em branch ao código principal. Dessa forma, é possível trabalhar em uma correção ou em um novo recurso e, quando ele estiver funcionando e testado, mesclá-lo no branch ativo e implantá-lo para o público.
<br> **Solicitação de pull**: Se você não tem autoridade com relação ao branch principal do repositório de origem, talvez seja necessário criar uma solicitação de pull, uma solicitação de mesclagem ou um pull de solicitação. Essas solicitações são a mesma coisa com nomes diferentes, dependendo da plataforma usada. Elas consistem simplesmente em uma solicitação sua à autoridade do branch principal para incorporar as atualizações a esse branch.

* #### *Clonagem e pull*
Ao trabalhar com o Git como sua escolha de controle de versão e código-fonte, é possível “unir” um repositório existente ou criar o seu próprio desde o início. Ao trabalhar com um repositório existente, é preciso começar com a clonagem dele. A clonagem do repositório cria uma cópia completa e exata dele. Ao clonar o repositório, você obtém a estrutura, todos os arquivos e todo o histórico associado a ele.
Como o Git funciona de maneira distribuída, isso significa que você tem uma cópia completa do repositório sempre que o clona. Se você não estiver preocupado com as atualizações feitas por outras pessoas, nunca precisará voltar ao repositório. No entanto, isso também é uma desvantagem. Se você não voltar e atualizar sua cópia do repositório em relação à origem, ficará fora de sincronização. O pull é semelhante à clonagem, mas serve para manter a continuidade após a clonagem inicial.
Tanto a clonagem quanto o pull de repositórios ajudarão você a obter e manter as versões, os históricos e os comentários mais recentes.




<h2 align=center> Git vs Github: Qual a diferença? </h2>

**Git** é um DVCS (sistema de controle de versão distribuído) que pode ser usado por vários desenvolvedores e outros colaboradores para trabalhar em um projeto. Ele fornece um modo de trabalhar com um ou mais branches locais e os envia por push para um repositório remoto.

**GitHub** O GitHub é um serviço de hospedagem de repositório que usa a estrutura Git para fornecer uma solução de controle de versão e de código-fonte, uma plataforma de nuvem e o repositório remoto que usa o Git como sua tecnologia principal. O GitHub simplifica o processo de colaboração em projetos e fornece um site, mais ferramentas de linha de comando e um fluxo geral que pode ser usado pelos desenvolvedores e pelos usuários para trabalhar juntos.


[^1]: função de Hash: fórmula matemática que pega os dados e gera essa "impressão digital",transformando dados de qualquer tamanho em um código de tamanho fixo (o hash).
[^2]: Exemplo: Imagine um Readme e nele é adicionado a frase "Olá, mundo!", nisto a função de Hash gera um código (ex. 123abc); Voltando no mesmo arquivo e se for feito uma alteração exemplo "Olá, Mundo!", mesmo que seja sutil, a funçã de hash cria um novo código para esta mudança (ex. 456def).
