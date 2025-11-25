Sales CY :=
CALCULATE(
    SUM(Sales[Amount]),
    YEAR(DimDate[Date]) = YEAR(TODAY())
)
