Margin Table :=
ADDCOLUMNS (
    Sales,
    "Revenue", Sales[Quantity] * Sales[Price],
    "COGS_Total", Sales[Quantity] * Sales[COGS],
    "Margin", ( Sales[Quantity] * Sales[Price] ) - ( Sales[Quantity] * Sales[COGS] )
)

Пояснення

ADDCOLUMNS створює обчислювані колонки без необхідності додавати їх у модель.
Це корисно для складних таблиць, дебагу та тимчасових розрахунків.
