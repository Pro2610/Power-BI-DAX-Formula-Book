Sales All Products :=
CALCULATE(
    SUM(Sales[Amount]),
    ALL(Products)
)
