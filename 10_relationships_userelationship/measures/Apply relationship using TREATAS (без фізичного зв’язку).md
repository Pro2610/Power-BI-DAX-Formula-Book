Sales via TREATAS :=
CALCULATE (
    [Total Sales],
    TREATAS ( VALUES ( DimRegion[RegionCode] ), Sales[RegionCode] )
)
