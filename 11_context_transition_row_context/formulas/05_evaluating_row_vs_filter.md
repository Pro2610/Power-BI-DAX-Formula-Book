# Row vs Filter Evaluation

## 📘 Description
Different results occur when using row context vs filter context.

## 🧮 Formula
```DAX
Max Unit Price (Row Context Demo) :=
MAXX ( Sales, Sales[Unit Price] )

Max Unit Price (Filter Context) :=
MAX ( Sales[Unit Price] )
📝 Explanation
MAXX loops row-by-row, MAX uses filter context directly.

🎯 When to Use
• understanding iterator inefficiencies
• debugging inconsistent results
