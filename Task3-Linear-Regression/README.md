# Task 3 - Simple Linear Regression

## 📌 Project Overview

This project demonstrates the implementation of Simple Linear Regression using Python and Scikit-learn.

The Superstore Sales dataset is used to study the relationship between the time since the first recorded order and sales. The objective is to build a regression model, make predictions, evaluate its performance, and visualize the regression line.

---

## 🎯 Objectives

- Prepare data for linear regression.
- Convert the order date into a numerical feature.
- Split the dataset into training and testing sets.
- Train a Simple Linear Regression model.
- Generate predictions.
- Evaluate model performance.
- Visualize actual values and the regression line.
- Interpret the regression results.

---

## 📊 Dataset

**Dataset:** Superstore Sales Dataset

The dataset contains sales transaction information including order dates, customers, products, categories, regions, and sales.

### Features Used

**Independent Variable:**

`Days_Since_First_Order`

This represents the number of days between an order date and the earliest order date in the dataset.

**Dependent Variable:**

`Sales`

The model attempts to predict Sales based on the number of days since the first recorded order.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Methodology

### 1. Data Preparation

The `Order Date` column was converted into a proper datetime format.

A new numerical feature was created:

```python
df["Days_Since_First_Order"] = (
    df["Order Date"] - df["Order Date"].min()
).dt.days
```
### 2. Feature Selection

The independent and dependent variables were selected:
```python
X = df[["Days_Since_First_Order"]]
y = df["Sales"]
3. Train-Test Split
```
The dataset was divided into training and testing sets.

The training data was used to train the model, while the test data was used to evaluate its performance.

### 4. Model Training

A Simple Linear Regression model from Scikit-learn was trained on the training dataset.
```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
```
### 5. Prediction

The trained model was used to predict sales values for the test dataset.

### 6. Model Evaluation

The model was evaluated using regression metrics such as:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score
  
### 7. Visualization

A scatter plot and regression line were used to visualize the relationship between the independent variable and Sales.

## 📈 Regression Model

The model follows the basic linear regression equation:

`y = mx + c`

Where:

`y = predicted Sales
x = Days Since First Order
m = slope/coefficient
c = intercept`

The coefficient represents the expected change in Sales for a one-unit increase in the independent variable.

## 📊 Model Evaluation

The notebook calculates:

- Metric	Purpose
- MAE	Average absolute prediction error
- MSE	Average squared prediction error
- RMSE	Typical magnitude of prediction error
- R² Score	Measures how much variation is explained by the model

The exact metric values can be found in the Jupyter Notebook.

## 🔎 Key Findings

The regression analysis demonstrates the relationship between order timing and sales.

The results also show that Sales cannot necessarily be explained by order timing alone because sales are affected by many other factors, such as:

- Product
- Category
- Customer
- Region
- Quantity
- Discounts
- Shipping
- Seasonality

Therefore, Simple Linear Regression provides a basic understanding of the relationship but may not be sufficient for highly accurate sales prediction.
