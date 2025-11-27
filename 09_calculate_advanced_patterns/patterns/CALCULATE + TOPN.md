Top 5 Products Sales =
CALCULATE (
    SUM ( Sales[Amount] ),
    KEEPFILTERS (
        TOPN ( 5, Products, Products[Sales], DESC )
    )
)
