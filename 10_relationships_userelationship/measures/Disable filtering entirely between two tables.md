Sales Ignore Customer Filter :=
CALCULATE (
    [Total Sales],
    CROSSFILTER ( Customers[CustomerID], Sales[CustomerID], NONE )
)
