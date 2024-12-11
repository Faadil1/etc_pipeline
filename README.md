# etc_pipeline
# ETL Pipeline for Financial Data Analysis

This project demonstrates an ETL (Extract, Transform, Load) pipeline designed to clean, transform, and analyze financial data for the top 500 companies in India. The dataset includes details such as market capitalization and quarterly sales, and it categorizes companies based on quartiles for market cap and sales. This pipeline enables in-depth analysis of the financial landscape, helping identify trends, patterns, and key metrics for competitive insights.

---

## Dataset Overview

The dataset contains financial information for the **top 500 companies in India**, with the following columns:
- **Name**: Company name.
- **Market Capitalization (Crore)**: Total market capitalization of the company in crores.
- **Quarterly Sales (Crore)**: Total sales for the last quarter in crores.

### Categorization
The data is categorized based on:
- **Market Cap Quartiles**: Companies are grouped into `Small Cap`, `Mid Cap`, `Large Cap`, and `Mega Cap` categories based on their market capitalization.
- **Sales Quartiles**: Companies are grouped into `Low Sales`, `Moderate Sales`, `High Sales`, and `Very High Sales` categories based on their quarterly sales.

This dataset enables detailed analysis and comparison of companies, helping to identify trends and competitive insights within the Indian financial market.

---

## Features of the ETL Pipeline

The ETL pipeline is divided into three main steps:

### 1. **Extract**
- Reads the raw financial data from a CSV file (`data/raw_data.csv`).
- Loads the data into a Pandas DataFrame for processing.

### 2. **Transform**
- **Standardizes Column Names**: Converts all column names to lowercase and replaces spaces with underscores.
- **Handles Missing Values**: Removes rows with missing values.
- **Categorizes Data**: 
  - Groups companies into quartiles based on market capitalization.
  - Groups companies into quartiles based on quarterly sales.
- **Calculates New Metrics**: Adds a `sales_to_market_cap_ratio` column, representing the ratio of quarterly sales to market capitalization.

### 3. **Load**
- Saves the cleaned and transformed data to a new CSV file (`data/transformed_data.csv`) for further analysis.

---

## Project Structure
etl_pipeline/ ├── etl_pipeline.py # Main ETL pipeline script ├── README.md # Documentation for the project ├── requirements.txt # List of Python dependencies ├── data/ │ ├── raw_data.csv # Example raw dataset │ ├── transformed_data.csv # Example transformed dataset ├── models/ # (Optional) Additional transformation functions │ ├── transform.py # Transformation logic (if modularized)
