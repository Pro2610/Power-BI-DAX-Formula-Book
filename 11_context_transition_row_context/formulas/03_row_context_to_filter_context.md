# Row Context → Filter Context

## 📘 Description
Row context alone does NOT filter other tables, unless converted via `CALCULATE`.

## 🧮 Formula
```DAX
Customer Total :=
CALCULATE (
    SUM ( Sales[Amount] )
)
📝 Explanation
The row context from Customer[CustomerID] becomes a filter on Sales[CustomerID].

🎯 When to Use
• calculations per entity (customer, product, region)
• debugging wrong totals
