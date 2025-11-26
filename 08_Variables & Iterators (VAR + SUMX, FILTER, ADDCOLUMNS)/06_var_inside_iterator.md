Dynamic Discount Revenue :=
SUMX (
    Sales,
    VAR Base = Sales[Quantity] * Sales[Price]
    VAR Discount =
        SWITCH (
            TRUE(),
            Sales[Quantity] >= 10, 0.10,
            Sales[Quantity] >= 5,  0.05,
            0
        )
    RETURN Base * (1 - Discount)
)

Пояснення

Використання VAR всередині SUMX дозволяє:
розрахувати “Base Revenue” із кількості × ціни;
застосувати динамічну знижку;
повернути результат у тому ж ітераторі.
