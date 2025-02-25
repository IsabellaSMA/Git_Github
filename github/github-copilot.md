<h1 align=center>Github Copilot </h1>
É um assistente de código que ajuda-nos a ecrever códigos mais rápido com menos eforço dando mais espaço ao programador a focar em outras soluções de problemas, ou seja, ajuda na produtividade.

## Como funciona:

De token em token: subdividindo as coisas para serem escritos.[^1]





<h2 align=center> Integração do GitHub Copilot ao ambiente de desenvolvedor</h2>

O GitHub Copilot integra-se nativamente ao Visual Studio Code, ao Visual Studio e a outros ambientes de desenvolvedor.

O GitHub Copilot é implementado usando duas extensões para o Visual Studio Code: GitHub Copilot e GitHub Copilot Chat.

* A extensão do GitHub Copilot fornece conclusões de código e geração de código a partir de comentários. Ferramentas avançadas que ajudam os desenvolvedores a escrever código de forma mais rápida e inteligente.
* A extensão GitHub Copilot Chat fornece ao editor uma interface de chat habilitada para IA focada em cenários de desenvolvedor. Ela reconhece todo o workspace do projeto, as revisões de código que estão sendo inseridas, mensagens de erro e outros aspectos do ambiente do compilador/runtime. Os desenvolvedores podem usar o Copilot Chat para obter uma análise detalhada de seu código, investigar novos recursos, aprimorar ou refatorar recursos existentes, gerar testes de unidade e até mesmo receber correções propostas para bugs.

<h2 align=center> Chat do GitHub Copilot</h2>

### Como ele funciona
O Chat do GitHub Copilot usa uma combinação de processamento de linguagem natural e aprendizado de máquina para entender sua pergunta e fornecer uma resposta. Esse processo pode ser dividido nas seguintes etapas.

### Processamento de entrada
O prompt de entrada do usuário é pré-processado pelo sistema de Chat do Copilot e enviado para um modelo de linguagem grande para obter uma resposta com base no contexto e no prompt. A entrada do usuário pode assumir a forma de snippets de código ou linguagem sem codificação. O sistema se destina apenas a responder a perguntas relacionadas à codificação.

### Análise de modelo de linguagem
Em seguida, o prompt pré-processado é passado pelo modelo de linguagem de Chat do Copilot, que é uma rede neural que foi treinada em um grande corpo de dados de texto. O modelo de linguagem analisa o prompt de entrada.

### Geração de resposta
O modelo de linguagem gera uma resposta com base na análise do prompt de entrada e no contexto fornecido. Essa resposta pode assumir a forma de código gerado, sugestões de código ou explicações do código existente.

### Formatação de saída
A resposta gerada pelo Chat do Copilot é formatada e apresentada ao usuário. O Chat do Copilot pode usar realce de sintaxe, recuo e outros recursos de formatação para adicionar clareza à resposta gerada. Dependendo do tipo de pergunta do usuário, links para o contexto que o modelo usou ao gerar uma resposta, como arquivos de código-fonte ou documentação, também podem ser fornecidos.

O Chat do GitHub Copilot destina-se a fornecer a resposta mais relevante para sua pergunta. No entanto, ele pode nem sempre fornecer a resposta que você está procurando. Os usuários do Chat do Copilot são responsáveis por revisar e validar as respostas geradas pelo sistema para garantir que elas sejam precisas e apropriadas.

<h2 align=center> Casos de uso para o Chat do GitHub Copilot</h2>

### Explicando e documentando código
O Chat do Copilot pode ajudar a explicar o código selecionado gerando descrições de linguagem natural da funcionalidade e da finalidade do código. Isso pode ser útil se você quiser entender o comportamento do código ou para stakeholders não técnicos que precisam entender como o código funciona. Por exemplo, se você selecionar uma função ou um bloco de código no editor de código, o Chat do Copilot poderá gerar uma descrição de linguagem natural do que o código faz e como ele se encaixa no sistema geral. Isso pode incluir informações como os parâmetros de entrada e saída da função, as dependências e a finalidade no aplicativo maior.

Ao gerar explicações e documentação, o Chat do Copilot pode ajudar você a entender o código selecionado, levando a uma colaboração aprimorada e um desenvolvimento de software mais eficaz.

### Respostas a perguntas de codificação
Você pode pedir ajuda ou esclarecimentos ao Chat do Copilot sobre problemas de codificação específicos e receber respostas no formato de linguagem natural ou no formato de snippet de código. Essa é uma ferramenta útil para programadores porque fornece diretrizes e suporte para tarefas e desafios comuns de codificação.

### Propondo correções de bug
O Chat do Copilot pode propor uma correção para bugs em seu código sugerindo snippets de código e soluções com base no contexto do erro ou problema. Isso é útil se você estiver lutando para identificar a causa raiz de um bug ou precisar de orientação sobre a melhor maneira de corrigi-lo. Por exemplo, se o código produzir uma mensagem de erro ou um aviso, o Chat do Copilot poderá sugerir possíveis correções com base na mensagem de erro, na sintaxe do código e no código ao redor.

O Chat do Copilot pode sugerir alterações em variáveis, estruturas de controle ou chamadas de função que podem resolver o problema e gerar snippets de código que podem ser incorporados à base de código. No entanto, é importante observar que as correções sugeridas nem sempre são ideais ou estão completas, portanto, você precisa examinar e testar as sugestões.

### Gerar casos de teste de unidade
O Chat do Copilot pode ajudá-lo a escrever casos de teste de unidade gerando snippets de código com base no código aberto no editor ou no snippet de código realçado no editor. Isso ajuda você a escrever casos de teste sem gastar tanto tempo em tarefas repetitivas. Por exemplo, se estiver escrevendo um caso de teste para uma função específica, você poderá usar o Chat do Copilot para sugerir possíveis parâmetros de entrada de dados e valores de resultado esperados com base na assinatura e no corpo da função. O Chat do Copilot também pode sugerir declarações que garantam que a função esteja funcionando corretamente, com base no contexto e na semântica do código.

O Chat do Copilot também pode ajudar você a escrever casos de teste para casos de borda e condições de limite que podem ser difíceis de se identificar manualmente. Por exemplo, o Chat do Copilot pode sugerir casos de teste para tratamento de erros, valores nulos ou tipos de entrada inesperados, ajudando você a garantir que seu código seja robusto e resiliente. No entanto, é importante observar que os casos de teste gerados podem não abranger todos os cenários possíveis, e testes manuais e revisão de código ainda são necessários para garantir a qualidade do código.

### Sugerindo melhorias em uma base de código existente
O Chat do Copilot também pode sugerir possíveis melhorias no código selecionado. Por exemplo, o Copilot Chat pode sugerir melhorias nas seguintes categorias:

### Qualidade do código: 
O Chat do Copilot pode sugerir maneiras de melhorar a legibilidade, a manutenção e o desempenho do código. Isso pode incluir sugestões de refatoração, simplificação de código e modularidade.

### Confiabilidade do código:
O Chat do Copilot pode sugerir maneiras de tornar seu código mais robusto e confiável. Isso pode incluir sugestões de tratamento de erros, validação de entrada e programação defensiva.

### Desempenho do código:
O Chat do Copilot pode sugerir maneiras de otimizar o desempenho do código. Isso pode incluir sugestões de melhorias algorítmicas, otimizações de estrutura de dados e paralelização.

### Segurança do código: O Chat do Copilot pode sugerir maneiras de tornar seu código mais seguro. Isso pode incluir sugestões de sanitização de entrada, controle de acesso e criptografia.
Ao sugerir melhorias, o Chat do Copilot pode ajudar você a escrever um código melhor que seja mais legível, confiável, com desempenho e seguro.

<h2 align=center> Limitações do GitHub Copilot Chat</h2>

### Escopo limitado
O GitHub Copilot Chat é treinado em um grande corpo de código, mas ainda tem um escopo limitado. Ele pode não ser capaz de lidar com algumas estruturas de código complexas ou linguagens de programação obscuras. Para cada linguagem de programação, a qualidade das sugestões recebidas pode depender do volume e da diversidade de dados de treinamento para esse idioma. Por exemplo, o JavaScript é bem representado em repositórios públicos e é uma das linguagens com melhor suporte do GitHub Copilot. Linguagens com menos representação em repositórios públicos podem ser mais desafiadoras para o Copilot Chat. Além disso, o Copilot Chat só pode sugerir código com base no contexto do código que está sendo escrito, portanto, ele pode não ser capaz de identificar problemas maiores de design ou arquitetura.

Possíveis desvios
Os dados de treinamento do GitHub Copilot são extraídos de repositórios de código existentes que podem conter desvios e erros. O GitHub Copilot poderá perpetuar os desvios se eles existirem nos dados de treinamento. O GitHub Copilot Chat pode ser tendencioso em relação a determinadas linguagens de programação ou estilos de codificação, o que pode levar a sugestões de código abaixo do ideal ou incompletas.

### Riscos à segurança
O Copilot Chat gera código com base no contexto do código que está sendo escrito, que pode potencialmente expor informações confidenciais ou vulnerabilidades se não for usado com cuidado. Você deve ter cuidado ao usar o Copilot Chat para gerar código para aplicativos sensíveis à segurança e sempre examinar e testar o código gerado minuciosamente.

### Correspondências com código público
O Copilot Chat é capaz de gerar um novo código e faz isso de forma probabilística. A probabilidade de o Copilot Chat produzir um código que corresponda ao código no conjunto de treinamento é baixa, mas não zero. Uma sugestão do Copilot Chat pode conter alguns snippets de código que correspondem ao código no conjunto de treinamento. O Copilot Chat usa filtros que bloqueiam correspondências com código público em repositórios do GitHub, mas você ainda deve tomar precauções. Você deve tratar as sugestões do GitHub Copilot da mesma maneira que trataria qualquer código que use um material que você não criou. Isso inclui precauções para garantir sua adequação. Isso inclui testes rigorosos, verificação de IP e acompanhamento de vulnerabilidades de segurança. Você deve verificar se o IDE ou o editor não compila ou executa automaticamente o código gerado antes de revisá-lo.

### Código impreciso
O GitHub Copilot Chat pode gerar um código que parece ser válido, mas não é. O código pode não estar semanticamente ou sintaticamente correto, ou pode não refletir com precisão a intenção do desenvolvedor. Para atenuar o risco de código impreciso, você deve examinar e testar cuidadosamente o código gerado. Isso é particularmente importante ao lidar com aplicativos críticos ou confidenciais. Você também deve garantir que o código gerado siga práticas recomendadas e os padrões de design e se encaixe na arquitetura geral e no estilo da base de código.

### Respostas imprecisas a tópicos de não codificação
O Copilot Chat não foi projetado para responder a perguntas não codificadas e, portanto, suas respostas podem nem sempre ser precisas ou úteis nesses contextos. Se um usuário fizer uma pergunta de não codificação ao Copilot Chat, ele poderá gerar uma resposta irrelevante ou sem sentido, ou pode simplesmente indicar que não é possível fornecer uma resposta útil.

[^1]:Tokenizer
