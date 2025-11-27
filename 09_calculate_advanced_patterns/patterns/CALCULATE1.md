з фільтром таблиці
Sales in US =
CALCULATE (
    SUM ( Sales[Amount] ),
    FILTER ( Customers, Customers[Country] = "USA" )
)
