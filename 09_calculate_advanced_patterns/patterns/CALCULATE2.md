з декількома умовами
Promo Sales =
CALCULATE (
    SUM ( Sales[Amount] ),
    Sales[IsPromo] = TRUE(),
    Sales[Amount] > 50
)
