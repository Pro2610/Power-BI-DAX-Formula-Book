(фільтр по динамічному значенню)
Sales for Current Category =
CALCULATE (
    SUM ( Sales[Amount] ),
    KEEPFILTERS ( Sales[Category] = SELECTEDVALUE ( Sales[Category] ) )
)
