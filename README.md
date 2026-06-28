# istanbul-retail-data-analysis

## 📌 Project Overview
This project focuses on analyzing retail transaction data to uncover customer purchasing behavior, evaluate statistical significance, and build predictive machine learning models. 

The analysis is structured into two main phases: **Exploratory Data Analysis (EDA)** to understand the data's baseline distribution, and **Advanced Statistical & Machine Learning Modeling** to identify key revenue drivers and predict transaction spending.

### 📊 Dataset
The dataset used in this project is the **Customer Shopping Dataset**, which contains shopping information from 10 different shopping malls in Istanbul, Turkey.
* **Data Source:** [Kaggle - Customer Shopping Dataset](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset)
* **Key Features:** Invoice Number, Customer ID, Gender, Age, Category, Quantity, Price, Payment Method, Shopping Mall.

---

## 🛠️ Analysis Methodology

### 1. Exploratory Data Analysis (EDA)
Before diving into statistical modeling, we conducted a thorough Exploratory Data Analysis (EDA). EDA is a critical first step in data science used to investigate the dataset, discover underlying patterns, spot anomalies, and check assumptions with the help of summary statistics and graphical representations. In this project, EDA helped us:
* Understand customer demographics (age and gender distribution).
* Analyze sales trends across different shopping malls and product categories.
* Identify the distribution of payment preferences.

### 2. Linear Correlation & Feature Exploration
We extended our analysis to investigate relationships between different continuous and categorical variables:
* **Age vs. Spending:** Investigated whether a linear relationship exists between customer age and total spend using Pearson correlation and scatter plots (revealing near-zero correlation).
* **Multivariate Distribution:** Generated pairplots to visualize the pairwise relationships and data structures across numerical metrics like price, quantity, and total spend.

### 3. Statistical Diagnostic & Predictive Modeling
To move from exploration to validation, we applied both statistical modeling and machine learning techniques:
* **OLS Regression Analysis:** Used to diagnose the statistical significance ($p$-values) of categorical variables (`category`, `payment_method`, `shopping_mall`) on basket size, establishing that product category is the dominant driver of transaction volume.
* **Linear Regression (Machine Learning):** Implemented using `scikit-learn` with an 80/20 train-test split to predict future transaction values, achieving a robust R-squared (~0.49) on unseen test data.