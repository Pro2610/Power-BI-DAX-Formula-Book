Sales A Premium :=
CALCULATE(
    SUM(Sales[Amount]),
    Products[ProductName] = "A",
    Products[Category] = "Premium"
)
