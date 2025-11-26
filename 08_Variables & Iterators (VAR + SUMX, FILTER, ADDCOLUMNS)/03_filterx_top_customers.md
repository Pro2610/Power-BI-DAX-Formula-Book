Top Customers Revenue :=
VAR TopCust =
    CALCULATETABLE (
        VALUES ( Customers[CustomerID] ),
        TOPN (
            10,
            SUMMARIZE ( Sales, Sales[CustomerID], "Rev", SUMX ( Sales, Sales[Quantity] * Sales[Price] ) ),
            [Rev],
            DESC
        )
    )
RETURN
SUMX (
    TopCust,
    CALCULATE ( SUMX ( Sales, Sales[Quantity] * Sales[Price] ) )
)
