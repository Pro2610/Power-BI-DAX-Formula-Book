Balance BoM :=
CALCULATE(
    FIRSTDATE(DimDate[Date]),
    STARTOFMONTH(DimDate[Date])
)
