Orders by Created Date :=
CALCULATE (
    DISTINCTCOUNT ( Sales[OrderID] ),
    USERELATIONSHIP ( Sales[CreatedDate], Calendar[Date] )
)
