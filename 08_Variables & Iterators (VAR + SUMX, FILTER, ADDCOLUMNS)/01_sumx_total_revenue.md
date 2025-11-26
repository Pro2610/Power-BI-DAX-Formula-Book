# SUMX — Total Revenue via Iteration

## Формула
```DAX
Total Revenue SUMX :=
SUMX (
    Sales,
    Sales[Quantity] * Sales[Price]
)

Пояснення

SUMX проходить по кожному рядку таблиці Sales і рахує Quantity × Price.
Потім підсумовує всі значення.
Це аналог row-by-row обчислення → часто зручніше, ніж SUM(Sales[Revenue]).
