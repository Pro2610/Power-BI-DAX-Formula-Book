# 11 — Context Transition & Row Context

Цей модуль пояснює одну з найважливіших концепцій у DAX —  
**transition між row context → filter context**, який запускається функціями:
- `CALCULATE`
- `CALCULATETABLE`
- `SUMX` / `FILTER` / iterators

Також розбираємо приклади, де row context створюється неявно (iterators) і як він впливає на формули.

---

## 📌 Зміст
1. Row Context Basics  
2. Context Transition (як працює CALCULATE)  
3. Row Context inside Iterators (SUMX, FILTER)  
4. Common Pitfalls (часті помилки)
