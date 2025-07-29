# Maven Analytics Toy Store Challenge 🧸

A complete case study on sales, inventory, and profit analysis for a fictional toy store chain in Mexico using **SQL** and **Power BI**.

---

## 📊 Project Overview

**Business Context:**
Maven Toys is a fictional chain of toy stores across Mexico. The company has provided data on products, stores, daily sales, and inventory levels. The dataset includes:

- Over **820,000** transactions from **Jan 2017 to Sep 2018**
- 35 products, 50 stores, and current inventory as of Oct 2018

**Objective:**
To prepare, analyze, and visualize the dataset to:
- Identify best-selling and least-performing products
- Understand seasonality in sales
- Optimize inventory allocation
- Support decisions on store performance and expansion

**Major Business Questions:**
1. Which product categories generate the highest profit, and is it consistent across store types?
2. Are there seasonal patterns in sales performance?
3. Are stockouts affecting sales at specific stores?
4. What is the value and longevity of the current inventory?

---

## 📊 Dataset Overview

- **Products** (35 rows)
- **Stores** (50 rows)
- **Sales** (~820K rows)
- **Inventory** (~1,500 rows)

> **Source:** [Kaggle – Maven Toys Sales Dataset](https://www.kaggle.com/)

---

## 📃 Database Schema

SQL-based relational schema:

- **Fact Table:** `sales`
- **Dimension Tables:** `products`, `stores`, `inventory`

SQL code for schema creation and data import provided in:
- [`Database Schema Creation.sql`](./Database%20Schema%20Creation.sql)
- [`Data Preparation.sql`](./Data%20Preparation.sql)

---

## 🔢 Data Preparation

Performed the following operations in MySQL:

- Loaded and verified CSV data
- Cleaned `product_cost` and `product_price` columns using string parsing and conversion
- Enforced primary and foreign key constraints
- Created temporary tables, views, stored procedures for advanced querying

See full pipeline in [`SQL Data Analysis.sql`](./SQL%20Data%20Analysis.sql)

---

## 🔍 Analysis Techniques

- **Views & Joins** to compare product performance across stores
- **Stored Procedures** to simulate store-by-store analysis loops
- **CTEs & Window Functions** for running totals and best-sellers
- **Temporary Tables** to modularize analysis for reporting

Key SQL deliverables:
- Products not sold at some stores
- Profit and sales per store and city
- Monthly/rolling revenue trends
- Top 3 products per store
- Inventory valuation and depletion forecasts

---

## 🌈 Power BI Dashboards

Two major dashboards were created to visualize:

### 1. Sales & Profit Dashboard
- Sales vs Profit by Product and Category
- Store-level breakdown
- Filters: City, Date, Category, Location

### 2. Inventory & Units Sold Dashboard
- Units sold by product and category
- Inventory on hand and turnover insights
- Cumulative sales by month and weekday

Screenshots from dashboards included in [`Maven Toys Dashboards.pdf`](./Maven%20Toys%20Dashboards.pdf)

![Dashboard Preview](./maven%20dashboard.png)

---

## 📈 Key Findings & Recommendations

### 1. **Top Profit-Driving Categories**
- **Toys** and **Electronics** account for 50%+ of profit
- `Colorbuds` and `Action Figures` are the highest performing products

### 2. **Seasonality Trends**
- Sales spike significantly in **December** (Christmas period)
- **March and April** also show higher activity

### 3. **Inventory Gaps**
- 40% of stores did not offer all products
- Some low-selling items (e.g., Monopoly, Dominoes) were often missing, likely no major impact

### 4. **Stock Valuation & Risk**
- $410K in potential revenue from existing inventory
- Current stock (~29.7K units) won’t meet upcoming high season demand based on sales velocity

### Recommendation Summary:
- Restock top 10 products before year-end
- Phase out low-selling SKUs
- Expand in cities where sales > $1M
- Monitor monthly inventory-to-sales ratio

---

## 🔍 Files & Artifacts

| File                              | Purpose                          |
|-----------------------------------|----------------------------------|
| `Database Schema Creation.sql`    | Base schema + constraints        |
| `Data Preparation.sql`            | Cleaning + transformation        |
| `SQL Data Analysis.sql`           | All queries + analysis views     |
| `Maven Toys Dashboards.pdf`       | Power BI dashboard snapshots     |
| `maven dashboard.png`             | PNG preview for GitHub/README    |

---

Feel free to fork or reference this project if you’re interested in retail analytics, BI visualization, or SQL reporting!
