## 🟦 1. Повноцінна Date Table (рекомендована)
```DAX
Date =
VAR StartDate = DATE(2018,1,1)
VAR EndDate   = TODAY()
RETURN
ADDCOLUMNS (
    CALENDAR ( StartDate, EndDate ),
    "Year", YEAR ( [Date] ),
    "Month", MONTH ( [Date] ),
    "Month Name", FORMAT ( [Date], "MMMM" ),
    "Month Short", FORMAT ( [Date], "MMM" ),
    "Year-Month", FORMAT ( [Date], "YYYY-MM" ),
    "Quarter", "Q" & FORMAT ( [Date], "Q" ),
    "Week", WEEKNUM ( [Date], 2 ),
    "Day", DAY ( [Date] ),
    "Day Name", FORMAT ( [Date], "dddd" ),
    "Day Short", FORMAT ( [Date], "ddd" ),
    "Is Weekend", IF ( WEEKDAY([Date],2) > 5, 1, 0 )
)

2. Коротка Date Table (мінімальна)
Date =
CALENDAR ( DATE(2020,1,1), TODAY() )

3. Financial Calendar (FY, FQ)

приклад — фінансовий рік починається у липні

"Fiscal Year",
    IF ( MONTH([Date]) >= 7, YEAR([Date]) + 1, YEAR([Date]) ),

"Fiscal Quarter",
    "FQ" &
    ROUNDUP( MOD( MONTH([Date]) - 7, 12 ) / 3 + 1, 0 )

4. Початок періодів (useful for measures)
"Start of Month", STARTOFMONTH('Date'[Date]),
"Start of Quarter", STARTOFQUARTER('Date'[Date]),
"Start of Year", STARTOFYEAR('Date'[Date])

5. Маркування Date Table

У Power BI:
Model View → Table → Mark as date table → Select column [Date]
В DAX не пишеться, але знати потрібно.

6. Функції Time Intelligence, які вимагають Date Table
Sales LY =
CALCULATE ( [Total Sales], SAMEPERIODLASTYEAR('Date'[Date]) )

Sales MTD =
CALCULATE ( [Total Sales], DATESMTD('Date'[Date]) )

Sales YTD =
CALCULATE ( [Total Sales], DATESYTD('Date'[Date]) )

7. Сортування: Month Name → Month Number

(В Power BI, не DAX)

Sort column → Month Name → By → Month

8. Динамічні діапазони дат
Last 30 Days =
DATESINPERIOD ( 'Date'[Date], TODAY(), -30, DAY )

9. Дні з початку року
Day of Year = 
FORMAT ( [Date], "DDD" )

10. Прапорець "Сьогодні"
Is Today =
IF ( 'Date'[Date] = TODAY(), 1, 0 )

Best Practices для Date Table

Завжди створюй власну Date Table → не використовуйте Auto Date/Time

Тримай повний діапазон дат (мінімум −3 роки назад)

Познач таблицю як Date Table

Усі зв’язки → many-to-one, single direction до Date Table

Блокуй використання NOW() всередині Date Table (performance)
