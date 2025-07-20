# Yulu Bike Sharing Demand Analysis

![Yulu Bike](flowchart (1).jpg)

### A comprehensive analysis of the factors influencing shared electric cycle demand, leveraging statistical testing and machine learning to drive business strategy.

---

### Table of Contents
1. [Project Overview](#project-overview)
2. [Business Problem](#business-problem)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Key Findings & Insights](#key-findings--insights)
6. [Actionable Recommendations](#actionable-recommendations)
7. [Tools and Libraries](#tools-and-libraries)


---

### Project Overview

This project conducts an in-depth analysis of the Yulu bike-sharing dataset to understand the variables affecting the demand for shared electric cycles. The analysis moves from foundational data exploration and rigorous hypothesis testing to advanced customer segmentation using machine learning. The final output is a set of data-driven, actionable recommendations designed to help Yulu optimize its operations, marketing, and pricing strategies to address a recent decline in revenue.

---

### Business Problem

Yulu, a leading micro-mobility service provider in India, has experienced a significant dip in revenue. They need to understand the key factors that influence the demand for their shared electric cycles to make informed decisions that will boost ridership and stabilize revenue. This analysis aims to answer the core question: **"What are the factors affecting the demand for shared electric cycles in the Indian market?"**

---

### Dataset

The analysis is based on a dataset containing hourly rental data for Yulu bikes. Key attributes include:
- `datetime`: Timestamp of the rental
- `season`: Season of the year (Spring, Summer, Fall, Winter)
- `holiday`: Whether the day is a holiday
- `workingday`: Whether the day is a workday
- `weather`: Weather conditions (Clear, Mist, Light Rain, etc.)
- `temp`: Temperature in Celsius
- `atemp`: "Feels like" temperature in Celsius
- `humidity`: Relative humidity
- `windspeed`: Wind speed
- `count`: Total number of rentals (target variable)

---

### Methodology

The project was structured as a multi-stage data investigation:

1.  **Data Cleaning & Feature Engineering:** The dataset was cleaned, and the `datetime` column was decomposed into more useful features like `hour`, `day_of_week`, `month`, and `year`.

2.  **Exploratory Data Analysis (EDA):** Visualizations were used to uncover initial patterns, such as the bimodal demand peaks on weekdays (commuter traffic) and the strong influence of weather and season on ridership.

3.  **Hypothesis Testing:** A suite of statistical tests was conducted to validate the findings from EDA with a significance level (alpha) of 0.05.
    - **ANOVA:** To test for significant differences in mean rentals across multiple groups (seasons, weather).
    - **Mann-Whitney U Test:** Used as a non-parametric alternative to the T-test to compare rental distributions on working vs. non-working days, as the data was not normally distributed.
    - **Pearson Correlation:** To quantify the strength and direction of the linear relationship between continuous variables (`temperature`, `humidity`) and rental counts.
    - **Chi-Square Test:** To test for a significant association between two categorical variables (season and weather).

4.  **Machine Learning - Clustering:** To move beyond *what* drives demand to *who* is driving it, **K-Means Clustering** was used to segment user sessions into distinct behavioral groups. The optimal number of clusters was determined using the silhouette score.

---

### Key Findings & Insights

The analysis yielded several statistically significant insights across different dimensions:

- **Demand Patterns:**
    - **Weekday vs. Weekend:** Weekdays show a distinct bimodal demand distribution with sharp peaks at **8 AM and 5-6 PM**, indicative of commuter traffic. Weekends show a single, broader peak in the early afternoon, suggesting leisure-based use.
    - **Year-over-Year Growth:** The business showed strong growth, with a **65% increase** in average hourly rentals from 2011 to 2012.

- **Environmental Factors:**
    - **Seasonal Influence:** Demand is highest in the **Fall** and lowest in the **Spring**, with weather being a key contributing factor.
    - **Weather is a Major Driver:** Clear weather conditions see the highest ridership. Temperature has a moderate positive correlation (**r = +0.40**) with demand, while humidity has a moderate negative correlation (**r = -0.32**).

- **Customer Segmentation (from K-Means Clustering):**
    - **Clear User Personas Identified:** The analysis successfully segmented users into three distinct behavioral groups:
        - **Cluster 2 ('High-Demand Midday'):** Averaging **492 rentals/hour**, this group represents peak demand on weekday afternoons in clear weather.
        - **Cluster 0 ('Weekday Warriors'):** The classic commuters, averaging **195 rentals/hour** with sharp peaks at 8 AM and 5-6 PM.
        - **Cluster 1 ('Low-Demand Off-Peak'):** Averaging just **46 rentals/hour**, concentrated in the early mornings with high humidity.

---

### Actionable Recommendations

Based on the findings, the following targeted strategies were proposed:

| Recommendation              | Target Cluster           | Proposed Action                                                                                             |
| --------------------------- | ------------------------ | ----------------------------------------------------------------------------------------------------------- |
| **Dynamic Pricing** | High-Demand Midday       | Implement a **+15% price surge** during peak hours to maximize revenue from high-intent users.              |
| **Loyalty Program** | Weekday Warriors         | Launch a "Commuter Pass" (monthly subscription) to lock in predictable revenue and increase user retention. |
| **Demand Stimulation** | Low-Demand Off-Peak      | Offer targeted **-20% discounts** during early morning hours to improve bike utilization and attract new users. |
| **Inventory Management** | All Clusters             | Proactively reallocate bikes to match the demand patterns of each cluster throughout the day and week.      |

---

### Tools and Libraries

This analysis was conducted in Python, utilizing the following core data science libraries:
- **Pandas:** For data manipulation and analysis.
- **NumPy:** For numerical operations.
- **Matplotlib & Seaborn:** For data visualization.
- **Scikit-learn:** For implementing the K-Means clustering algorithm and data preprocessing (StandardScaler).
- **SciPy:** For conducting the statistical tests.

---


    
