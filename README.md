# 🚀 FMCG Data Pipeline using Medallion Architecture (Databricks)

## 📌 Overview
This project implements an end-to-end data pipeline using the Medallion Architecture (Bronze → Silver → Gold) on Databricks.

It processes FMCG datasets (customers, products, pricing, sales) and transforms raw data into analytics-ready tables using Delta Lake.

## 🏗️ Architecture
Flow: Data Sources → Bronze → Silver → Gold → Analytics  
Orchestration: Customer → Product → Pricing → Fact

## 🔹 Data Sources
- customers.csv
- products.csv
- pricing.csv
- sales.csv

## 🥉 Bronze Layer (Raw Data)
- Stores raw data in Delta format
- 1:1 ingestion from source
- Preserves historical data
- Designed for traceability and reprocessing

## 🥈 Silver Layer (Cleaned Data)
- Cleans and standardizes data
- Removes duplicates
- Performs joins across datasets
- Prepares consistent datasets for downstream use

## 🥇 Gold Layer (Business Layer)
- Builds analytics-ready data model

Tables:
- fact_sales
- dim_customer
- dim_product
- dim_date

- Implements star schema for analytics

## ⚡ Incremental Processing
- Implemented using Delta Lake MERGE
- Handles updates without full reloads
- Improves performance and scalability

## ⚙️ Orchestration
- Built using Databricks Workflows
- Dependency-based execution

Pipeline Flow: Customer → Product → Pricing → Fact

- Ensures reliable and automated pipeline runs

## 🛠️ Tech Stack
- Databricks
- PySpark
- Delta Lake
- SQL

## 📊 Outcome
- Built a complete data pipeline from raw data to analytics
- Reduced manual data processing
- Created reusable and scalable workflows
- Delivered analytics-ready datasets

## 🔮 Future Improvements
- Data quality validation (Great Expectations)
- Delta optimization (OPTIMIZE, ZORDER)
- Monitoring and alerting
- Streaming ingestion

## ⭐ Key Takeaway
This project demonstrates how to design and build a scalable, production-style data pipeline using modern data engineering practices.
