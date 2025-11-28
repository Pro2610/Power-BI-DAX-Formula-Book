Sales Dual :=
VAR Mode = SELECTEDVALUE ( 'Date Mode'[Mode] )   -- 'Order' or 'Ship'
RETURN
    SWITCH (
        Mode,
        "Order", [Total Sales],
        "Ship",
            CALCULATE (
                [Total Sales],
                USERELATIONSHIP ( Sales[ShipDate], Calendar[Date] )
            )
    )
