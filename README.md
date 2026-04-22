# Analyst-sql-portforlio-project
SQL Server Data Warehouse Analytics project using T-SQL. Built star-schema tables, loaded CSV data with BULK INSERT, performed sales/customer/product analysis using CTEs and window functions, and created customer &amp; product report views with KPIs for business insights.


# 📊 Data Warehouse Analytics SQL Project

A complete **SQL Server Data Warehouse Analytics Project** built using **T-SQL**. This project transforms raw CSV datasets into a structured analytical warehouse and generates valuable business insights through SQL reporting.

It showcases practical **Data Analyst / SQL Developer / BI Developer** skills including data modeling, ETL, reporting, segmentation, and KPI analysis.

---

## 🚀 Project Overview

This project creates a database named:

```sql
DataWarehouseAnalytics

Inside the database, a schema named gold is created to store analytics-ready tables.

📁 Tables Created
Dimension Tables
gold.dim_customers
gold.dim_products
Fact Table
gold.fact_sales
🛠️ Tools & Technologies
Microsoft SQL Server
SQL Server Management Studio (SSMS)
T-SQL
CSV Flat Files
Data Warehousing Concepts
📂 Data Model
👤 Customers Table

Contains customer information:

Customer ID
Customer Number
Full Name
Country
Gender
Marital Status
Birthdate
Create Date
📦 Products Table

Contains product details:

Product ID
Product Name
Category
Subcategory
Product Line
Cost
Start Date
💰 Sales Table

Contains transaction records:

Order Number
Customer Key
Product Key
Order Date
Shipping Date
Due Date
Quantity
Price
Sales Amount
⚙️ ETL Process

Source CSV files are imported into SQL Server using:

BULK INSERT
📁 Files Loaded
dim_customers.csv
dim_products.csv
fact_sales.csv
📈 Business Analysis Performed
1️⃣ Time Series Analysis
Monthly sales trends
Yearly sales summary
Order volume trends
Quantity sold over time
2️⃣ Running Total & Moving Analysis

Using window functions:

Running total sales
Moving average price
3️⃣ Product Performance Analysis

Compared yearly product sales against:

Average product sales
Previous year sales
Growth / decline trends
4️⃣ Category Sales Contribution

Identify categories contributing the most revenue.

5️⃣ Product Cost Segmentation

Products grouped into:

Below 100
100 – 500
501 – 1000
Above 1000
6️⃣ Customer Segmentation

Customers classified into:

VIP
Regular
New

Based on purchase history and total spending.

📋 Reports Created
👤 Customer Report View
gold.report_customer

Includes:

Customer Name
Age
Age Group
Customer Segment
Last Order Date
Recency
Total Orders
Total Sales
Total Quantity Purchased
Total Products Bought
Lifespan
Average Order Value
Average Monthly Spend
📦 Product Report View
gold.report_products

Includes:

Product Name
Category
Subcategory
Product Segment
Last Sale Date
Recency
Total Orders
Total Sales
Total Quantity Sold
Total Customers
Lifespan
Average Selling Price
Average Order Revenue
Average Monthly Revenue
💡 SQL Concepts Used
Common Table Expressions (CTE)
CASE Statements
Aggregations
GROUP BY
JOINS
Window Functions
LAG()
SUM() OVER()
AVG() OVER()
DATEDIFF()
DATETRUNC()
Views
BULK INSERT
🎯 Business Value

This project helps businesses:

Understand top-selling products
Identify loyal/VIP customers
Track revenue trends
Improve pricing strategy
Optimize product portfolio
Support dashboard creation in Power BI / Tableau
▶️ How to Run This Project
Step 1: Open SQL Server Management Studio

Connect to your SQL Server instance.

Step 2: Run SQL Script

Execute the provided .sql file in sequence.

Step 3: View Reports
SELECT * FROM gold.report_customer;
SELECT * FROM gold.report_products;
📸 Recommended Screenshots for GitHub

Add screenshots of:

Database Tables
SQL Queries
Query Results
Report Outputs
SSMS Interface
👨‍💻 Author

Muhammed Mahir K
Aspiring Data Analyst | SQL Developer | Power BI Enthusiast

🔗 LinkedIn: https://www.linkedin.com/in/mhdmahir-k/

🔗 GitHub: https://github.com/mahirkambran

⭐ Support

If you found this project useful, please give it a star ⭐ on GitHub.
