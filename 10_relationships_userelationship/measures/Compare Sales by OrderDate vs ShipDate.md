Sales Comparison :=
VAR ByOrder = [Total Sales]
VAR ByShip  =
    CALCULATE (
        [Total Sales],
        USERELATIONSHIP ( Sales[ShipDate], Calendar[Date] )
    )
RETURN
    ByOrder - ByShip
