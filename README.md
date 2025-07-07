# Mortgage Loan Approval Analysis Using Machine Learning in R

## Overview

This project analyzes a large-scale mortgage loan dataset to determine the key factors influencing loan approval decisions in the United States post-COVID-19. Using the **Home Mortgage Disclosure Act (HMDA)** dataset and **machine learning models built in R (XGBoost)**, the study explores both financial and demographic predictors of mortgage loan decisions, with a special focus on the feasibility of **reverse mortgage** options for older applicants.


## Project Goals

* Identify the **primary financial and demographic variables** that predict mortgage loan approval or denial.
* Evaluate the **importance of U.S. Census demographic fields** in predicting outcomes.
* Investigate the impact and viability of **Reverse Mortgage** products for elderly borrowers.
* Implement and evaluate **machine learning models** (XGBoost) using R to support decision-making.


## Research Questions

* What are the key predictors for loan approval or denial in the mortgage application process?
* How significant are U.S. Census-based demographic features in influencing loan decisions?
* Can Reverse Mortgage be considered a beneficial option for senior borrowers? How does it affect interest rates and approval chances?


## Literature Review Highlights

* **Deep Learning vs. Robust Regression**: Deep Neural Networks outperformed traditional regression models for predicting loan rates.
* **Loan Closing Delays**: Text mining on discussion forums accurately predicted risks of loan delays.
* **House Prices & Borrowing**: House prices significantly impact household borrowing elasticity.
* **CART for Default Prediction**: Classification trees effectively identified key borrower attributes causing defaults.
* **XGBoost & Random Forest**: Ensemble models like XGBoost outperform traditional methods for mortgage default prediction.

### Tools Used

* **R** programming language
* **RStudio** IDE
* Key libraries: `xgboost`, `dplyr`, `caret`, `ggplot2`

### Data Source

* 2023 Loan Application Register (LAR) from [HMDA](https://ffiec.cfpb.gov)
* 11.4 million+ loan applications across 99 features

### Model Used

* **Extreme Gradient Boosting (XGBoost)** for multi-class classification
* One-hot encoding for categorical variables
* 70/30 train-test data split


## Exploratory Data Analysis (EDA)

* **Top Predictors**: Age, Debt-to-Income Ratio, Income, Property Value, and Occupancy Type.
* **Geographic Trends**: Highest loan approvals in California, denials in Florida.
* **Loan Types by Race**: Conventional loans were preferred by all racial groups; government-backed loans had demographic variance.
* **Reverse Mortgage**: Underused (<0.5% of entries); data sparse and inconclusive.


## Key Results

* **XGBoost Accuracy**: 91.43% on test data

* **Top Features** (Descending):

  1. Age
  2. Debt-to-Income Ratio
  3. Property Value
  4. Income
  5. Occupancy Type
  6. Loan Purpose
  7. Loan Type
  8. Race
  9. Ethnicity
  10. State

* **Census Features**: Found to have **minimal influence**, with top-ranked census field at only position 21 in importance.

## Key Insights

* Financial attributes are **more predictive** than demographics or census information.
* Reverse Mortgage is not significantly influencing interest rate or approval probability due to data scarcity.
* Younger to middle-aged applicants (25–44 years) show higher approval rates.
* Model performance is impacted by **missing values and NotApplicable fields**, often correlated with loan denial.

## Future Work

* Enhance model by exploring **label encoding** and **dimensionality reduction**.
* Expand analysis to include **denial reason** and generate **recommendations** for applicants.
* Integrate additional reverse mortgage data to conduct robust statistical testing.
* Re-label and use more categories from the `action_taken` variable for a broader model.

