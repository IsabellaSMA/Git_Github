<h1 align=center>Eventos</h1>

<h2 align=center>Eventos agendados</h2>

Com esse tipo de gatilho, um agendamento cron precisa ser fornecido. Os agendamentos do Cron são baseados em cinco valores:
* Minuto (0 a 59)
* Hora (0 a 23)
* O dia do mês (1 a 31)
* Mês (1 a 12)
* Dia da semana (0 a 6)

Aliases para os meses são JAN-DEC e, para os dias da semana, são SUN-SAT.

Um curinga significa qualquer um. (* é um valor especial em YAML, portanto, a cadeia de caracteres cron precisará estar entre aspas)

No exemplo abaixo, o agendamento seria das 8h às 17h de segunda a sexta-feira

`YAML`

    on:

    schedule:

        - cron: '0 8-17 * * 1-5'


<h2 align=center>Eventos de código</h2>

Eventos de código dispararão a maioria das ações. Isso acontece quando ocorre um evento de interesse no repositório. Exemplo de evento de solicitação de pull:

`YAML`

    on:

    pull_request

Exemplo de evento de solicitação de pull ou push:

`YAML`

    on:

    [push, pull_request]

Exemplo de evento de como ser específico sobre a seção relevante do código

`YAML`

    on:

    pull_request:
        branches:

            - develop

<h2 align=center>Eventos manuais</h2>

Há um evento exclusivo usado para disparar as execuções de fluxo de trabalho manualmente. Use o evento **workflow_dispatch**. Seu fluxo de trabalho deve estar na ramificação padrão do repositório.


<h2 align=center>Eventos do webhook</h2>
Fluxos de trabalho podem ser executados quando um webhook do GitHub é chamado. Esse evento seria disparado quando alguém atualizasse (ou criasse primeiro) uma página do Wiki:

`YAML`

    on: gollum

 <h2 align=center>Eventos externos</h2>
 
 Os eventos podem estar em **repository_dispatch**. Isso permite que os eventos sejam disparados de sistemas externos
