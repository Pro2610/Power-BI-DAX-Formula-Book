Net Profit :=
VAR Revenue =
    SUMX ( Sales, Sales[Quantity] * Sales[Price] )
VAR COGS =
    SUMX ( Sales, Sales[Quantity] * Sales[COGS] )
VAR OperatingCost =
    SUM ( Finance[OperatingCost] )
RETURN
Revenue - COGS - OperatingCost
