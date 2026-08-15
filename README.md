Total Tickets	Total Tickets = COUNTROWS(Table1_2)

Resolved Tickets	Resolved Tickets = CALCULATE(COUNTROWS(Table1_2), Table1_2[Status] = "Resolved")

SLA Met Tickets	SLA Met Tickets = CALCULATE(COUNTROWS(Table1_2), Table1_2[SLA_Status] = "SLA Met")

SLA Breached Tickets	SLA Breached Tickets = CALCULATE(COUNTROWS(Table1_2), Table1_2[SLA_Status] = "SLA Breached")

SLA Compliance %	SLA Compliance % = DIVIDE([SLA Met Tickets], [SLA Met Tickets] + [SLA Breached Tickets])

Average Resolution Hours	Average Resolution Hours = AVERAGE(Table1_2[Resolution_Hours])

Average Customer Rating	Average Customer Rating = AVERAGE(Table1_2[Customer_Rating])

Escalated Tickets	Escalated Tickets = CALCULATE(COUNTROWS(Table1_2), Table1_2[Escalated] = "Yes")

Escalation Rate	Escalation Rate = DIVIDE([Escalated Tickets], [Total Tickets])
