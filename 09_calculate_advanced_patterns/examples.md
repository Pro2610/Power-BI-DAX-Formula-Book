## 1. Sales LY but ignoring Product filter
Sales LY (Ignore Product) =
CALCULATE (
    [Total Sales],
    SAMEPERIODLASTYEAR ( Dates[Date] ),
    REMOVEFILTERS ( Products )
)

## 2. Customers who purchased in current month only
DAX
Copy code
Customers CM Only =
CALCULATE (
    DISTINCTCOUNT ( Sales[CustomerID] ),
    FILTER (
        Customers,
        Customers[FirstPurchaseMonth] = SELECTEDVALUE ( Dates[Month] )
    )
)

## 3. Conversion from Viewer → Buyer
DAX
Copy code
Viewer to Buyer % =
DIVIDE (
    CALCULATE ( DISTINCTCOUNT ( Users[UserID] ), Users[Role] = "Buyer" ),
    CALCULATE ( DISTINCTCOUNT ( Users[UserID] ), Users[Role] = "Viewer" )
)

## 4. Sales for the last 14 days (dynamic)
DAX
Copy code
Sales Last 14 Days =
CALCULATE (
    [Total Sales],
    Dates[Date] >= MAX ( Dates[Date] ) - 14
)

## 5. New vs Returning Customers Split
DAX
Copy code
Returning Customers Sales =
CALCULATE (
    [Total Sales],
    Customers[IsReturning] = TRUE()
)

## 6. Sales ignoring slicers except Date
DAX
Copy code
Sales Only Date =
CALCULATE (
    [Total Sales],
    ALL ( Products ),
    ALL ( Customers )
)

## 7. Sales for selected category but ignoring subcategory
DAX
Copy code
Sales Category Only =
CALCULATE (
    [Total Sales],
    ALLEXCEPT ( Products, Products[Category] )
)

## 8. Top 10% customers by revenue
DAX
Copy code
Top 10% Customers Sales =
CALCULATE (
    [Total Sales],
    FILTER (
        Customers,
        Customers[RevenueRankPercent] <= 0.10
    )
)

## 9. Sales for weekends only
DAX
Copy code
Weekend Sales =
CALCULATE (
    [Total Sales],
    FILTER ( Dates, Dates[IsWeekend] = TRUE() )
)

## 10. Selected Month vs Previous Month Sales
DAX
Copy code
Sales MoM =
[Total Sales]
    - CALCULATE ( [Total Sales], DATEADD ( Dates[Date], -1, MONTH ) )
