# SQL Data Warehouse Analytics Project

A comprehensive SQL data warehouse solution for sales analytics, customer segmentation, and product performance analysis. Built for research analyst portfolio demonstration.

## 🎯 Project Overview

**Business Problem**: Analyze sales performance, customer behavior patterns, and product profitability to drive data-informed business decisions.

**Solution**: Complete data warehouse with star schema, ETL pipeline, and production-ready BI reports using advanced SQL analytics.

**Key Deliverables**:
- Customer lifecycle analysis (VIP/Regular/New segments)
- Product performance benchmarking
- Time-series sales trends
- Category contribution analysis

## 🏗️ Technical Architecture
DataWarehouseAnalytics (Gold Schema)
├── dim_customers → Customer master data
├── dim_products → Product catalog + cost data
└── fact_sales → Granular sales transactions

text

**Star Schema** | **3 Tables** | **Production Views**

## 🚀 Quick Setup

### Prerequisites
SQL Server 2022+

Local path: C:\SQL2022\sql-data-analytics-project\datasets

text

### One-Command Deployment
```sql
-- Single script execution:
-- 1. Creates database + gold schema
-- 2. Bulk loads 3 CSV datasets  
-- 3. Creates production report views
-- 4. Runs sample analytics queries
```

## 📊 Core Analytics Engine

### Time Intelligence
```sql
-- Monthly trends, cumulative totals, moving averages
SELECT YEAR(order_date), MONTH(order_date), 
       SUM(sales_amount), COUNT(DISTINCT order_number)
FROM gold.fact_sales
GROUP BY YEAR(order_date), MONTH(order_date);
```

### Product Performance
```sql
-- YoY growth, avg benchmarking, performance tiers
WITH yearly_sales AS (...)
SELECT product_name, current_sales, py_sales,
       CASE WHEN current_sales > avg_sales THEN 'Above Avg' END
FROM yearly_product_sales;
```

## 📈 Production BI Reports

### Customer Report View
| KPI | Business Value |
|----|---------------|
| Recency (months) | Customer engagement |
| AOV | Order profitability |
| Monthly Spend | Predictable revenue |
| Segments | Targeted marketing |

**VIP Definition**: ≥12 months + >€5K lifetime value

### Product Report View  
| KPI | Business Value |
|----|---------------|
| ASP vs Cost | Product margins |
| Performance Tier | Inventory decisions |
| Monthly Revenue | Forecasting |

**High Performer**: >€50K total sales

## 💼 Research Analyst Skills
🔹 ADVANCED SQL
└─ Window functions (LAG, AVG OVER)
└─ CTEs for complex logic
└─ Dynamic segmentation

🔹 DATA WAREHOUSING
└─ Star schema design
└─ ETL via BULK INSERT
└─ Production views

🔹 BUSINESS INTELLIGENCE
└─ KPI development (AOV, recency, CLV)
└─ Customer lifecycle
└─ Revenue attribution

text

## 🧪 Sample Insights Generated
🏆 TOP CATEGORY: [Data-driven result]
💰 BEST PERFORMER: [Product name] +[X]% YoY
👥 VIP COUNT: [X] customers (Y% of revenue)
📈 GROWTH TREND: [Monthly pattern]

text

## 📋 Usage

```sql
-- Customer insights (for marketing)
SELECT * FROM gold.report_customer 
ORDER BY total_sales DESC;

-- Product analysis (for supply chain)  
SELECT * FROM gold.report_products
WHERE product_segment = 'High-Performer';

-- Executive summary
SELECT category, total_sales,
       CONCAT(ROUND(percentage,1),'%') AS contrib
FROM category_sales ORDER BY total_sales DESC;
```

## 📁 Repository Structure
├── README.md (You're reading it)
├── setup_complete.sql (Full deployment)
├── datasets/flat-files/ (CSV source data)
├── output/ (Generated reports)
└── docs/ (ERD, data dictionary)

text

## 🎓 Learning Outcomes

1. **Production-grade SQL** for enterprise analytics
2. **Star schema optimization** for BI workloads
3. **KPI framework** for business stakeholders
4. **Segmentation logic** for targeted strategies

## 🔮 Next Steps (Production)
□ Power BI/Tableau dashboards
□ Python forecasting models
□ Customer retention cohorts
□ ABC inventory analysis
□ Marketing campaign ROI

text

## 📄 License
MIT - Free for portfolio use, interviews, and learning.

---

**Research Analyst Portfolio** | **SQL Server 2022** | **April 2026**  
**Ready for Production Deployment**
