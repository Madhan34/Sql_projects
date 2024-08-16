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
CREATE DATABASE p1_retail_db;

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
