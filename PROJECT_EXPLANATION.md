# Project Explanation

This document provides a detailed explanation of the analytical approach used in the Customer & Revenue Analytics project.

The purpose of this document is to explain the reasoning behind the analysis and the SQL techniques used.

---

# What This Project Does

This project analyzes a transactional retail dataset to understand how revenue is generated and how different factors contribute to business performance.

The analysis focuses on identifying patterns in customer purchases, product demand, geographic markets, and revenue trends.

By answering these questions, the project demonstrates how SQL can be used to extract insights from raw transactional data.

---

# Why This Analysis Matters

Retail businesses generate large amounts of transactional data. Without analysis, this data provides limited value.

Data analysis helps businesses answer important questions such as:

- Which customers generate the most revenue?
- Which products drive sales?
- Which markets perform best?
- When does demand increase or decrease?

Understanding these patterns allows companies to make better decisions about marketing strategies, inventory planning, and customer retention.

---

# Dataset Description

The dataset used in this project is the **Online Retail II dataset**, which contains transaction-level records from an online retailer.

Each row represents an item purchased within a transaction.

Key columns include:

| Column | Description |
|------|-------------|
Invoice | Unique transaction identifier |
StockCode | Product identifier |
Description | Product name |
Quantity | Number of items purchased |
InvoiceDate | Timestamp of the transaction |
Price | Price per unit |
Customer ID | Customer identifier |
Country | Customer location |

Revenue is calculated using the formula:

Revenue = Quantity × Price

---

# How the Analysis Was Performed

The analysis follows a structured workflow used in many data analytics projects.

---

## 1. Data Loading

The dataset is loaded using pandas and converted into a DuckDB table. This allows SQL queries to be executed directly within the notebook.

---

## 2. Data Cleaning

The dataset contains negative quantities that represent returned or cancelled orders.

To accurately measure sales revenue, transactions with negative quantities are excluded from revenue calculations.

---

## 3. Business KPI Summary

Before performing deeper analysis, key business metrics are calculated:

- Total number of orders
- Total number of customers
- Total revenue

These metrics help establish the scale of the dataset and provide context for further analysis.

---

## 4. Revenue by Country

Revenue is aggregated by country to identify the company’s strongest geographic markets.

This helps understand which regions contribute the most to overall business performance.

---

## 5. Customer Revenue Analysis

Customer-level revenue is calculated to identify high-value customers.

This analysis reveals whether revenue is evenly distributed across customers or concentrated among a small group.

---

## 6. Customer Revenue Ranking

Window functions are used to rank customers by their revenue contribution.

This technique is commonly used in business analytics to identify top-performing customers or products.

---

## 7. Product Performance Analysis

Product-level revenue is calculated to determine which products generate the most sales.

This analysis helps businesses identify their most important products.

---

## 8. Revenue Trend Analysis

Revenue is aggregated by month to analyze changes in sales over time.

This helps identify seasonal patterns and periods of increased demand.

---

# Key Findings

The analysis reveals several important insights:

- Revenue is concentrated among a small number of customers.
- The United Kingdom is the dominant revenue market.
- Certain decorative home products drive a large share of sales.
- Revenue increases significantly toward the end of the year.
- Return transactions must be filtered for accurate analysis.

---

# Conclusion

This project demonstrates how SQL can be used to analyze transactional retail data and extract meaningful business insights.

The analytical workflow shown in this project reflects common tasks performed by data analysts working in retail analytics, business intelligence, and product analytics.
