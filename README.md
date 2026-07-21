# 📊 Superstore Sales Data Analysis & Power BI Dashboard

## Project Overview

This project demonstrates a complete data analytics workflow using Python and Power BI. The pipeline starts with a raw Superstore sales dataset, performs data cleaning and feature engineering in a Jupyter Notebook, and produces a cleaned dataset that can be used for visualization in a Power BI dashboard.

The notebook also includes exploratory data analysis (EDA) with multiple visualizations to understand sales performance, profitability, and regional trends.

---

# Project Structure

```text
Superstore-Sales-Project/
│
├── SuperStore Sales DataSet.xlsx          # Raw dataset
├── Clean_Superstores_sales.xlsx           # Cleaned dataset
├── superstore_sales.ipynb                 # Data cleaning & analysis notebook
├── Superstore_Sales_dashboard.pbit        # Power BI dashboard template
└── README.md
```

---

# Data Dictionary (Cleaned Dataset)

| Column | Description |
|---------|-------------|
| Row ID+O6G3A1:R6 | Unique identifier for each sales record |
| Order ID | Unique order number |
| Order Date | Date when the order was placed |
| Ship Date | Date when the order was shipped |
| Ship Mode | Shipping method used |
| Customer ID | Unique customer identifier |
| Customer Name | Customer's full name |
| Segment | Customer segment (Consumer, Corporate, Home Office, etc.) |
| Country | Country where the order was placed |
| City | Customer city |
| State | Customer state |
| Region | Sales region |
| Product ID | Unique product identifier |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product description |
| Sales | Revenue generated from the sale |
| Quantity | Number of units sold |
| Profit | Profit earned from the order |
| Returns | Return status (missing values replaced with 0) |
| Payment Mode | Payment method used |
| Year | Year extracted from **Order Date** |
| Month | Month name extracted from **Order Date** |
| Profit Margin (%) | Calculated as `(Profit / Sales) × 100` |

---

# Data Cleaning & Feature Engineering

The notebook performs the following preprocessing steps:

- Loaded the Excel dataset using Pandas.
- Inspected dataset structure and summary statistics.
- Checked for missing values.
- Removed unnecessary columns:
  - `ind1`
  - `ind2`
- Filled missing values in the **Returns** column with `0`.
- Checked for duplicate records.
- Converted **Order Date** to datetime format.
- Created a new **Year** column from Order Date.
- Created a new **Month** column from Order Date.
- Calculated **Profit Margin (%)** using:

```python
Profit Margin (%) = (Profit / Sales) * 100
```

---

# Exploratory Data Analysis

The notebook includes visualizations for:

- 📈 Yearly Sales Trend (Bar Chart)
- 📊 Sales by Sub-Category
- 🥧 Regional Sales Distribution (Pie Chart)
- 📉 Sales vs Profit Scatter Plot
- 🔥 Correlation Heatmap

---

# Technologies Used

## Programming Language

- Python

## Python Libraries

- pandas
- numpy
- matplotlib
- seaborn
- warnings

## Business Intelligence

- Microsoft Power BI

## File Formats

- Excel (.xlsx)
- Jupyter Notebook (.ipynb)
- Power BI Template (.pbit)

---

# How to Run

## 1. Clone or Download the Project

Place all project files in the same folder.

---

## 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

---

## 3. Run the Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
superstore_sales.ipynb
```

Run all cells sequentially.

The notebook will:

- Load the raw dataset
- Clean the data
- Generate new features
- Perform exploratory analysis
- Produce the cleaned dataset for Power BI

---

## 4. Open the Power BI Dashboard

1. Open Microsoft Power BI Desktop.
2. Open:

```
Superstore_Sales_dashboard.pbit
```

3. If prompted, browse to the cleaned Excel dataset.
4. Refresh the data model.

The interactive dashboard will then be ready for analysis.

---

# Data Quality Improvements

The cleaning process improves data quality by:

- Removing unnecessary placeholder/index columns (`ind1` and `ind2`).
- Replacing missing values in the **Returns** column with `0` to avoid null-related issues during analysis.
- Standardizing **Order Date** into a proper datetime format for time-series analysis.
- Creating derived fields (**Year** and **Month**) to simplify trend analysis.
- Computing **Profit Margin (%)**, providing a more meaningful profitability metric.
- Checking for duplicate records to support dataset integrity.
- Producing a cleaner, analysis-ready dataset for Power BI and future reporting.

---

# Dashboard Purpose

The Power BI dashboard enables users to:

- Monitor yearly sales performance.
- Compare regional sales distribution.
- Analyze category and sub-category performance.
- Evaluate the relationship between sales and profit.
- Explore profitability using the calculated Profit Margin metric.

---

# Author

Data Analysis Project using **Python**, **Pandas**, **Jupyter Notebook**, and **Microsoft Power BI**.
