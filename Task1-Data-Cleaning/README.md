# Task 1 - Data Cleaning & Exploration with Pandas

## 📌 Project Overview

This project focuses on data cleaning and basic data exploration using Python and Pandas.

A sample Superstore Sales dataset was used to identify and handle common data quality issues such as missing values, duplicate records, incorrect data types, and inconsistent date formats.

The cleaned dataset was then explored using basic statistical operations and value counts.

---

## 🎯 Objectives

- Load a CSV dataset using Pandas.
- Understand the structure and characteristics of the dataset.
- Identify missing values.
- Handle missing values appropriately.
- Check and handle duplicate records.
- Correct incorrect data types.
- Convert date columns into proper datetime format.
- Calculate basic statistics such as mean and median.
- Analyze categorical values using value counts.
- Summarize the data cleaning process.

---

## 📊 Dataset

**Dataset:** Superstore Sales Dataset

The dataset contains information about:

- Orders
- Customers
- Shipping
- Locations
- Products
- Categories
- Sub-categories
- Sales

### Important Columns

| Column | Description |
|---|---|
| Order ID | Unique identifier for an order |
| Order Date | Date on which the order was placed |
| Ship Date | Date on which the order was shipped |
| Ship Mode | Shipping method |
| Customer ID | Unique customer identifier |
| Customer Name | Customer name |
| Segment | Customer segment |
| City | Customer city |
| State | Customer state |
| Region | Sales region |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Name of the product |
| Sales | Sales amount |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- Matplotlib

---

## 🔍 Data Cleaning Steps

The following data-cleaning operations were performed:

### 1. Dataset Loading

The CSV dataset was loaded using Pandas.

```python
import pandas as pd

df = pd.read_csv("Superstore.csv")
