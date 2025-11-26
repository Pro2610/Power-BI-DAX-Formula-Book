AOV :=
VAR OrdersTable =
    SUMMARIZE (
        Sales,
        Sales[OrderID],
        "OrderRevenue", SUMX ( CURRENTGROUP(), Sales[Quantity] * Sales[Price] )
    )
RETURN
AVERAGEX ( OrdersTable, [OrderRevenue] )

Пояснення
Групуємо дані по OrderID.
Для кожного замовлення рахуємо дохід через SUMX.
Потім використовуємо AVERAGEX, щоб знайти середній дохід на замовлення.
