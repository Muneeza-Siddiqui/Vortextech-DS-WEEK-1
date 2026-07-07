# Retail Sales Data Analysis

A comprehensive data analysis project exploring online retail transaction data to uncover patterns, trends, and actionable insights about customer behavior and product performance.

## Project Overview

This project performs an in-depth analysis of online retail transaction data to understand customer purchasing patterns, identify data quality issues, and extract meaningful business insights through exploratory data analysis and visualizations.

### Main Objectives

1. Load and clean the retail dataset
2. Handle missing values and remove duplicates
3. Perform exploratory data analysis (EDA)
4. Identify key patterns and trends in customer behavior
5. Create visualizations to communicate findings

---

## Dataset Description

### Source
Online retail transaction data from a UK-based e-commerce platform containing customer purchase history.

### Data Overview
- **Initial Records**: 541,909 transactions
- **After Cleaning**: 406,684 records
- **Features**: 8 columns

### Column Information

| Column | Type | Description |
|--------|------|-------------|
| InvoiceNo | String | Unique transaction identifier |
| StockCode | String | Product stock code |
| Description | String | Product description |
| Quantity | Integer | Number of units purchased |
| InvoiceDate | DateTime | Date and time of transaction |
| UnitPrice | Float | Price per unit in GBP |
| CustomerID | Integer | Unique customer identifier |
| Country | String | Customer's country |

### Key Statistics

- **Quantity Range**: -80,995 to 80,995 (includes returns)
- **Unit Price Range**: -£11,062.06 to £38,970.00
- **Average Transaction Quantity**: 9.55 units
- **Median Transaction Quantity**: 3.00 units
- **Average Unit Price**: £4.61

---

## Data Cleaning Process

### Issues Identified

1. **Missing Description Values**: 1,454 records
2. **Missing CustomerID**: 135,080 records (24.9% of data)
3. **Duplicate Records**: 5,225 rows

### Cleaning Steps Executed

1. **Missing Descriptions**: Filled with "Unknown" placeholder
2. **Incomplete Records**: Removed rows without CustomerID (essential for customer analysis)
3. **Duplicates**: Removed 5,225 duplicate records
4. **Data Type Conversion**: 
   - Converted InvoiceDate to datetime format
   - Converted CustomerID to integer type

### Final Result
- **Records Removed**: 135,080 + 5,225 = 140,305
- **Final Clean Dataset**: 406,684 records
- **Data Quality**: 0% missing values

---

## Exploratory Data Analysis

### Quantity Analysis
- Most transactions are small orders (median: 3 units)
- High variability in quantities (std dev: 218.08) due to bulk orders and returns
- Negative quantities represent returns and cancellations

### Price Analysis
- Highly diverse product portfolio with prices ranging from -£11,062 to £38,970
- Median price: £2.08, indicating budget-friendly product focus
- Large standard deviation (£96.76) suggests significant price variations

### Customer Base
- Approximately 4,372 unique customers
- Global customer distribution across multiple countries
- Transactions span from December 2010 onwards

---

## What the Analysis Reveals

### Data Quality Insights
- **25% of records** initially lacked customer IDs, requiring removal for reliable customer-based analysis
- **Less than 1%** of records were duplicates, indicating generally good data integrity
- Product descriptions missing in a small percentage of records, easily handled with placeholder values

### Business Insights
- **Mixed transaction patterns**: Combination of small individual purchases and bulk orders
- **Return activity**: Presence of negative quantities indicates active returns/cancellation processes
- **Diverse pricing strategy**: Wide range of product prices suggests varied product categories
- **Global operations**: Customer base spans multiple countries

### Key Findings
- After cleaning, the dataset provides reliable foundation for customer segmentation analysis
- Transaction patterns show typical e-commerce behavior with predominance of small orders
- Data quality issues are manageable and don't significantly impact analysis reliability

---

## Technologies Used

- **Python 3**: Programming language
- **Pandas**: Data manipulation and cleaning
- **NumPy**: Numerical computations
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive analysis environment

---

## How to Use

1. **Load the notebook**: Open `task1.ipynb` in Jupyter Notebook
2. **Prepare the data**: Ensure `data.csv` is in the project directory
3. **Run the cells**: Execute cells sequentially to see the analysis flow
4. **Review outputs**: Each cell displays the results of data cleaning and analysis steps

---

## Notebook Structure

The `task1.ipynb` contains:

1. **Library Setup** - Import required packages
2. **Data Loading** - Read the CSV file
3. **Data Preview** - Display sample data
4. **Data Inspection** - Check structure and info
5. **Statistical Summary** - Describe numeric columns
6. **Missing Values Analysis** - Identify gaps in data
7. **Data Cleaning** - Fill and remove incomplete records
8. **Duplicate Detection** - Find and remove duplicates
9. **Data Type Conversion** - Convert to appropriate types
10. **Summary Statistics** - Final analysis of cleaned data

---

**Project Created**: Vortextech Data Science Week 1  
**Status**: Data cleaning and exploration complete ✓
