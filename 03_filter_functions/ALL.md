Active Customers :=
CALCULATE (
    DISTINCTCOUNT ( Sales[CustomerID] ),
    Sales[Amount] > 0
)
