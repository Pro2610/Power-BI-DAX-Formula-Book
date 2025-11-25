Sales High Margin :=
CALCULATE(
    SUM(Sales[Amount]),
    Products[Margin] > 0.30
)
