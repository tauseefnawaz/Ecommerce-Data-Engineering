# Olist Data Engineering Project

## Problem Statement

1. **Olist** is a Brazilian e-commerce marketplace connecting sellers and buyers across the country.
2. This project develops an end-to-end data engineering pipeline for Olist to analyze order, customer, and product data, and to enrich product categories for deeper business insights.
3. The solution enables Olist to better understand customer behavior, delivery performance, and product trends, supporting data-driven decision-making.

---

## Technologies Used

1. **Azure Data Factory:** Data orchestration and pipeline automation
2. **Azure Data Lake Storage:** Raw, cleaned, and curated data storage
3. **Databricks (PySpark):** Data processing and transformation (Bronze/Silver/Gold)
4. **MongoDB:** Product category enrichment
5. **GitHub:** Version control

---

## High-Level Details

1. **Source Systems:** CSV files from Kaggle (Olist dataset), product category translations from MongoDB.
2. **Architecture:** 3-layered medallion architecture (Bronze/Silver/Gold).
3. **Data Cleaning:** Handles missing values, duplicates, and inconsistent formats.
4. **Transformations:** Joins multiple datasets, calculates delivery delays, and enriches product categories.
5. **Gold Layer:** Final curated data stored as Parquet/Delta tables, ready for analytics.
6. **Consumption:** Gold layer data can be accessed by BI tools for visualization and reporting.

---

## Additional Information

1. All raw data is ingested into the Bronze layer in ADLS.
2. Data is cleaned and transformed in Databricks, then stored in the Silver layer.
3. Product category translations are fetched from MongoDB and joined for enrichment.
4. The Gold layer contains customer-centric views, such as customer details with delivery delay metrics.
5. Best practices in data engineering and lakehouse design are followed throughout.

---

## Dataset Information

- **Source:** [Olist Store - Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Description:**  
  The dataset contains information on orders, customers, order items, payments, reviews, products, sellers, and geolocations.

---
## Data ingestion flow

![Ingestion Diagram](https://github.com/babitaratudi/BigDataProject/blob/main/Data%20Ingestion%20flow.png)

---

## Architecture Diagram

![Architecture Diagram](https://github.com/babitaratudi/BigDataProject/blob/main/Architecture%20Diagram.png)

---

## Project Flow Summary

- **Ingestion:** Raw data to ADLS Bronze.
- **Transformation:** Cleaning, joining, and enrichment in Databricks.
- **Enrichment:** Product categories from MongoDB.
- **Silver Layer:** Cleaned, enriched data.
- **Gold Layer:** Curated, analytics-ready data.
- **Consumption:** BI tools for reporting and insights.

---

**Best practices in data engineering and lakehouse architecture have been followed throughout the project.**
