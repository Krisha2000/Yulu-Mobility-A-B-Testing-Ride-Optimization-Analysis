# Yulu – Hypothesis Testing for Micro-Mobility Demand

## Overview

This project explores the demand patterns for Yulu, a leading micro-mobility service provider in India offering shared electric cycles. Yulu has been facing challenges with declining revenue and partnered with a consulting team to analyze key factors influencing the demand for its services.

The goal is to identify and validate which variables significantly impact the rental demand for electric cycles through structured hypothesis testing and statistical analysis.

## Objective

- To determine which factors (e.g., season, weather, working day) significantly affect the number of Yulu electric cycles rented.
- To conduct hypothesis tests and draw actionable insights for business improvement.

## Dataset Description

The dataset includes the following features:

| Column        | Description                                           |
|---------------|-------------------------------------------------------|
| datetime      | Date and time of the record                          |
| season        | Season (1: spring, 2: summer, 3: fall, 4: winter)     |
| holiday       | 1 if it is a holiday, 0 otherwise                     |
| workingday    | 1 if it is a working day, 0 otherwise                 |
| weather       | Weather conditions categorized in multiple levels    |
| temp          | Temperature in Celsius                                |
| atemp         | Apparent (feels-like) temperature in Celsius          |
| humidity      | Humidity percentage                                   |
| windspeed     | Wind speed                                            |
| casual        | Number of casual users                                |
| registered    | Number of registered users                            |
| count         | Total number of users (casual + registered)           |

## Key Questions Addressed

1. Does the number of electric cycles rented vary between working and non-working days?
2. Is there a significant difference in rental count across different seasons?
3. Does the weather condition influence the number of cycles rented?
4. Is weather condition dependent on the season?

## Statistical Methods Used

- **Bi-Variate Analysis**
- **Two-sample t-test**
- **ANOVA (Analysis of Variance)**
- **Chi-Square Test of Independence**
- **Data Visualization for Statistical Assumptions**
    - Histograms
    - Boxplots
    - Q-Q Plots
- **Assumption Testing**
    - Shapiro-Wilk test (Normality)
    - Levene’s test (Homogeneity of variances)

## Steps Followed

1. **Exploratory Data Analysis (EDA)** to understand data structure and feature relationships.
2. **Formulating Hypotheses**:
   - Null Hypothesis (H₀)
   - Alternate Hypothesis (H₁)
3. **Test Assumptions** for each statistical test.
4. **Run Statistical Tests** to validate hypotheses.
5. **Draw Inferences** and derive insights relevant to Yulu’s business problem.

## Insights & Outcome

- Identified key features that significantly impact rental demand.
- Provided data-driven recommendations on how environmental and temporal conditions affect usage.
- Results can help improve pricing, marketing, and inventory planning strategies.

## Tools & Technologies

- Python (pandas, numpy, scipy, statsmodels)
- Data Visualization: matplotlib, seaborn
- Jupyter Notebook

## Conclusion

This project demonstrates how hypothesis testing and structured statistical analysis can help uncover insights in a real-world business scenario. The findings are intended to support strategic decisions at Yulu for improving service efficiency, customer experience, and revenue growth.


