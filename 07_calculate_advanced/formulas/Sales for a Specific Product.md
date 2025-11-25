Sales Product A :=
CALCULATE(
    SUM(Sales[Amount]),
    Products[ProductName] = "A"
)
