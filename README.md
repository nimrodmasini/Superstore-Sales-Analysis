# 📊 Superstore Sales Dashboard
![image](https://github.com/user-attachments/assets/0de88410-52c6-4edd-ac76-66759f5efe2c)

## Project Overview

- **Tool Used**: Microsoft Power BI
- **Dataset**: [Superstore Dataset (Kaggle)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

This dashboard analyzes sales, profit, and order trends for a fictional superstore across different regions, categories, and time periods. The goal is to provide business intelligence to support decision-making.

---

## Data Description

The dataset contains over 9,000 rows of transactional retail data, with fields such as:

- `Order Date`, `Ship Date`, `Region`, `State`, `City`
- `Sales`, `Profit`, `Quantity`, `Discount`
- `Category`, `Sub-Category`, `Product Name`
- `Customer Name`, `Segment`, `Ship Mode`

---

## Data Cleaning & Transformation

Performed using Power BI’s Power Query Editor and DAX:

- Changed column data types (Dates, Currency, Numbers)
- Removed unnecessary columns (`Country`, `Postal Code`)
- Renamed columns for clarity
- Handled missing values and duplicates

### Measures Created

```DAX
Total Sales = SUM(Superstore[Sales])
Total Profit = SUM(Superstore[Profit])
Total Orders = DISTINCTCOUNT(Superstore[Order ID])
Profit Margin = DIVIDE([Total Profit], [Total Sales])
```

## Dashboard Components

| Visual                     | Purpose                                                        |
|---------------------------|----------------------------------------------------------------|
| **KPI Cards**              | Display total sales, total profit, and total orders            |
| **Bar Chart**              | Compare total sales across different regions                   |
| **Pie Chart**              | Visualize sales distribution across product categories         |
| **Line Chart**             | Track monthly sales trends over time                           |
| **Filled Map**             | Show state-level sales distribution with color shading         |
| **Top 10 Products Table**  | Highlight top-selling products based on sales                  |
| **Slicers**                | Enable interactive filtering by Region, Category, and Date     |

---

## Key Insights

- **Regional Performance**: The **West** region leads in total sales, followed by **East** and **Central**.
- **Profitability**: **Technology** category is the most profitable, while **Office Supplies** has lower margins.
- **Product Sales**: A small group of products contributes significantly to overall revenue.
- **Geography**: States like **California**, **New York**, and **Texas** generate the most revenue.
