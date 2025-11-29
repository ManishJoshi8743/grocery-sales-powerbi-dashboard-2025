# Grocery Sales Analytics Dashboard (Power BI)

This project analyzes grocery store sales using a one-page Power BI dashboard. It highlights revenue, discounts, store performance, top products, and profit leakage.

## Dashboard Preview
(Thumbnail image inside /images folder)
![Dashboard](images/dashboard_preview.png)

## Project Structure
- data/cleaned_grocery_data.csv  
- pbix/Grocery_Sales_Dashboard.pbix  
- images/dashboard_preview.png  
- README.md  

## Key Features
- Store-wise revenue comparison  
- Aisle-wise discount analysis  
- Top-selling products  
- Profit leakage (discount-related loss)  
- Loyalty point insights  
- Month-wise performance  

## Power BI DAX (Measures)
```dax
Total Revenue = SUM(sales[final_amount])
Gross Sales = SUM(sales[total_amount])
Total Discount = SUM(sales[discount_amount])
Profit Leakage M = SUM(sales[total_amount]) - SUM(sales[final_amount])
Total Qty = SUM(sales[quantity])
Total Loyalty Points = SUM(sales[loyalty_points])
```

## Calculated Columns
```dax
Discount % = DIVIDE(sales[discount_amount], sales[total_amount], 0) * 100
Profit Leakage = sales[total_amount] - sales[final_amount]
Revenue Per Unit = DIVIDE(sales[final_amount], sales[quantity], 0)
Month = MONTH(sales[transaction_date])
Month Name = FORMAT(sales[transaction_date], "MMMM")
```

## Tools Used
- Power BI  
- Python (Pandas)  
- Excel/CSV  
- GitHub  

## About Me
I’m **Manish Joshi**, a Data Analyst skilled in Power BI, SQL, Python, and EDA.  
This project showcases my ability to clean data, build KPIs, design dashboards, and generate business insights.

