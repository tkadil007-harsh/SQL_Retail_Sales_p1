# SQL_Retail_Sales_p1

## Project Overview


**Project Title**: Retail Sales Analysis  
**Database**: `sql_projectc_p2`

This project is designed to demonstrate SQL skills and techniques typically used by data analysts to explore, clean, and analyze retail sales data. The project involves setting up a retail sales database, performing exploratory data analysis (EDA), and answering specific business questions through SQL queries. This project represents my foundational work in SQL and data analysis.

## Objectives

1. **Set up a retail sales database**: Create and populate a retail sales database with the provided sales data.
2. **Data Cleaning**: Identify and remove any records with missing or null values.
3. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
4. **Business Analysis**: Use SQL to answer specific business questions and derive insights from the sales data.

## Project Structure

### 1. Database Setup

- **Database Creation**: The project starts by creating a database named `sql_projectc_p2`.
- - **Table Creation**: A table named `retail_sales` is created to store the sales data. The table structure includes columns for transaction ID, sale date, sale time, customer ID, gender, age, product category, quantity sold, price per unit, cost of goods sold (COGS), and total sale amount.

```sql
CREATE DATABASE sql_projectc_p2;
CREATE TABLE retail_sales
 (
               transactions_id	INT PRIMARY KEY,
			   sale_date DATE,	
			   sale_time TIME, 	
			   customer_id INT,
			   gender VARCHAR(15),
			   age INT,
			   category VARCHAR(15),
			   quantiy INT,
			   price_per_unit FLOAT,
			   cogs FLOAT,
			   total_sale FLOAT
);
```


### 2. Data Exploration & Cleaning

- **Record Count**: Determine the total number of records in the dataset.
- **Customer Count**: Find out how many unique customers are in the dataset.
- **Category Count**: Identify all unique product categories in the dataset.
- **Null Value Check**: Check for any null values in the dataset and delete records with missing data.

```sql
SELECT COUNT(*) FROM retail_sales;
SELECT COUNT(DISTINCT customer_id) FROM retail_sales;
SELECT DISTINCT category FROM retail_sales;

SELECT * FROM retail_sales
WHERE  
     transactions_id IS NULL
	 OR
	 sale_date IS NULL
	 OR
	 sale_time IS NULL
	 OR
	 customer_id IS NULL
	 OR
	 gender IS NULL
	 OR
	 category IS NULL 
	 OR
	 quantiy IS NULL 
	 OR
	 cogs IS NULL 
	 OR
	 total_sale IS NULL;

DELETE FROM retail_sales
WHERE  
     transactions_id IS NULL
	 OR
	 sale_date IS NULL
	 OR
	 sale_time IS NULL
	 OR
	 customer_id IS NULL
	 OR
	 gender IS NULL
	 OR
	 category IS NULL 
	 OR
	 quantiy IS NULL 
	 OR
	 cogs IS NULL 
	 OR
	 total_sale IS NULL;

```

















