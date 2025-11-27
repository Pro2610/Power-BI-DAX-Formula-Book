з умовним фільтром (логічний вираз)
High Value Sales =
CALCULATE (
    SUM ( Sales[Amount] ),
    Sales[Amount] > 1000
)
