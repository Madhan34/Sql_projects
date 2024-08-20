# Retail Sales Analysis SQL Project

## Project Overview

**Project Title**: Retail Sales Analysis    
**Database**: `RETAIL_SALES_ANALYSIS`

This project aims to illustrate SQL skills and methodologies often used by data analysts to examine, clean, and analyze retail sales data. The project entails creating a retail sales database, conducting exploratory data analysis (EDA), and answering particular business questions using SQL queries. This project is suitable for people who are just starting out in data analysis and wish to have a strong foundation in SQL.

## Goals

1. **Construct a retail sales database**: Using the sales data that has been supplied, create and fill a retail sales database.
2. **Data Cleaning**: Find and eliminate any entries that have null or missing values.
3. **Exploratory Data Analysis (EDA)**: To comprehend the dataset, do out rudimentary exploratory data analysis.
4. **Business Analysis**: Utilize SQL to find answers to particular business queries and gain understanding from sales information.

## Project Structure

### 1. Database Setup

- **Database Creation**: The project starts by creating a database named `RETAIL_SALES_ANALYSIS`.
- **Table Creation**: A table named `RETAIL_SALES_ANALYSIS` is created to store the sales data. The table structure includes columns for transaction ID, sale date, sale time, customer ID, gender, age, product category, quantity sold, price per unit, cost of goods sold (COGS), and total sale amount.

```sql
CREATE DATABASE Retail_Sales_Analysis;
GRANT ALL PRIVILEGES TO Retail_Sales_Analysis;

CREATE TABLE Retail_Sales_Analysis
(
    transactions_id NUMBER,
    sale_date DATE,
    sale_time VARCHAR2(8),
    customer_id NUMBER,
    gender VARCHAR2(6),
    age NUMBER,
    category VARCHAR2(50),
    quantity NUMBER,
    price_per_unit NUMBER,
    cogs NUMBER,
    total_sale NUMBER
);
```

### 2. Data Exploration & Cleaning

- **Record Count**: Determine the total number of records in the dataset.
- **Customer Count**: Find out how many unique customers are in the dataset.
- **Category Count**: Identify all unique product categories in the dataset.
- **Null Value Check**: Check for any null values in the dataset and delete records with missing data.

 ```sql
   select COUNT (*) from retail_sales_analysis;
   select count(distinct(CUSTOMER_ID)) as customers from retail_sales_analysis;
   select unique(CATEGORY) from retail_sales_analysis;
   SELECT * FROM retail_sales_analysis WHERE 
    sale_date IS NULL OR sale_time IS NULL OR customer_id IS NULL OR 
    gender IS NULL OR age IS NULL OR category IS NULL OR 
    quantity IS NULL OR price_per_unit IS NULL OR cogs IS NULL;```
