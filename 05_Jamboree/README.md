# Jamboree Education – Graduate Admission Prediction

## Project Overview

This project focuses on analyzing the factors that influence graduate admission chances at top universities, particularly Ivy League institutions, from an Indian applicant's perspective.

The objective is to understand the relationship between academic performance, standardized test scores, university ratings, Statement of Purpose (SOP), Letters of Recommendation (LOR), and research experience. A Linear Regression model is developed to estimate an applicant's probability of admission based on these factors.

The project combines exploratory data analysis, statistical analysis, regression modeling, model diagnostics, and regularization techniques to support data-driven admission predictions.

## Business Problem

Jamboree Education helps students prepare for competitive examinations such as GRE, GMAT, and SAT.

To help students better understand their graduate admission prospects, Jamboree introduced a feature that estimates the probability of admission to top universities.

The business challenge is to identify the important factors influencing admission chances and develop a predictive model that estimates admission probability using an applicant's profile.

## Business Objectives

- Identify the key factors influencing graduate admission chances.
- Understand relationships between GRE, TOEFL, CGPA, university ratings, SOP, LOR, and research experience.
- Perform exploratory data analysis to identify patterns and trends.
- Develop a regression model to estimate admission probability.
- Evaluate Linear Regression assumptions and model performance.
- Apply Lasso and Ridge regularization to improve model generalization.
- Provide actionable recommendations for students and Jamboree Education.

## Dataset Description

The project uses the `Jamboree_Admission.csv` dataset.

| Attribute | Details |
|---|---|
| Total records | 500 |
| Original columns | 9 |
| Predictive features | 7 |
| Target variable | Chance of Admit |
| Missing values | None |
| Data types | Integer and Float |

### Dataset Features

| Feature | Description |
|---|---|
| GRE Score | Graduate Record Examination score |
| TOEFL Score | Test of English as a Foreign Language score |
| University Rating | Rating of the applicant's undergraduate university |
| SOP | Statement of Purpose rating |
| LOR | Letter of Recommendation rating |
| CGPA | Undergraduate academic performance |
| Research | Indicates research experience |
| Chance of Admit | Estimated probability of admission |

The `Serial No.` column was removed because it does not provide meaningful predictive information.

## Tools & Technologies

- **Python** – Data analysis and model development
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Exploratory data analysis and statistical visualization
- **Scikit-learn** – Regression models, preprocessing, and evaluation
- **Statsmodels** – Ordinary Least Squares (OLS) regression and statistical summaries
- **SciPy** – Statistical testing
- **Lasso & Ridge Regression** – Regularization techniques

## Methodology

### 1. Data Cleaning and Preprocessing

- Loaded and inspected the admission dataset.
- Examined dataset dimensions, column names, data types, and statistical summaries.
- Checked for missing values and confirmed that all columns had complete records.
- Removed the `Serial No.` column.
- Separated independent variables (features) and the dependent variable (`Chance of Admit`).
- Split the data into training and testing sets.
- Applied StandardScaler to standardize input features for regression analysis.

### 2. Exploratory Data Analysis

Performed univariate and bivariate analysis to understand individual feature distributions and relationships.

Key analysis included:

- GRE and TOEFL score distributions.
- University rating distribution.
- SOP and LOR rating distributions.
- CGPA distribution.
- Relationships between GRE, TOEFL, and CGPA.
- Relationships between academic indicators and admission probability.
- Correlation analysis using a heatmap.

### 3. Key Exploratory Findings

- Higher GRE scores are generally associated with higher admission chances.
- Higher TOEFL scores show a positive relationship with admission probability.
- Applicants with higher CGPA generally have better admission prospects.
- Higher-rated universities tend to be associated with applicants having stronger GRE and TOEFL scores.
- GRE and TOEFL scores show a strong positive relationship.
- Research experience shows a comparatively weaker correlation with admission probability than major academic indicators.
- SOP and LOR ratings show relationships with other applicant profile variables.

### 4. Correlation Analysis

The correlation analysis identified the following relationships with the target variable:

| Feature | Correlation with Chance of Admit |
|---|---:|
| GRE Score | 0.810 |
| TOEFL Score | 0.792 |
| University Rating | 0.690 |
| SOP | 0.684 |
| LOR | 0.645 |
| CGPA | 0.882 |
| Research | 0.546 |

**Key Finding:** CGPA showed the strongest positive correlation with admission probability, followed by GRE and TOEFL scores.

### 5. Regression Model Development

Developed regression models to estimate the probability of admission.

The project explored:

- Linear Regression
- Lasso Regression (L1 Regularization)
- Ridge Regression (L2 Regularization)
- Polynomial Regression

The Ordinary Least Squares (OLS) implementation using Statsmodels was also used to examine model coefficients, statistical significance, R-squared, and adjusted R-squared.

### 6. Linear Regression Model Evaluation

The OLS regression model achieved the following results in the initial model summary:

| Evaluation Metric | Result |
|---|---:|
| R-squared | 0.823 |
| Adjusted R-squared | 0.820 |
| F-statistic | 260.6 |
| Observations | 400 |

The model demonstrated a strong relationship between the selected applicant features and admission probability.

The regression analysis also examined individual feature coefficients and p-values to understand their statistical significance.

### 7. Multicollinearity and Model Diagnostics

Evaluated the assumptions of Linear Regression to assess model reliability.

The analysis covered:

- Linearity
- Independence of observations
- Homoscedasticity
- Normal distribution of residuals
- Multicollinearity

Additional techniques included:

- Variance Inflation Factor (VIF) analysis.
- Residual distribution analysis.
- Shapiro-Wilk test for residual normality.
- Goldfeld-Quandt test for heteroscedasticity.

The Goldfeld-Quandt test returned a p-value of approximately 0.303, providing no strong evidence of heteroscedasticity at the conventional 5% significance level.

### 8. Regularization and Polynomial Regression

Explored polynomial regression with degree 5 to capture potential nonlinear relationships.

The degree-5 polynomial model showed overfitting, with extremely low training error but substantially higher testing error.

To address overfitting, Lasso and Ridge regularization techniques were applied.

| Regularization Model | Training MSE | Testing MSE |
|---|---:|---:|
| Lasso (α = 0.01) | 0.003692 | 0.003729 |
| Ridge (α = 1.0) | 0.003077 | 0.003784 |

Regularization reduced the errors substantially compared with the unregularized degree-5 polynomial model.

## Key Business Insights

- **Academic performance:** CGPA is strongly associated with admission probability and is an important factor to consider.
- **Standardized test scores:** GRE and TOEFL scores show strong positive relationships with admission chances.
- **University ratings:** Applicants with stronger academic profiles tend to be associated with higher-rated universities.
- **Research experience:** Research experience has a positive relationship with admission probability, although its correlation is weaker than several academic indicators.
- **Interrelated factors:** GRE, TOEFL, and CGPA are positively correlated, indicating that applicant characteristics are interconnected.

## Business Recommendations

- **Improve academic performance:** Students should focus on maintaining a strong CGPA throughout their undergraduate studies.
- **Prepare for standardized tests:** Jamboree can help students improve GRE and TOEFL scores through practice tests, mock examinations, and structured preparation.
- **Strengthen university selection:** Use university ratings and applicant profiles to support more informed university shortlisting.
- **Improve admission guidance:** Incorporate the important admission factors into Jamboree's website-based admission probability feature.
- **Provide personalized insights:** Use predictive analysis to help students understand how their academic and examination profiles relate to admission chances.

## Conclusion

This project demonstrates how exploratory data analysis and regression techniques can be applied to understand and predict graduate admission chances.

The analysis identified CGPA, GRE scores, and TOEFL scores as important indicators associated with admission probability. Linear Regression provided a useful predictive approach, while statistical diagnostics helped evaluate its assumptions and reliability.

The project also explored polynomial regression and Lasso and Ridge regularization, highlighting the importance of controlling overfitting and improving model generalization.

The findings can help Jamboree Education provide more informed admission guidance and support students in identifying areas where they can strengthen their applications.

---

**Project Author:** Ashwin R  
**GitHub:** [itsashwinr](https://github.com/itsashwinr)  
**Project Category:** Exploratory Data Analysis | Statistical Analysis | Linear Regression | Predictive Modeling
