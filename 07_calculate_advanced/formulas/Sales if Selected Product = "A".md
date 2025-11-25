Sales Only If A :=
IF(
    SELECTEDVALUE(Products[ProductName]) = "A",
    CALCULATE(SUM(Sales[Amount])),
    BLANK()
)
