(вибір альтернативного зв’язку)
Sales by Ship Date =
CALCULATE (
    SUM ( Sales[Amount] ),
    USERELATIONSHIP ( Dates[Date], Sales[ShipDate] )
)
