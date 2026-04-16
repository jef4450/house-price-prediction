# 🏠 House Price Prediction (Kaggle Competition)

## 📌 Overview
This project is a machine learning solution for the Kaggle competition **"House Prices: Advanced Regression Techniques"**.  
The goal is to predict housing prices based on 79 features describing various aspects of residential homes in Ames, Iowa.

---

## 🚀 Problem Statement
Given a dataset of house attributes (size, quality, location, etc.), predict the final sale price of each house.

Evaluation metric:
- Root Mean Squared Error (RMSE) on log-transformed prices

---

## 🧠 Approach

### 1. Data Preprocessing
- Combined train and test datasets for consistent preprocessing
- Handled missing values:
  - Numerical → median imputation
  - Categorical → filled with `"None"`
- Applied one-hot encoding using `pd.get_dummies()`

---

### 2. Feature Engineering
Created new meaningful features:
- `TotalSF` = Total square footage (basement + 1st + 2nd floor)
- `HouseAge` = Year sold − year built

---

### 3. Target Transformation
- Applied log transformation to reduce skewness:
  - `SalePrice = log(SalePrice)`

---

### 4. Model Used
- XGBoost Regressor
- Tuned parameters:
  - n_estimators = 1000
  - learning_rate = 0.05
  - max_depth = 4
  - subsample = 0.8
  - colsample_bytree = 0.8

---

## 📊 Results
- Kaggle Public Leaderboard Score: **~0.132 RMSE**

---

## 🛠️ Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Kaggle Notebook

---

## 📈 Key Insights
- Overall quality of the house is the strongest predictor of price
- Total living area significantly impacts price
- Garage size and condition influence property value
- Newer houses tend to have higher prices
- Location and zoning play a major role in pricing

---

## 📁 Files in this repository
- `notebook.ipynb` → Full ML pipeline
- `submission.csv` → Kaggle submission file

---

## 🔗 Competition Link
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

---

## 👤 Author
Built as a machine learning portfolio project using Kaggle datasets.
