# Data 712 - Homework 7

## Overview

This project applies multilevel count data models to the **Diabetes Health Indicators Dataset** to analyze the number of mentally unhealthy days (`ment_hlth`). The analysis explores both individual-level predictors (e.g., high blood pressure, age, physical activity) and group-level variation based on income levels.

Standard count models (Poisson, Negative Binomial) are compared to multilevel variants that account for unobserved heterogeneity across income brackets. This approach enhances model fit and provides deeper insights into mental health disparities.

## Objectives

- Clean and prepare health survey data
- Model count outcomes using Poisson and Negative Binomial regression
- Test for overdispersion and justify model selection
- Implement multilevel models using `glmmTMB`
- Compare models using AIC/BIC and interpret fixed/random effects
- Visualize income-level variation in mentally unhealthy days

## Dataset

**Name:** Diabetes Health Indicators  
**Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset)  
**File:** `Diabetes Health Indicators.csv`

The dataset includes over 250,000 observations from the U.S. Behavioral Risk Factor Surveillance System (BRFSS), with features related to physical and mental health, demographics, and health behaviors.

## Key Takeaways

- **Overdispersion** was detected, making Negative Binomial models more appropriate than Poisson.
- **Physical activity** was associated with significantly fewer mentally unhealthy days.
- **High blood pressure** increased the number of unhealthy days across models.
- Multilevel models revealed **income-based heterogeneity**, supporting targeted intervention strategies.
- **Standardized age** (`age_z`) improved convergence and interpretability in multilevel models.

## Tools & Packages Used

- `tidyverse`  
- `janitor`  
- `lme4`, `glmmTMB` (for multilevel models)  
- `MASS`, `AER` (for overdispersion and NB models)  
- `texreg`, `broom.mixed` (for model summary and visualization)  
- R Markdown with **rmdformats::material** theme


## RPubs Link
https://rpubs.com/data-jesse/1291226
