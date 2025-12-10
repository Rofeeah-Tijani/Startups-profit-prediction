# Startups-profit-prediction

## TABLE OF CONTENTS

[Project Overview](#-Project-Overview)

[❗Problem Statement](#-Problem-Statement)

[🎯Objective](#-Objective)

[📌Focus Areas](#-Focus-Areas)

[🌐Source Of Data](#-Source-Of-Data)

[📊 Dataset Description](#-Dataset-Description)

[🛠️Tool Used](#-Tool-Used)

[🔧Methodology](#-Methodology)

[Model Summary And Interpretation](#-Model-Summary-And-Interpretation)

[📬Let's Connect](#-Let's-Connect)

**Project Overview**  
This repository contains an analysis and predictive modelling workflow applied to a dataset of 50 startup observations. The goal is to explore how company expenditures and location (state) relate to **Profit** and to build a regression model that predicts profit using available features.

---

❗ **Problem Statement**  
Startups often need to decide how to allocate budgets (R&D, Administration, Marketing) to maximize profit. This project investigates how these expenditures and the company's state affect Profit, and builds models to predict Profit for new observations.

🎯 **Objective**  
- Explore relationships between expenditures, state, and profit.  
- Prepare features and build a regression model to predict Profit.  
- Evaluate model performance using metrics (R², MAE, MSE/RMSE).

📌 **Focus Areas**  
- Exploratory Data Analysis (EDA)  
- Feature engineering (scaling, dummy encoding for State)  
- Model building (linear regression baseline)  
- Diagnostics and assumptions for regression (residual analysis, heteroscedasticity, autocorrelation if relevant)  
- Model evaluation and interpretation

🌐 **Source Of Data**  
This dataset (`Startups.csv`) appears to be a classic startups dataset comprising R&D, Administration, Marketing expenditures, State, and Profit. It is included in this repo for demonstration/learning purposes.

📊 **Dataset Description**  
- **Rows:** 50  
- **Columns:** 5  

| Column | Type | Description |
|---|---:|---|
| R&D Expenditure | numeric | Amount spent on R&D (input feature) |
| Administration Expenditure | numeric | Amount spent on administration (input feature) |
| Marketing Expenditure | numeric | Amount spent on marketing (input feature) |
| State | categorical | State where the startup is located (feature to encode) |
| Profit | numeric | Target variable — company profit to predict |

All columns have no missing values in the provided file.

🛠️ **Tools Used**  
- Python (pandas, numpy, matplotlib, seaborn)  
- scikit-learn (modeling and evaluation)  
- statsmodels (diagnostics and formal regression tests)  
- Jupyter Notebook / VS Code for development

🔧 **Methodology**
1. Load and inspect the data (shape, types, missing values).  
2. EDA/Assumptions: distribution of features, pairplots/scatterplots, correlation matrix, boxplots for outliers.  
3. Preprocessing: split into train/test.  
4. Baseline model: Linear Regression. Compute metrics (R², MAE, MSE).  
5. Diagnostics: residual plots, Breusch–Pagan (post-fit), Durbin–Watson (post-fit) .   
6. Final model evaluation and interpretation.

📊 **Model Summary and Interpretation**

After training a Linear Regression model on the startup dataset, the following performance metrics were obtained:

Model Performance Metrics

MSE (Mean Squared Error): 80,926,321.22

R² Score: 0.9001

MAE (Mean Absolute Error): 6,979.15

Interpretation

R² = 0.90 means the model explains 90% of the variation in Profit, showing a strong predictive relationship between expenditures (R&D, Administration, Marketing), State, and the actual Profit values.

MAE ≈ 6,979 indicates that, on average, the model's predictions are off by about 6,979 units of profit, which is relatively small when compared to the typical profit scale in the dataset (which is in the hundreds of thousands).

MSE ≈ 80.9 million reflects the squared magnitude of errors. Since MSE is highly sensitive to large deviations, this value is reasonable given the scale of the target variable.

Overall, the model shows strong predictive performance, with high explanatory power and reasonably low error, making it useful for estimating profit levels based on startup expenditures and state.


