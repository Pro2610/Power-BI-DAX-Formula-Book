Total Sales by Ship Date :=
CALCULATE (
    [Total Sales],
    USERELATIONSHIP ( Sales[ShipDate], Calendar[Date] )
)
