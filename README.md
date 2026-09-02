# ⚡ Hourly Energy Consumption Forecasting using Time Series Analysis & Machine Learning

> **An end-to-end time series forecasting project that compares classical statistical forecasting methods with Machine Learning models to predict hourly electricity demand.**

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange?style=for-the-badge&logo=pandas)
![LightGBM](https://img.shields.io/badge/LightGBM-Gradient%20Boosting-green?style=for-the-badge)
![Statsmodels](https://img.shields.io/badge/Statsmodels-SARIMA-red?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)

---

# 📖 Project Overview

Accurate electricity demand forecasting is essential for efficient power grid management, energy planning, and resource optimization. This project implements an end-to-end forecasting pipeline that compares **traditional statistical forecasting techniques** with **Machine Learning models** to understand their strengths, limitations, and forecasting performance.

Instead of focusing solely on prediction accuracy, this project emphasizes:

- Time Series Analysis
- Statistical Forecasting
- Feature Engineering
- Model Evaluation
- Forecast Accuracy Metrics
- Fair Model Comparison
- Interpretation of Results

---

# 🎯 Objectives

- Analyze historical hourly electricity consumption data
- Identify trend, seasonality and stationarity
- Build baseline forecasting models
- Perform feature engineering for ML
- Train a LightGBM regression model
- Compare statistical and machine learning approaches
- Evaluate forecasting performance using multiple metrics
- Interpret forecasting results rather than only reporting scores

---

# 📂 Repository Structure

```
Hourly-Energy-Consumption
│
├── DataSet/
│
├── Images/
│
├── Notebooks/
│   ├── 01_Data_Loading_and_Exploratory_Data_Analysis.ipynb
│   ├── 02_Baseline_Time_Series_Forecasting.ipynb
│   ├── 03_Feature_Engineering_and_LightGBM.ipynb
│   └── 04_Final_Model_Comparison_and_Analysis.ipynb
│
└── README.md
```

---

# 🚀 Project Workflow

---

# 📘 Notebook 1 — Data Loading & Exploratory Data Analysis

### 🎯 Objective

Explore the dataset and understand the characteristics of the hourly energy consumption before forecasting.

### Tasks Performed

- Imported and explored the hourly energy dataset
- Converted timestamp into datetime format
- Checked missing values and duplicates
- Performed exploratory data analysis
- Visualized yearly and monthly consumption trends
- Identified daily and weekly seasonality
- Generated ACF and PACF plots
- Performed Augmented Dickey-Fuller (ADF) Test for stationarity

### Improvements Implemented

✅ Added ADF Test to validate stationarity

✅ Extended PACF interpretation

✅ Added explanation of weekly seasonality observed in ACF

✅ Removed redundant preprocessing code

### Outputs

- Clean Dataset
- Trend Analysis
- Seasonality Visualization
- ACF & PACF Plots
- ADF Test Report

---

# 📙 Notebook 2 — Baseline Forecasting Models

### 🎯 Objective

Develop baseline statistical forecasting models and establish performance benchmarks.

### Models Implemented

- Naive Forecast (t−1)
- Seasonal Naive (t−24)
- Seasonal Naive (t−168)
- SARIMA

### Tasks Performed

- Created chronological train-test split
- Reserved last 7 days for testing
- Built baseline forecasting models
- Generated future predictions
- Compared forecasting performance
- Calculated MAE, RMSE and MAPE

### Improvements Implemented

✅ Removed duplicate forecasting workflow

✅ Added MAE leaderboard

✅ Added MAPE evaluation

✅ Added combined Actual vs Forecast visualization

✅ Updated conclusion based on actual leaderboard results

✅ Explained why Seasonal Naive (t−168) can outperform SARIMA

✅ Documented SARIMA's limitation in capturing weekly seasonality

### Outputs

- Forecast Comparison
- Leaderboard
- Error Metrics
- Model Performance Analysis

---

# 📗 Notebook 3 — Feature Engineering & LightGBM

### 🎯 Objective

Transform the forecasting problem into a supervised Machine Learning task using engineered temporal features.

### Feature Engineering

#### Lag Features

- lag_1
- lag_24
- lag_168

#### Rolling Features

- rolling_mean_24
- rolling_mean_168
- rolling_std_24
- rolling_std_168

#### Time Features

- Hour
- Day of Week
- Month
- Quarter
- Weekend Indicator

### Machine Learning Model

- LightGBM Regressor

### Tasks Performed

- Engineered lag and rolling features
- Prevented data leakage using shifted rolling windows
- Trained LightGBM model
- Generated feature importance
- Compared ML model against statistical baselines

### Improvements Implemented

✅ Eliminated feature leakage

✅ Used shift() before rolling calculations

✅ Added Feature Importance visualization

✅ Corrected feature interpretation based on actual output

✅ Added LightGBM to leaderboard

✅ Compared one-step forecasting with recursive forecasting

✅ Explained why LightGBM significantly outperformed baseline models

### Outputs

- Feature Matrix
- Trained LightGBM Model
- Feature Importance Plot
- Updated Leaderboard
- Model Analysis

---

# 📕 Notebook 4 — Final Model Comparison & Analysis

### 🎯 Objective

Perform a comprehensive comparison of all forecasting approaches and summarize project findings.

### Models Compared

| Model | Category |
|--------|----------|
| Naive | Statistical |
| Seasonal Naive (24) | Statistical |
| Seasonal Naive (168) | Statistical |
| SARIMA | Statistical |
| LightGBM | Machine Learning |

### Tasks Performed

- Compared forecasting accuracy
- Ranked models using evaluation metrics
- Visualized forecast results
- Compared statistical and ML models
- Summarized key findings

### Improvements Implemented

✅ Consolidated all model evaluations

✅ Added visual comparison charts

✅ Explained fairness of model comparison

✅ Discussed recursive vs one-step forecasting

✅ Documented strengths and limitations of each model

### Outputs

- Final Leaderboard
- Model Comparison Charts
- Forecast Visualizations
- Final Conclusions

---

# 📊 Evaluation Metrics

| Metric | Description |
|----------|-------------|
| MAE | Mean Absolute Error |
| RMSE | Root Mean Squared Error |
| MAPE | Mean Absolute Percentage Error |

---

# 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib |
| Statistical Modeling | Statsmodels |
| Machine Learning | LightGBM |
| Notebook Environment | Jupyter Notebook |

---

# 📈 Key Learnings

- Time Series Forecasting
- Stationarity Analysis
- Seasonal Pattern Identification
- Statistical Forecasting Techniques
- Feature Engineering
- Machine Learning for Time Series
- Forecast Accuracy Evaluation
- Fair Model Comparison
- Model Interpretation

---
# 🎥 Project Demo

Want to understand the project in under a minute?

This short demo explains the problem, the solution, and how the forecasting model works in simple, non-technical language.

### 📺 Watch the Demo

▶️ **[Telecom Tower Energy Consumption Forecasting Demo](https://drive.google.com/file/d/1tHKcYqNb6UGi3ZOg7St9S5XAdwpCTQYy/view?usp=sharing)**

### 📌 What you'll see

- 📡 Why forecasting telecom tower energy consumption is important
- ⚠️ Challenges of inaccurate energy planning
- 📊 How historical data is transformed into meaningful features
- 🤖 How Time Series Analysis and LightGBM predict future energy consumption
- 📈 Model comparison and forecasting results
- 🌍 Real-world applications and impact

> 💡 *This demo is designed for both technical and non-technical audiences to provide a quick overview of the project.*

# 🚀 Future Improvements

- XGBoost Forecasting
- Facebook Prophet
- LSTM & GRU Models
- Hyperparameter Optimization
- Quantile Forecasting
- Streamlit Dashboard
- Real-time Forecasting API
- Model Deployment using Docker

---

# 📚 References

- Forecasting: Principles and Practice (FPP3)
- Statsmodels Documentation
- LightGBM Documentation
- Kaggle Hourly Energy Consumption Dataset

---

# 👩‍💻 Author

**Vanshika Agrawal**

B.Tech Computer Science & Engineering (AI & ML)

📧 GitHub: https://github.com/agrawalvanshika

---

## ⭐ If you found this project useful, consider giving it a Star!
