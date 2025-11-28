Sales One Direction :=
CALCULATE (
    [Total Sales],
    CROSSFILTER ( Customers[CustomerID], Sales[CustomerID], ONEWAY )
)
