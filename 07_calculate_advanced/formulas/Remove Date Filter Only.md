Sales Ignore Date :=
CALCULATE(
    SUM(Sales[Amount]),
    REMOVEFILTERS(DimDate)
)
