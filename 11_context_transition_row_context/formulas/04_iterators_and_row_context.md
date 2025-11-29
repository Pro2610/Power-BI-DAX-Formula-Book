# Iterators and Row Context

## 📘 Description
Iterators (`SUMX`, `AVERAGEX`, `FILTER`) create row context.

## 🧮 Formula
```DAX
Total Line Amount :=
SUMX (
    Sales,
    Sales[Quantity] * Sales[Unit Price]
)
📝 Explanation
SUMX evaluates the expression for each row → creates row context.

🎯 When to Use
• when column-level aggregations are not enough
• weighted averages, conditional logic
