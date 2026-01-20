# Hourly Energy Consumption Prediction using XGBoost 

##  Project Overview
This project focuses on forecasting future energy consumption using historical time-series data. By analyzing over 10 years of hourly energy data (PJME), I built a Machine Learning model to predict energy demand patterns.

The goal is to understand how time-based features (hour of the day, day of the week, seasons) impact energy usage and to provide accurate forecasts using the **XGBoost** algorithm.

##  Dataset
* **Source:** PJME (PJM Interconnection LLC) Hourly Energy Consumption Data.
* **Range:** 2002 - 2018.
* **Target:** `PJME_MW` (Megawatts).
* **Split:** Training data (Before 2015) and Test data (2015 and after).

##  Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, XGBoost, Scikit-Learn.

##  Methodology
1.  **Data Preprocessing:** Converted timestamps to datetime objects and sorted the data.
2.  **Feature Engineering:** Created time-series features such as `hour`, `dayofweek`, `quarter`, `month`, and `year` to capture seasonality and daily trends.
3.  **Model Training:** Trained an **XGBRegressor** with 1000 estimators and early stopping to prevent overfitting.
4.  **Evaluation:** Used **RMSE (Root Mean Squared Error)** to evaluate model performance on the unseen test set.

## Results
* **Feature Importance:** The model identified that the **Hour of the day** is the most significant factor in predicting energy consumption, followed by the **Month** (seasonality).

##  How to Run
1.  Clone the repository.
2.  Install dependencies: `pip install pandas xgboost matplotlib sklearn`
3.  Run the Jupyter Notebook: `Energy_Prediction.ipynb`
