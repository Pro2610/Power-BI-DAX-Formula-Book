# Row Context Basics

## 📘 Description
Row context exists when a formula is evaluated row-by-row (e.g., calculated columns, iterators).

## 🧮 Formula
```DAX
Line Total :=
Sales[Quantity] * Sales[Unit Price]
📝 Explanation
Each row has access only to its own fields — no aggregation.

🎯 When to Use
• calculated columns
• iterating over a table
