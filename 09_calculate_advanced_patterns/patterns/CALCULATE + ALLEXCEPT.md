Total Sales by Product (Ignoring Date) =
CALCULATE (
    SUM ( Sales[Amount] ),
    ALLEXCEPT ( Sales, Sales[Product] )
)
