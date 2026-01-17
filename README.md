# 🏥 Health Insurance Pricing Audit: Smoking × BMI Risk
## 📌 Project Overview

This project is a diagnostic data analysis of health insurance pricing, focused on understanding why smokers with high BMI (obese smokers) are priced significantly higher than other customers.

The goal is to audit existing pricing logic, identify true risk drivers, and propose simple, fair, and data-driven pricing adjustments that align premiums with actual observed risk.

This analysis combines Excel, Python, and Tableau to move from raw data exploration to business-ready insights and recommendations.

## 🎯 Business Objective

Health insurance pricing often treats smokers as a uniformly high-risk group.
This project investigates whether that assumption is valid.

Key questions addressed:

-- Are all smokers equally expensive?

-- Does BMI interact with smoking status to amplify risk?

-- Is there a clear “cost cliff” where charges increase sharply?

-- How can pricing be adjusted to better reflect actual risk?


## 📊 Dataset📊 Dataset Description

The dataset contains health insurance beneficiary data with the following key variables: Description

The dataset contains health insurance beneficiary data with the following key variables:

| Column   | Description               |
| -------- | ------------------------- |
| age      | Age of the beneficiary    |
| bmi      | Body Mass Index           |
| smoker   | Smoking status (Yes/No)   |
| sex      | Gender                    |
| region   | Geographic region         |
| children | Number of dependents      |
| charges  | Medical insurance charges |


## Analysis

### Phase 1: Data Cleaning & Feature Engineering

Converted categorical variables to proper types

Created:

- Smoker_Binary

- BMI_Category

- BMI × Smoker interaction term

Prepared data for modeling and visualization

### Phase 2–3: Exploratory & Diagnostic Analysis

Visualized BMI vs charges using scatter plots

Compared cost distributions using boxplots

Calculated average charges by:

- Smoking status

- BMI category

Identified a sharp cost increase for smokers after BMI ≥ 30

### Phase 4: Pricing Logic Diagnosis (Regression)

Built two regression models:

- Baseline model: No interaction

- Interaction model: Includes BMI × Smoker term

Key finding:
- Smoking alone is not the primary driver — obesity magnifies smoking-related risk


### Phase 5: Pricing Recommendation

Proposed simple risk multipliers:

| Segment          | Proposed Multiplier |
| ---------------- | ------------------- |
| Non-smoker       | 1.0                 |
| Smoker, BMI < 30 | ~1.1                |
| Smoker, BMI ≥ 30 | 1.8–2.2             |


Simulated adjusted charges

Highlighted fairness and business impact

### Phase 6: Visualization & Communication

Built an interactive Tableau dashboard showing:

- Cost cliff at BMI 30

- Distribution differences by segment

- KPI cards for executive clarity

Designed slides for non-technical stakeholders

## 🔍 Key Insights

- Smoking alone does not explain high insurance costs

- Obesity dramatically amplifies smoking-related risk

- Costs remain relatively stable until BMI ≥ 30, after which smoker charges spike sharply

- Current pricing risks overcharging low-risk smokers

- Tiered pricing better reflects actual cost drivers

## 📈 Tools Used

1. Excel
Initial data review and sanity checks

2. Python
- Pandas & NumPy for data preparation
- Statsmodels for regression analysis

4. Tableau
Interactive dashboards and visual storytelling

5. Canva / PowerPoint
Executive-ready presentation slides

## 📬 Contact

### Author: Fabian Ndung'u
#### Focus Areas: Data Analysis, Data Science, Pricing Analytics, Business Intelligence

Feel free to explore the repo, review the dashboard, or reach out for feedback or collaboration.