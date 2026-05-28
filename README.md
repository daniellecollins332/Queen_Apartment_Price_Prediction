
# Queens, NY Apartment Price Prediction
 
> Predicting apartment sale prices in Queens, NY using three machine learning models, benchmarked against Zillow's Zestimate (2.3% median absolute error target).
 
---
 
## Table of Contents
 
- [Overview](#overview)
- [Data](#data)
- [Models](#models)
- [Results](#results)
- [Tech Stack](#tech-stack)
- [Course Context](#course-context)
---
 
## Overview
 
This project uses a dataset of condo and co-op sales in Queens, NY (Feb 2016 – Feb 2017) collected via Amazon MTurk. The data is raw and messy — a significant portion of the work involved cleaning, featurizing, and handling missingness before any modeling could begin.
 
### Goals
- Build and compare three ML models to predict apartment sale prices
- Perform rigorous data cleaning and feature engineering on raw MTurk data
- Evaluate out-of-sample performance against Zillow's Zestimate benchmark
---
 
## Data
 
- **Source:** `housing_data_2016_2017.csv`
- **Scope:** Condos and co-ops in select Queens zip codes, sales up to $1M
- **Collection:** Amazon MTurk — raw, required extensive cleaning
### Key Preprocessing Steps
- Missing data imputation and error correction
- Feature engineering from raw MTurk fields
- Outlier detection and removal
---
 
## Models
 
### Regression Tree
Single decision tree trained on cleaned housing data. Top 10 most important features visualized via variable importance plot. Prone to overfitting — serves as a complexity baseline.
 
### OLS Linear Regression
Baseline linear model used to interpret feature coefficients and establish a performance floor before ensemble methods.
 
### Random Forest
Primary production model. Out-of-bag (OOB) error used for out-of-sample validation without a separate test set. Best overall performance.
 
---
 
## Results
 
| Model | In-Sample R² | In-Sample RMSE | OOS R² | OOS RMSE | Normalized RMSE |
|---|---|---|---|---|---|
| Regression Tree | 0.9652 | $32,941 | 0.5730 | $112,756 | 0.3615 |
| OLS Linear | 0.8511 | $68,156 | 0.7849 | $80,697 | 0.2587 |
| Random Forest | 0.9496 | $39,672 | 0.7950 | $79,221 | 0.2540 |
 
> **Best model:** Random Forest — OOS RMSE of $79,221 (Normalized RMSE: 0.2540). While Zillow's Zestimate benchmark was not surpassed, results are strong given the constraints of the dataset — raw MTurk-collected data with significant missingness and a narrow geographic and price-range scope.
 
---
 
## Tech Stack
 
| Tool | Purpose |
|---|---|
| R | Primary language |
| `randomForest` | Random forest model |
| `rpart` | Regression tree |
| `ggplot2` | Visualization |
| `dplyr` | Data wrangling |
 
---
 
## Course Context
 
Final project for **MATH 342W** — Data Science via Machine Learning, Queens College CUNY (Prof. Kapelner).
 
---
 
---
 
