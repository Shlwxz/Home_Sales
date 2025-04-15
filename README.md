# 🏡 Home Sales Analysis with SparkSQL

---

## 📌 Overview

This project leverages Apache Spark and SparkSQL to analyze a dataset of home sales stored in a cloud-based CSV. The goal is to derive meaningful real estate metrics, such as average prices by feature and year, and to measure performance improvements using caching and partitioning techniques.

---

## 🧪 Key Objectives

- Load housing sales data into a Spark DataFrame
- Create and interact with temporary SQL views
- Use SparkSQL to compute key metrics like average price by year, room count, or square footage
- Optimize Spark query performance using caching and partitioning
- Compare performance before and after optimization

---

## 🔍 SQL Queries Completed

- ✅ **Average price of 4-bedroom homes by year**
- ✅ **Average price of 3 bed / 3 bath homes by build year**
- ✅ **Average price of 3 bed / 3 bath / 2 floor homes ≥ 2,000 sqft**
- ✅ **Average home price per "view" rating (≥ $350K)**

Each query result was rounded to **two decimal places** for clarity and professionalism.

---

## 🚀 Performance Optimization

### Caching
- The `home_sales` temp view was cached using Spark SQL
- Query runtime was measured **before and after caching**

### Partitioning
- Dataset was partitioned by `date_built`
- Saved as **Parquet format**
- Partitioned Parquet file used to create a second temp view
- Query runtime on partitioned data was also measured

### Uncaching
- The `home_sales` table was uncached
- Verification step confirmed that the cache was removed

---

## 📁 Repository Contents

```
Home_Sales/
├── Home_Sales_Custom.ipynb         # Your personalized SparkSQL analysis
├── Resources/
│   └── home_sales_revised.csv      # Cloud-based housing dataset (AWS)
└── README.md                       # Project summary and findings
```

---

## 📈 Summary

This notebook demonstrates how PySpark SQL can be used for real estate analytics, and how tools like `cacheTable()` and data partitioning can significantly reduce query runtime. The project mimics real-world big data scenarios by optimizing distributed queries and managing memory efficiently.
