# Context Transition

## 📘 Description
Context transition occurs when `CALCULATE` converts row context into filter context.

## 🧮 Formula
```DAX
SalesAmount :=
SUM ( Sales[Amount] )
Evaluated with:

DAX
Copy code
CALCULATE ( [SalesAmount] )
📝 Explanation
Inside CALCULATE, the current row values (e.g., CustomerID = 15) become actual filters.

🎯 When to Use
• understanding how calculated columns work
• debugging unexpected CALCULATE behaviour
