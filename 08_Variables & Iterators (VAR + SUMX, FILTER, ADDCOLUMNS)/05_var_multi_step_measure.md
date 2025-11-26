Net Profit :=
VAR Revenue =
    SUMX ( Sales, Sales[Quantity] * Sales[Price] )
VAR COGS =
    SUMX ( Sales, Sales[Quantity] * Sales[COGS] )
VAR OperatingCost =
    SUM ( Finance[OperatingCost] )
RETURN
Revenue - COGS - OperatingCost

Пояснення

VAR підвищує читабельність:
окремо виносимо виручку, собівартість, операційні витрати;
далі повертаємо кінцевий результат.
