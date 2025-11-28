ShipDate YTD :=
CALCULATE (
    [Total Sales],
    USERELATIONSHIP ( Sales[ShipDate], Calendar[Date] ),
    DATESYTD ( Calendar[Date] )
)
