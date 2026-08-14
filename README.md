# Zepto Data Analysis Using PostgreSQL

## Project Overview

This project analyzes Zepto product data using PostgreSQL to explore product categories, pricing, discounts, inventory, stock availability, product weight, and estimated revenue.

The project covers data exploration, data cleaning, and business-oriented SQL analysis to identify useful insights from the product and inventory data.

## Dataset

The `zepto_v2.csv` dataset contains the following columns:

| Column | Description |
|---|---|
| `Category` | Product category |
| `name` | Product name |
| `mrp` | Maximum Retail Price |
| `discountPercent` | Discount percentage |
| `availableQuantity` | Available inventory quantity |
| `discountedSellingPrice` | Selling price after discount |
| `weightInGms` | Product weight in grams |
| `outOfStock` | Indicates whether the product is out of stock |
| `quantity` | Product quantity |

## Database

The project uses PostgreSQL with the database:

`zepto_SQL_project`

The main table used for the analysis is:

`zepto`

A `sku_id` column is generated as a PostgreSQL `SERIAL` primary key when the table is created.

## Tools & Technologies

- PostgreSQL
- SQL
- CSV Dataset

## Data Exploration

The project explored the dataset by:

- Counting the total number of records
- Examining sample records
- Checking for null values
- Identifying different product categories
- Comparing products that are in stock and out of stock
- Identifying product names associated with multiple SKUs

## Data Cleaning

The following data cleaning steps were performed:

- Created the `zepto` table with appropriate PostgreSQL data types
- Identified products with zero MRP or discounted selling price
- Removed products with zero MRP
- Converted price values from paise to rupees
- Verified the updated MRP and discounted selling prices

## Data Analysis

### 1. Best-Value Products

Identified the top 10 products offering the highest discount percentages.

### 2. High-MRP Out-of-Stock Products

Identified products with an MRP greater than ₹300 that were out of stock.

### 3. Estimated Revenue by Category

Calculated estimated revenue for each category using discounted selling price and available quantity.

### 4. High-MRP Low-Discount Products

Identified products with an MRP greater than ₹500 and a discount percentage below 10%.

### 5. Highest Average Discount Categories

Identified the top 5 categories with the highest average discount percentage.

### 6. Price per Gram

Calculated the price per gram for products weighing at least 100 grams to identify products offering better value based on weight.

### 7. Product Weight Classification

Classified products into three weight categories:

- `Low` — Less than 1000 grams
- `Medium` — 1000 to less than 5000 grams
- `Bulk` — 5000 grams or more

### 8. Total Inventory Weight by Category

Calculated the total inventory weight for each product category using product weight and available quantity.

## SQL Concepts Used

- `CREATE TABLE`
- `DROP TABLE`
- `SELECT`
- `WHERE`
- `DISTINCT`
- `COUNT()`
- `SUM()`
- `AVG()`
- `ROUND()`
- `GROUP BY`
- `HAVING`
- `ORDER BY`
- `LIMIT`
- `DELETE`
- `UPDATE`
- `CASE WHEN`
- Boolean filtering
- Aggregate Functions
- Data Cleaning
- Conditional Classification
- PostgreSQL Data Types
- Primary Keys

## Key Skills Demonstrated

- PostgreSQL Data Analysis
- Data Exploration
- Data Cleaning
- Inventory Analysis
- Product Analysis
- Revenue Analysis
- Pricing Analysis
- Discount Analysis
- SQL Aggregation
- Business-Oriented Data Analysis

## Project Files

- `ps zepto pro.sql` — PostgreSQL queries used for data exploration, cleaning, and analysis
- `zepto_v2.csv` — Dataset used for the analysis

## Project Structure

```text
zepto-sql-analysis/
│
├── README.md
├── ps zepto pro.sql
└── zepto_v2.csv
