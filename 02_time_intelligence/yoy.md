Total Sales YoY % :=
VAR PrevYear =
    CALCULATE ( [Total Sales], SAMEPERIODLASTYEAR ( 'Date'[Date] ) )
RETURN
DIVIDE ( [Total Sales] - PrevYear, PrevYear )
