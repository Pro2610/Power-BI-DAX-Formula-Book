Sales Large Orders :=
CALCULATE(
    SUM(Sales[Amount]),
    Sales[Amount] > 1000
)
