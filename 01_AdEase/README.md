# AdEase – Forecasting

## Project Overview

This project focuses on analyzing and forecasting Wikipedia page views to help AdEase, an advertising and marketing company, optimize advertising placements across different languages and regions.

The objective is to understand historical page-view patterns and develop time-series forecasting models to predict future traffic.

## Business Problem

AdEase aims to help businesses maximize advertising reach while minimizing advertising costs.

To achieve this, the project analyzes historical Wikipedia page-view data and forecasts future traffic. These predictions can support better advertising placement decisions based on expected page popularity.

## Project Objectives

- Analyze historical Wikipedia page-view data.
- Identify traffic patterns and weekly seasonality.
- Explore page-view trends across different languages.
- Apply time-series forecasting techniques.
- Evaluate forecasting performance using appropriate error metrics.
- Generate insights to support advertising placement optimization.

## Dataset Description

The primary dataset contains:

- 145,063 Wikipedia pages.
- 550 daily page-view observations.
- 551 columns, including the page identifier and daily observations.
- Additional campaign/event indicator data for time-series analysis.

## Tools & Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Statsmodels
- Scikit-learn
- Prophet

## Methodology

1. Data Loading and Understanding
2. Data Cleaning and Preprocessing
3. Exploratory Data Analysis
4. Time-Series Trend and Seasonality Analysis
5. Stationarity and Differencing
6. Autocorrelation and Partial Autocorrelation Analysis
7. Time-Series Model Development
8. Forecast Evaluation and Comparison

## Forecasting Models

- ARIMA
- SARIMAX
- Prophet

## Model Evaluation

The forecasting models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

## Key Takeaway

This case study demonstrates how time-series analysis and forecasting techniques can be applied to historical web traffic data to support business planning and advertising optimization.

## Conclusion

The project provides practical experience in exploratory data analysis, time-series modeling, forecasting, and model evaluation using Python.

---

**Project Category:** Data Science | Time-Series Forecasting  
**Tools:** Python, Pandas, NumPy, Statsmodels, Prophet
