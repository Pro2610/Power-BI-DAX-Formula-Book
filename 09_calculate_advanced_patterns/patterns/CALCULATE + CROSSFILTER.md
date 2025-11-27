Sales Bidirectional =
CALCULATE (
    SUM ( Sales[Amount] ),
    CROSSFILTER ( Sales[CustomerID], Customers[CustomerID], BOTH )
)
