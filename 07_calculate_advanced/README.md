# 07 — CALCULATE Advanced Patterns

У цьому блоці зібрані типові та просунуті патерни використання CALCULATE у DAX.
Вони покривають теми:
- зміна контексту фільтра
- заміна фільтрів (override)
- комбінування логіки AND / OR
- очищення контексту (REMOVEFILTERS, ALL)
- умовні CALCULATE-конструкції
- “What-if” патерни

Формули згруповано так:

1. Replace Filter Context  
2. Add Filter Context  
3. Remove Filter Context  
4. Conditional CALCULATE  
5. Combine Filters (AND / OR)  
6. Semi-Additive Patterns (EoM / BoM)

Використовується стандартна модель:
- таблиця **Sales** (Date, Amount)
- таблиця дат **DimDate**
- таблиця продуктів **Products**
