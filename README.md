# 🍔 Swiggy Sales Analysis | SQL Data Analytics Project

## 📌 Project Overview

The **Swiggy Sales Analysis** project focuses on analyzing restaurant listings, food categories, menu pricing, customer ratings, and location-wise patterns across India using SQL Server.

The project uses SQL queries to clean and validate data, organize information through dimensional modelling, calculate key performance indicators (KPIs), and identify meaningful business insights.

## 🎯 Business Problem

Swiggy has restaurant and food-related data across multiple cities in India. Understanding restaurant distribution, menu pricing, customer ratings, and food-category trends can help identify patterns in the restaurant and food delivery landscape.

This project explores the dataset to generate insights that can support better business understanding and decision-making.

## 🎯 Project Objectives

- Analyze restaurant distribution across cities and states.
- Identify the most frequently represented restaurants.
- Understand food category and dish distribution.
- Analyze menu pricing and price ranges.
- Evaluate customer ratings and rating patterns.
- Explore monthly, quarterly, and yearly trends.
- Generate meaningful insights using SQL queries.

## 📊 Dataset Information

| Description | Details |
|---|---|
| Dataset Name | Swiggy_Data.csv |
| Total Records | 197,430 |
| Total Columns | 10 |
| Unique Restaurants | 993 |
| Cities | 28 |
| States | 28 |
| Distinct Category Labels | 4,972 |
| Dataset Period | January 2025 – August 2025 |

### Dataset Columns

| Column Name | Description |
|---|---|
| State | State name |
| City | City name |
| Order_Date | Date field |
| Restaurant_Name | Restaurant name |
| Location | Local area |
| Category | Food category |
| Dish_Name | Food item name |
| Price_INR | Menu price in rupees |
| Rating | Customer rating |
| Rating_Count | Number of ratings |

## 🛠️ Tools & Technologies

- **SQL Server:** Data cleaning, querying and analysis.
- **SQL:** Data manipulation, aggregations and business analysis.
- **Microsoft PowerPoint:** Project presentation and reporting.

## 🧹 Data Cleaning & Preparation

The following data cleaning and validation operations were performed:

- Checked NULL values across all 10 columns.
- Checked blank and empty string values.
- Identified duplicate records.
- Used `ROW_NUMBER()` to identify and remove duplicate rows.
- Validated menu prices and other important fields.
- Prepared the dataset for further analysis.

### Data Quality Findings

- NULL cells found: 0
- Exact duplicate rows identified: 27
- Minimum listed price: ₹1
- Maximum listed price: ₹8,000

## 🗂️ Data Modelling – Star Schema

The project uses a Star Schema to organize restaurant and menu information into dimension tables and a central fact table.

### Fact Table

**FACT_SWIGGY_ORDERS**

Contains:
- Price_INR
- Rating
- Rating_Count
- Dimension keys

### Dimension Tables

| Table Name | Description |
|---|---|
| DIM_DATE | Date, year, month, quarter and week |
| DIM_LOCATION | State, city and location |
| DIM_RESTAURANT | Restaurant names |
| DIM_CATEGORY | Food categories |
| DIM_DISH | Dish names |

This structure helps organize the data and perform analysis across different business dimensions.

## 📈 Key Performance Indicators (KPIs)

The following KPIs were calculated using SQL:

| KPI | Result |
|---|---:|
| Total Dataset Records | 197,430 |
| Unique Restaurants | 993 |
| Average Dish Price | ₹268.51 |
| Average Customer Rating | 4.34 / 5 |
| Total Rating Count | 5,591,574 |
| Total Cities | 28 |

## 🔍 SQL Analysis Performed

### 1. Restaurant Analysis
- Top 10 restaurants by representation.
- Restaurant-wise record distribution.
- Restaurant coverage across locations.

### 2. Location Analysis
- City-wise restaurant distribution.
- State-wise restaurant analysis.
- Top 10 cities based on the selected price-based metric.

### 3. Food Category Analysis
- Most frequently listed food categories.
- Category-wise record counts.
- Category-wise average customer ratings.

### 4. Pricing Analysis
- Average and median menu prices.
- Price range classification.
- Food item price distribution.

### 5. Customer Rating Analysis
- Average customer ratings.
- Rating distribution.
- Rating count analysis.

### 6. Date-Based Analysis
- Monthly trends.
- Quarterly trends.
- Yearly trends.
- Day-of-week analysis.

### SQL Concepts Used

- SELECT and WHERE
- GROUP BY and ORDER BY
- Aggregate Functions
- CASE Statements
- Subqueries
- Common Table Expressions (CTEs)
- ROW_NUMBER()
- Joins
- Date Functions
- Primary Keys and Foreign Keys
- Star Schema Modelling

## 💡 Key Business Insights

1. **City Analysis:** Bengaluru recorded the highest dataset volume with 20,077 records.

2. **Restaurant Analysis:** McDonald's was the most represented restaurant with 13,530 records, followed by KFC with 12,961 records.

3. **Pricing Analysis:** The average listed dish price was ₹268.51, while the median price was ₹229.

4. **Customer Ratings:** The average displayed customer rating was 4.34 out of 5.

5. **Price Distribution:** The ₹100–₹199 price range had the highest number of records, with 56,375 entries.

6. **Rating Distribution:** The 4.1–4.5 rating range had the highest number of records, with 125,136 entries.

## 📁 Project Folder Structure

```text
Swiggy-Sales-Analysis/
│
├── README.md
│
├── 01_Business_Problem/
│   └── Business_Problem.pdf
│
├── 02_Dataset/
│   └── Swiggy_Data.csv
│
├── 03_SQL_Queries/
│   └── Swiggy_Sales_Analysis.sql
│
├── 04_Project_Presentation/
│   └── Swiggy_Sales_Analysis.pptx
│
└── 05_Project_Screenshots/
    ├── Project_Overview.png
    ├── Restaurant_Analysis.png
    └── Ratings_Analysis.png
```

## 🚀 How to Run This Project

1. Download or clone this repository.
2. Open SQL Server Management Studio (SSMS).
3. Create a database for the project.
4. Import the Swiggy dataset into SQL Server.
5. Ensure the imported table is named `swiggy_data`.
6. Open the SQL script from the `03_SQL_Queries` folder.
7. Execute the SQL queries to perform data cleaning, dimensional modelling and analysis.
8. Review the query results and business insights.

## 📌 Conclusion

This project demonstrates how SQL Server can be used to clean, transform, organize, and analyze restaurant and menu data.

Through data cleaning, dimensional modelling, KPI calculations, and business analysis, the project provides insights into restaurant distribution, food pricing, customer ratings, and food-category patterns across Indian cities.

## ⚠️ Important Data Interpretation

The supplied dataset contains restaurant and menu records, not verified transaction-level sales data. It does not include transaction IDs or quantities sold.

Therefore, record counts should not be interpreted as confirmed orders, and the sum of listed menu prices should not be interpreted as actual sales revenue.

## 👩‍💻 Author

**Swetha Podaralla**

Data Analytics Portfolio Project


