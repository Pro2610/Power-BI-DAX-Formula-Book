Total Sales (All) =
CALCULATE (
    SUM ( Sales[Amount] ),
    REMOVEFILTERS ( Sales )
)
