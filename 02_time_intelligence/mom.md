Total Sales :=
SUM ( Sales[Amount] )

Sales MoM % :=
VAR PrevMonth =
    CALCULATE ( [Total Sales], DATEADD ( 'Date'[Date], -1, MONTH ) )
RETURN
DIVIDE ( [Total Sales] - PrevMonth, PrevMonth )
