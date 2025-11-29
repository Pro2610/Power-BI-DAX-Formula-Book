# CALCULATE & Context Transition

## 📘 Description
`CALCULATE` modifies the filter context AND converts any existing row context.

## 🧮 Formula
```DAX
Customer Sales :=
CALCULATE (
    SUM ( Sales[Amount] ),
    Customer[Status] = "Active"
)
📝 Explanation
Row context (customer) + new filters (status) together define the final filter context.

🎯 When to Use
• row-level metrics
• dynamic filtering
• conditional aggregations

yaml
Copy code
