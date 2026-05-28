## Queens, NY Apartment Price Prediction
Predicting apartment sale prices in Queens, NY using three machine learning models, benchmarked against Zillow's Zestimate (2.3% median absolute error target).

### Overview
This project uses a dataset of condo and co-op sales in Queens, NY (Feb 2016 – Feb 2017) collected via Amazon MTurk. The data is raw and messy — a significant portion of the work involved cleaning, featurizing, and handling missingness before any modeling.

### Models Built:-
ModelDescriptions: Single Regression Decision: top 10 features visualized, OLS Linear Regression: Baseline linear model with coefficient interpretation, Random Forest Primary production model: OOB error used for validation

### Results:-

| Model | In-Sample R² | In-Sample RMSE | OOS R² | OOS RMSE | Normalized RMSE |
| Regression Tree | 0.9652 | $32,951 | 0.6350 | $106,073 | 0.3401 |
| OLS Linear | 0.8452 | $69,492 | 0.7831 | $81,510 | 0.2614 |
| Random Forest | 0.9526 | $38,443 | 0.7939 | $79,818 | 0.2559 |

### Data:-

Source: housing_data_2016_2017.csv
Scope: Condos and co-ops in select Queens zip codes, sales up to $1M
Collected via Amazon MTurk — raw, requires extensive cleaning

### Key Steps:-

Missing data imputation and error correction
Feature engineering from raw MTurk fields
Model training, tuning, and comparison
Out-of-sample validation against Zillow benchmark

### Tech Stack:-

Language: R
Libraries: randomForest, rpart, ggplot2, dplyr

### Course Context:-
Final project for MATH 342W — Data Science via Machine Learning, Queens College CUNY (Prof. Kapelner).
