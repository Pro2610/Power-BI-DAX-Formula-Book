# 04 — Iterator Functions (X-Functions)

Ітератори — це DAX-функції, які проходяться по рядках таблиці, обчислюють вираз для кожного рядка, а потім агрегують результат (сума, середнє, мін/макс тощо).

Цей блок збирає основні X-функції:

- `SUMX`
- `AVERAGEX`
- `MINX`
- `MAXX`
- `COUNTX`
- `RANKX`
- Патерн: `SUMX + FILTER`
- Патерн: `ADDCOLUMNS + X-функції` для розрахунків "на льоту"

> У прикладах використовується умовна таблиця **Sales**  
> з колонками: `Sales[Date]`, `Sales[CustomerID]`, `Sales[Product]`, `Sales[Quantity]`, `Sales[Price]`, `Sales[Revenue]`.

