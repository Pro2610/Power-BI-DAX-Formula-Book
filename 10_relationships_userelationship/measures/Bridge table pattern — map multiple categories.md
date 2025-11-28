Sales by Category Bridge :=
CALCULATE (
    [Total Sales],
    TREATAS ( VALUES ( Bridge[Category] ), Sales[Category] )
)
