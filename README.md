# Black-Friday-Sales-Forecast
Machine Learning project to analyze customer behavior and predict purchase amounts during Black Friday sales.

![Black Friday Sales Prediction](https://searchengineland.com/figz/wp-content/seloads/2014/12/black-friday1-ss-1920.jpg "Black Friday Sales Prediction")

## Table of Contents
- [Project Introduction](#project-introduction)
- [Dataset Description](#dataset-description)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preparation](#data-preparation)
- [Modeling Phase](#modeling-phase)
- [Evaluation Metric](#evaluation-metric)
- [Technologies Used](#technologies-used)
- [Conclusion](#conclusion)

---

## Project Introduction

Black Friday is a major shopping event that drives massive sales volumes across the retail industry. For both brick-and-mortar stores and e-commerce platforms, accurately predicting customer spending is essential to optimize marketing, inventory, and pricing strategies.

This project aims to analyze customer purchasing behavior and develop machine learning models to predict purchase amounts using historical transaction data. The insights and predictions generated can help businesses create personalized offers and forecast revenue more effectively.

---

## Dataset Description

The dataset for this project originates from an online analytics competition hosted by **Analytics Vidhya**. It consists of detailed purchase records, capturing customer demographics and product information.

**Key attributes include:**

- **User ID**  
- **Product ID**  
- **Gender**  
- **Age** (in bins)  
- **Occupation**  
- **City Category**  
- **Years of Stay in Current City**  
- **Marital Status**  
- **Product Categories (1, 2, 3)**  
- **Purchase Amount** *(Target Variable)*

The dataset contains **537,577 entries** and **12 columns** in total.

---

## Exploratory Data Analysis (EDA)

During EDA, several important trends and patterns were discovered:

- **Gender:** Males contributed approximately 75% of total transactions and also showed higher average spending compared to females.
- **Marital Status:** Single users made more purchases overall, but average spending remained similar between married and unmarried customers.
- **Age Group:** Users aged **26–35 years** dominated the purchase volume, indicating higher spending propensity in this segment.
- **City Category:** While **City B** recorded the highest sales volume, **City C** had customers with higher per-transaction spending on average.
- **Stay in Current City:** Newer residents (1–2 years) exhibited greater purchase frequency, suggesting higher initial spending behavior.

Visualizations were created using **Matplotlib** and **Seaborn** to better understand these relationships.

---

## Data Preparation

To prepare the data for modeling, the following steps were performed:

- **Label Encoding:** Applied to `Gender`, `Age`, and `City_Category` to convert categorical variables into numeric format.
- **One-hot Encoding:** Used on `Stay_In_Current_City_Years` to capture duration of stay.
- **Missing Values:** Filled missing values in `Product_Category_2` and `Product_Category_3` with 0.
- **Dropping Irrelevant Columns:** `User_ID` and `Product_ID` were removed, as they do not contribute predictive value.

---

## Modeling Phase

After preprocessing, the dataset was split into training and testing sets (70:30 ratio). Four regression models were implemented and evaluated:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**

Hyperparameters were tuned where applicable to improve performance.

---

## Evaluation Metric

The primary evaluation metric used was **Root Mean Square Error (RMSE)**. RMSE measures the average magnitude of the prediction error and is widely used for regression problems.

Lower RMSE values indicate better model performance.

---

## Technologies Used

- **Python**  
- **Pandas** – Data manipulation and cleaning  
- **NumPy** – Numerical operations  
- **Matplotlib & Seaborn** – Data visualization  
- **Scikit-learn** – Preprocessing, regression modeling, evaluation metrics  
- **XGBoost** – Gradient boosting regression model  
- **Google Colab / Jupyter Notebook** – Interactive development environment

---

## Conclusion

Multiple models were trained and compared to identify the most effective approach for predicting purchase amounts.

Among all the models tested, the **XGBoost Regressor** achieved the best performance with an RMSE of **2879**, making it the preferred model for this project.

The insights generated from EDA and the predictive model can help retailers better understand customer segments and optimize their marketing and sales strategies during major shopping events like Black Friday.

---
