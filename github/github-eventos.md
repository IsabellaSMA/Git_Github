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
