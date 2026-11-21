# Power BI Dashboard Build Guide — Apex Finance

1. Open Power BI Desktop → Get Data → Text/CSV → select `Apex_Finance_Sales_Dataset.csv`.
2. Set `Date` to Date and `Amount_INR` to Whole Number/Currency.
3. Create measures:

```DAX
Total Revenue = SUM(Sales[Amount_INR])
Transaction Count = DISTINCTCOUNT(Sales[Transaction_ID])
Successful Transactions = CALCULATE([Transaction Count], Sales[Status] = "Successful")
Success Rate = DIVIDE([Successful Transactions], [Transaction Count], 0)
Average Transaction Value = DIVIDE([Total Revenue], [Transaction Count], 0)
```

4. Add KPI cards for Total Revenue, Transaction Count, Success Rate and Average Transaction Value.
5. Add a line chart: Date (month) on X-axis, Total Revenue on Y-axis.
6. Add bar charts for Revenue by Product and Revenue by Branch.
7. Add a stacked column or donut chart for Status and a bar chart for Payment_Mode.
8. Add slicers for Date, Branch, Product and Payment_Mode.
9. Save as `Apex_Finance_Dashboard.pbix`.

**Data note:** sample data are fictional and for academic demonstration only. Verify relationships and aggregation after import.
