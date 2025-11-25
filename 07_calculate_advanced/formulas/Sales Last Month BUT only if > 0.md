Sales LM Positive :=
VAR lm =
    CALCULATE(
        SUM(Sales[Amount]),
        DATEADD(DimDate[Date], -1, MONTH)
    )
RETURN
IF(lm > 0, lm)
