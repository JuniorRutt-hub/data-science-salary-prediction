# data-science-salary-prediction

##  Overview

This project uses data-driven models to analyze and predict salary ranges for data science roles based on key job and company attributes. The goal is to help organizations offer competitive compensation and support data-driven hiring strategies in a growing and competitive tech labor market.

## Objectives

- Predict data science salaries using structured datasets from real job listings.
- Identify which factors most strongly influence compensation (e.g., remote ratio, experience, company size).
- Provide actionable insights to support fair and competitive hiring.

## Business Context

Companies often struggle to structure competitive salary packages, resulting in challenges like:
- High recruitment costs from poor compensation alignment
- Reduced offer acceptance and employee retention
- Difficulty in benchmarking across job types and geographies

Our model enables HR teams and hiring managers to design smarter salary structures tailored to role, company size, and region.

## Dataset

- **Source**: [Kaggle – Data Science Salaries 2023](https://www.kaggle.com/datasets)
- **Records**: 3,755 job listings
- **Attributes**:
  - `Experience Level`, `Job Title`, `Remote Ratio`, `Company Size`, `Location`, `Salary (USD)`

## Methodology

### Data Preprocessing
- Removed redundant columns
- Handled missing values and outliers
- Converted dates and normalized salary formats

### Modeling
- Exploratory Data Analysis (EDA)
- Built and compared regression models: `Lasso`, `Support Vector Regression (SVR)`, and `CatBoost`
- Evaluated with `RMSE` and `R²` scores
- Used SHAP for feature importance visualization

### NLP Feature Engineering
- Applied **Sentiment Analysis**, **NER**, and **POS Tagging** on job descriptions and host introductions
- Extracted 180+ new features to capture soft attributes (like company culture, tone, etc.)

## Key Results

- **CatBoost Model R²** improved from **0.693** to **0.715** using NLP-enhanced attributes
- Features such as location, company size, and job title had the highest impact on predicted salaries
- Visualized feature importance using SHAP values to explain model predictions


## Insights

- NLP-derived features (tone, amenities, descriptions) improve salary prediction accuracy
- Remote work flexibility, company size, and experience level are top predictors of compensation
- This model can support salary planning, offer structuring, and HR analytics
