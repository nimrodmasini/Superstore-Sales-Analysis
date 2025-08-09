# 📊 Superstore Sales Dashboard

This dashboard analyzes sales, profit, and order trends for a fictional superstore across different regions, categories, and time periods.

![image](https://github.com/user-attachments/assets/0de88410-52c6-4edd-ac76-66759f5efe2c)

## Project Description

**Purpose:**

The SuperStore Sales Analysis Dashboard was created to help business managers quickly understand sales performance, profit trends, and customer purchasing behavior. By analyzing key metrics such as sales by category, region, and time, the dashboard provides actionable insights for optimizing product offerings, improving profit margins and identifying underperforming areas

**Technologies Used:**
- Power BI
- PowerQuery

---

## Data and Processing

**Data Source:**

The dataset was sourced from [Kaggle’s SuperStore Sales Dataset](https://www.kaggle.com/datasets). 

It contains detailed order, product, and customer information, including:
- **Order details**: Order ID, Order Date, Ship Date, Ship Mode
- **Product details**: Category, Sub-Category, Product Name
- **Customer details**: Customer Name, Segment, Region
- **Sales metrics**: Sales, Quantity, Discount, Profit

The data covers a 4-year period.

**Data Cleaning:**
- Changed column data types (Dates, Currency, Numbers)
- Removed unnecessary columns (`Country`, `Postal Code`)
- Renamed columns for clarity
- Handled missing values and duplicates

**Measures Created:**
```DAX
Total Sales = SUM(Superstore[Sales])
Total Profit = SUM(Superstore[Profit])
Total Orders = DISTINCTCOUNT(Superstore[Order ID])
Profit Margin = DIVIDE([Total Profit], [Total Sales])
```

--- 

## Dashboard Features

- KPI Cards - Display total sales, total profit, and total orders
- Bar Chart - Compare total sales across different regions
- Pie Chart - Visualize sales distribution across product categories
- Line Chart - Track monthly sales trends over time
- Filled Map - Show state-level sales distribution with color shading
- Top 10 Products Table - Highlight top-selling products based on sales
- Slicers - Enable interactive filtering by Region, Category, and Date

---

## Key Insights

- **Regional Performance**: The **West** region leads in total sales, followed by **East** and **Central**.
- **Profitability**: **Technology** category is the most profitable, while **Office Supplies** has lower margins.
- **Product Sales**: A small group of products contributes significantly to overall revenue.
- **Geography**: States like **California**, **New York**, and **Texas** generate the most revenue.

---

## Recommendations
- **Focus on High-Performing Regions** - Continue investing in the **West** region while exploring strategies to boost performance in the **Central** and **South** regions.
- **Leverage Technology Category** - Expand offerings and marketing for the **Technology** category, given its strong profitability.
- **Optimize Office Supplies** - Review pricing and discount strategies for **Office Supplies** to improve margins.
- **Capitalize on Top Products** - Maintain stock and marketing focus on the small group of products driving the majority of revenue.
- **Strengthen Key States** – Deepen customer relationships and targeted promotions in **California**, **New York**, and **Texas** to further grow revenue.

