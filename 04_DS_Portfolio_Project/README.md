# Product Sales Forecasting Using Machine Learning

## Project Overview

This project focuses on predicting daily retail store sales using machine learning techniques. The analysis explores how factors such as store type, location, region, discounts, holidays, and dates influence sales performance.

The project compares Linear Regression and XGBoost Regressor models, evaluates their predictive performance, and deploys the best-performing model through a Flask web application for real-time sales predictions.

## Business Problem

Retail businesses need accurate sales forecasts to make better decisions about inventory planning, resource allocation, and revenue management.

The objective of this project is to predict daily sales for individual stores based on store-related information, location, regional characteristics, holidays, and discounts.

## Business Objectives

- Predict daily sales for retail stores using machine learning.
- Understand the impact of discounts and holidays on sales.
- Analyze sales performance across different store types and regions.
- Identify the most influential features affecting sales predictions.
- Compare machine learning models using appropriate evaluation metrics.
- Deploy the best-performing model through a web application.

## Dataset Description

The dataset contains historical retail sales information with the following characteristics:

| Attribute | Details |
|---|---|
| Training records | 188,340 |
| Unique stores | 365 |
| Date range | January 2018 – May 2019 |
| Missing values | No missing values after data cleaning |

The analysis considers store type, location type, region, discounts, holidays, weekends, days of the week, orders, and sales.

## Tools & Technologies

- **Python** – Data analysis and machine learning
- **Pandas & NumPy** – Data manipulation and preprocessing
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-learn** – Model development and evaluation
- **XGBoost** – Gradient boosting regression
- **SciPy** – Statistical hypothesis testing
- **Tableau** – Interactive sales dashboard
- **Flask** – Model deployment and web application
- **Pickle** – Saving the trained model and encoders

## Methodology

### 1. Data Cleaning and Preprocessing

- Inspected and prepared the historical sales dataset.
- Processed the data for analysis and model development.
- Verified that there were no missing values after data cleaning.
- Prepared relevant store, location, date, discount, and holiday features.

### 2. Exploratory Data Analysis

Analyzed sales patterns across different business dimensions:

- Store type and location type.
- Regional sales performance.
- Discount and holiday impact.
- Weekend and weekday sales patterns.
- Relationship between orders and sales.

### 3. Statistical Analysis and Hypothesis Testing

Conducted statistical tests to examine relationships and differences in sales:

| Hypothesis | Statistical Test | Result |
|---|---|---|
| Discounts increase sales | T-Test | Significant |
| Holidays affect sales | T-Test | Significant |
| Sales differ by store type | ANOVA | Significant |
| Sales vary by region | Kruskal-Wallis | Significant |
| Orders correlate with sales | Pearson Correlation | r = 0.94 |

All hypothesis tests were statistically significant at p < 0.05.

### 4. Machine Learning Model Development

Developed and compared two regression models:

- Linear Regression
- XGBoost Regressor

### 5. Model Evaluation

Evaluated model performance using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

## Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 9,789 | 13,520 | 0.459 |
| XGBoost Regressor | 5,488 | 7,918 | 0.8145 |

**Best Performing Model: XGBoost Regressor**

The XGBoost model achieved an R² score of 0.8145, explaining approximately 81.45% of the variance in sales.

It also achieved lower MAE and RMSE compared with Linear Regression.

## Key Business Insights

- **Discount impact:** Average sales were 32% higher with discounts (₹49,426) compared with without discounts (₹37,403).
- **Holiday impact:** Average sales were 19% lower on holidays (₹35,451) compared with non-holidays (₹43,897).
- **Store type:** Store Type S4 recorded the highest average sales of ₹59,945.
- **Store performance:** Store Type S2 recorded the lowest average sales of ₹27,530.
- **Regional performance:** Region R1 recorded the highest average sales of ₹46,765.
- **Orders and sales:** A strong positive correlation of 0.94 was observed between orders and sales.

## Feature Importance

The XGBoost model identified the following features as important contributors to sales predictions:

| Feature | Importance |
|---|---:|
| Store_Type | 0.40 |
| Location_Type | 0.15 |
| Discount | 0.13 |
| Holiday | 0.07 |
| IsWeekend | 0.05 |
| DayOfWeek | 0.04 |

**Key Finding:** Store_Type was the most influential feature in the model, followed by Location_Type and Discount.

## Business Recommendations

- **Inventory planning:** Use store-level sales forecasts to improve inventory allocation and reduce the risk of overstocking or stockouts.
- **Discount strategy:** Evaluate discount campaigns across store types to understand their impact on sales and improve promotional planning.
- **Store-level planning:** Consider differences in store types when setting sales targets and allocating resources.
- **Holiday planning:** Account for observed holiday-related sales patterns when planning inventory and staffing.
- **Regional strategy:** Use regional sales differences to support location-specific business decisions.

## Model Deployment

The trained XGBoost model was deployed through a Flask web application.

**Deployment workflow:**

1. Saved the trained XGBoost model as `xgb_model.pkl` using Pickle.
2. Saved label encoders as `encoders.pkl`.
3. Developed a Flask application with `/` and `/predict` endpoints.
4. Created an HTML frontend to collect user inputs.
5. Loaded the trained model when the server starts.
6. Processed user inputs and generated real-time sales predictions.

**Sample Prediction**

| Input | Value |
|---|---|
| Store ID | 250 |
| Store Type | S4 |
| Region | R1 |
| Location | L2 |
| Date | 15-Jan-2019 |
| Discount | Yes |
| Holiday | No |
| Predicted Sales | ₹76,824.99 |

The application was hosted on Render's free plan. The initial application load may take approximately 30–50 seconds.

## Project Deliverables

- Tableau dashboard for sales analysis.
- GitHub repository containing project code.
- Technical blog documenting the project.
- Loom video demonstrating the project.
- Flask web application for sales prediction.

## Conclusion

This project demonstrates how machine learning can support retail sales forecasting and business decision-making. Through exploratory data analysis, statistical hypothesis testing, and model comparison, XGBoost Regressor outperformed Linear Regression, achieving an R² score of 0.8145.

The deployed Flask application makes the trained model accessible for generating sales predictions using store and date-related inputs.

The project highlights the practical application of data analysis, statistical testing, machine learning, visualization, and model deployment to address a real-world retail business problem.

---

**Project Author:** Ashwin R  
**GitHub:** [itsashwinr](https://github.com/itsashwinr)  
**Project Category:** Machine Learning | Regression | Retail Analytics
