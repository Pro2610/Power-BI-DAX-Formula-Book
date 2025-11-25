Balance EoM :=
CALCULATE(
    LASTNONBLANKVALUE(
        DimDate[Date],
        SUM(Sales[Balance])
    ),
    ENDOFMONTH(DimDate[Date])
)
