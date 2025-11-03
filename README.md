# 🛍️ Supermarket Sales Dashboard (Excel + DAX)

An interactive **Excel dashboard** built for analyzing supermarket sales performance across different years, months, and sales types.  
This project combines **Power Pivot**, **DAX formulas**, and **Excel interactivity** (including tick-box controls) to present a dynamic and insightful view of sales trends and profitability.

---

## 📊 Dashboard Overview

![Supermarket Sales Dashboard](https://raw.githubusercontent.com/<your-username>/<your-repo-name>/main/images/supermarket_sales_dashboard.png)

> *(Replace the above link with your actual GitHub image URL after uploading your screenshot.)*

---

## ✅ Key Highlights

- 💵 **Total Sales & Profit Cards** — Displays real-time total sales, total profit, and profit percentage  
- 🧮 **Dynamic DAX Measures** — Used for calculating total sales, total profit, and profit %  
- 📅 **Monthly & Daily Sales Analysis** — Visualize sales trends using bar and line charts  
- 🛒 **Sales by Product & Category** — Analyze best-performing products and categories  
- 🔘 **Tick-Box Monthly Filter** — Enables users to filter monthly data dynamically  
- 💳 **Payment & Sales Type Insights** — Compare sales distribution by payment method and sales channel  
- 🏆 **Top Product & Top Category Cards** — Highlights the most profitable items and categories  

---

## 🎯 Business Purpose

This dashboard empowers retail and supermarket managers to:

- Track daily and monthly performance  
- Compare direct, online, and wholesale sales  
- Evaluate category-level contribution to total sales  
- Monitor profitability and identify improvement areas  
- Support strategic decision-making using real-time insights  

---

## 🧰 Tools & Techniques Used

| Tool / Feature | Purpose |
|----------------|----------|
| **Microsoft Excel** | Dashboard creation & interactivity |
| **Power Pivot** | Data modeling & relationships |
| **DAX (Data Analysis Expressions)** | KPI calculations |
| **Pivot Tables & Charts** | Sales and profit analysis |
| **Tick Boxes (Form Controls)** | Dynamic monthly sales check |
| **Conditional Formatting** | Visual emphasis on key metrics |

---

## 🧮 Example DAX Measures Used

```DAX
Total Sales = SUM(Sales[SalesAmount])

Total Profit = SUM(Sales[Profit])

Profit % = DIVIDE([Total Profit], [Total Sales], 0) * 100

Monthly Sales =
IF(
    SELECTEDVALUE(Month[IsChecked]) = TRUE(),
    CALCULATE([Total Sales], VALUES(Month[MonthName])),
    BLANK()
)
