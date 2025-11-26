Margin Table :=
ADDCOLUMNS (
    Sales,
    "Revenue", Sales[Quantity] * Sales[Price],
    "COGS_Total", Sales[Quantity] * Sales[COGS],
    "Margin", ( Sales[Quantity] * Sales[Price] ) - ( Sales[Quantity] * Sales[COGS] )
)
