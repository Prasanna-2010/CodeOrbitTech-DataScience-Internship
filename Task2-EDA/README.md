# Task 2 - Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on the Superstore Sales dataset using Python.

The objective of EDA is to understand the structure of the data, identify important patterns and trends, detect possible outliers, and visualize relationships between different variables.

Pandas was used for data analysis, while Matplotlib and Seaborn were used to create visualizations.

---

## 🎯 Objectives

- Understand the structure of the dataset.
- Analyze numerical and categorical variables.
- Identify patterns and trends in sales.
- Study the distribution of sales values.
- Compare sales across different categories and regions.
- Identify potential outliers.
- Create meaningful visualizations.
- Summarize the major findings from the analysis.

---

## 📊 Dataset

**Dataset:** Superstore Sales Dataset

The dataset contains approximately 9,800 sales records and includes information about customers, products, categories, regions, shipping, and sales.

### Important Features

| Feature | Description |
|---|---|
| Order Date | Date when the order was placed |
| Ship Date | Date when the order was shipped |
| Ship Mode | Shipping method |
| Customer Name | Name of the customer |
| Segment | Customer segment |
| City | Customer city |
| State | Customer state |
| Region | Sales region |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product name |
| Sales | Sales amount |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 🔍 EDA Process

### 1. Data Loading

The dataset was loaded using Pandas.

```python
import pandas as pd
df = pd.read_csv("Superstore.csv")
```
### 2. Data Inspection

The structure and characteristics of the dataset were examined using:
```python
df.head()
df.shape
df.info()
df.describe()
```
### 3. Data Cleaning

Before performing EDA, the data was checked for:

- Missing values
- Duplicate records
- Incorrect data types
- Date formatting issues

Date columns were converted into appropriate datetime formats.

### 4. Univariate Analysis

Individual variables were analyzed to understand their distributions.

For example, the distribution of Sales was visualized using a histogram.
```python
sns.histplot(df["Sales"], kde=True)
plt.title("Distribution of Sales")
plt.show()
5. Categorical Analysis
```
Sales were compared across different categories and regions using bar charts.

Examples include:
- Sales by Category
- Sales by Region
- Sales by Sub-Category

### 6. Relationship Analysis

Scatter plots were used to explore relationships between numerical variables where applicable.

### 7. Outlier Detection

Sales distributions and visualizations such as box plots were used to identify unusually high or low values.

## 📈 Visualizations

The notebook contains visualizations such as:
- Histogram

Used to understand the distribution of sales values.
- Bar Charts

Used to compare sales across:

- Categories
- Regions
- Sub-Categories
- Scatter Plots

Used to investigate relationships between numerical variables.
- Box Plots

Used to identify the spread of data and possible outliers.

## 🔎 Key Findings

The EDA helped identify several useful patterns in the Superstore dataset:

- Sales vary considerably across individual orders.
- Different product categories contribute differently to total sales.
- Sales performance varies across geographical regions.
- Some products and sub-categories contribute significantly more sales than others.
- The Sales distribution contains high-value observations that can be investigated as potential outliers.
- Categorical analysis helps identify which product groups and regions perform better.

