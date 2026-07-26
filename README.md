# E-Commerce-Sales-Dashboard
An interactive Power BI dashboard analyzing sales performance and customer behavior using the Olist Brazilian E-Commerce dataset. The dashboard highlights revenue trends, top product categories, geographic sales distribution, payment preferences, and top-performing sellers all summarized with key business insights.

# Overview
This project explores e-commerce order data to answer key business questions:
- How is revenue trending over time?
- Which product categories and states generate the most revenue?
- What payment methods do customers prefer?
- Who are the top-performing sellers on the platform?

# Tools & Technologies
- Power BI Desktop — dashboard design, data modeling, DAX measures
- Power Query — data cleaning and transformation
- DAX (Data Analysis Expressions) — custom measures for accurate KPI calculations

# Dataset
-Source: Brazilian E-Commerce Public Dataset by Olist (Kaggle)
Real, anonymized order data from a Brazilian online marketplace (2016–2018), covering orders, customers, products, sellers, and payments.

# Dashboard Features
KPI Summary Cards

- Total Revenue
- Total Orders (distinct count)
- Total Customers (distinct count)
- Total Products (distinct count)


# Visualizations
- Revenue trend by month (line chart)
- Top product categories by revenue (bar chart, Top N filtered)
- Sales by customer state (bar chart)
- Top sellers by revenue (bar chart)
- Payment type distribution (donut chart)

Key Insights Panel A written summary of key findings, including revenue growth trends, top-performing states, and dominant payment methods.

# Key DAX Measures 
Total Revenue = SUM('Brazilian E-Commerce Public Dataset by Olist'[price])

Total Orders = DISTINCTCOUNT('Brazilian E-Commerce Public Dataset by Olist'[order_id])

Total Customers = DISTINCTCOUNT('Brazilian E-Commerce Public Dataset by Olist'[customer_unique_id])

Total Products = DISTINCTCOUNT('Brazilian E-Commerce Public Dataset by Olist'[product_id])

DISTINCTCOUNT was used instead of simple counts because the source table is denormalized (order line items repeat customer/order details across rows), so raw counts would overstate totals.

# Design
A dark teal and orange color theme was applied consistently across all visuals and KPI cards for a clean, cohesive, presentation-ready look.

# How to View
- Download Dashboard.png
- Open it with Power BI Desktop (free)
- Explore the interactive visuals — click any chart element to cross-filter the rest of the dashboard
