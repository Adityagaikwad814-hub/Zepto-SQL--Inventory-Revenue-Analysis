Zepto E-commerce Inventory & Revenue Analysis
Project Overview
This project performs an end-to-end SQL data analysis on a real-world e-commerce dataset scraped from Zepto, a leading quick-commerce platform
. The analysis mimics the role of a Data Analyst by exploring an inventory of 3,732 unique SKUs to uncover actionable business insights regarding pricing strategies, stock availability, and logistics planning
.
Dataset Description
The dataset contains 3,732 rows and 9 columns, representing unique product listings (SKUs)
. Key features include:
Product Information: Name, Category, and Weight
.
Pricing: MRP, Discount Percentage, and Final Selling Price
.
Inventory: Available Quantity and Out-of-Stock status
.
Tech Stack
Database: PostgreSQL
.
Interface: pgAdmin
.
Dataset Source: Kaggle (Scraped Zepto data)
.
Project Workflow
1. Environment Setup & Data Cleaning
Table Schema: Created a structured table with appropriate data types (Integer, Numeric, Varchar, Boolean) and a primary SKU_ID
.
Encoding Fixes: Resolved import errors by converting the source file to UTF-8 encoding
.
Invalid Data Removal: Identified and deleted records with an impossible MRP of zero
.
Currency Standardization: Converted prices from paise to rupees by dividing MRP and selling prices by 100
.
2. Exploratory Data Analysis (EDA)
Verified data integrity by checking for null values across all columns
.
Analyzed product distribution across categories such as Beverages, Dairy, Fruits & Vegetables, and Personal Care
.
Quantified stock levels, identifying that 453 products were currently out of stock
.
3. Business Insights & SQL Queries
Advanced queries were used to solve specific business problems:
Revenue Optimization: Estimated total revenue per category by calculating Selling Price * Available Quantity
.
Missed Opportunities: Identified high-priced items (MRP > 300) that are currently out of stock to prioritize restocking
.
Discount Analysis: Found that Fruits and Vegetables offer the highest average discount at 15%, providing insights for marketing teams
.
Logistics & Weight Segmentation: Utilized CASE statements to categorize products into Low, Medium, and Bulk weight classes to assist in delivery and warehouse planning
.
Inventory Mass: Calculated the total weight per category to identify which products occupy the most warehouse space
.
Key Insights
Pricing Strategy: Identified top "best value" products with discounts exceeding 50%
.
Customer Value: Calculated price-per-gram for products over 100g to help compare value-for-money across different pack sizes
.
Warehouse Planning: Determined the categories contributing most to overall inventory weight, essential for operational efficiency.
