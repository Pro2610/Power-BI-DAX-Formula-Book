Sales A or HighMargin :=
CALCULATE(
    SUM(Sales[Amount]),
    Products[ProductName] = "A"
        || Products[Margin] > 0.30
)
