# CALCULATE — найважливіша функція DAX

## 1️⃣ Sales for Current Year
```DAX
Sales CY :=
CALCULATE (
    [Total Sales],
    YEAR ( 'Date'[Date] ) = YEAR ( TODAY() )
