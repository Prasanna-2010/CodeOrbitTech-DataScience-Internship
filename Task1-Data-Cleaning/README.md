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
```

### 2. Dataset Inspection

The dataset structure was examined using functions such as:

```python
df.head()
df.shape
df.info()
df.columns.tolist()
```
### 3. Missing Value Detection

Missing values were identified using:
```python
df.isnull().sum()
```
The analysis showed missing values in the Postal Code column.

### 4. Missing Value Handling

The missing values were handled appropriately based on the nature of the column.

### 5. Duplicate Detection

Duplicate records were checked using:
```python
df.duplicated().sum()
```
### 6. Data Type Correction

Date columns were initially stored as object/string values.

They were converted into proper datetime format for further analysis.
```python
df["Order Date"] = pd.to_datetime(
    df["Order Date"],
    dayfirst=True
)

df["Ship Date"] = pd.to_datetime(
    df["Ship Date"],
    dayfirst=True
)
```
### 7. Statistical Analysis

Basic statistics such as mean and median were calculated for numerical columns.

Example:
```python
df["Sales"].mean()
df["Sales"].median()
```
### 8. Categorical Analysis

Value counts were used to understand the distribution of categorical variables.

Example:
```python
df["Category"].value_counts()
```

## 📈 Key Findings

After cleaning and exploring the dataset:

- The dataset contains approximately 9,800 records.
- The dataset contains 18 columns.
- Most columns contain complete data.
- A small number of missing values were found in the Postal Code column.
- Date columns required conversion from object/string format to datetime.
- Sales is a numerical variable suitable for statistical analysis.
- Category and Sub-Category can be analyzed using frequency counts.
