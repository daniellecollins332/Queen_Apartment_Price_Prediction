## Queens, NY Apartment Price Prediction
Predicting apartment sale prices in Queens, NY using three machine learning models, benchmarked against Zillow's Zestimate (2.3% median absolute error target).
Overview
This project uses a dataset of condo and co-op sales in Queens, NY (Feb 2016 – Feb 2017) collected via Amazon MTurk. The data is raw and messy — a significant portion of the work involved cleaning, featurizing, and handling missingness before any modeling.
Models Built
ModelDescriptionRegression TreeSingle decision tree; top 10 features visualizedOLS Linear RegressionBaseline linear model with coefficient interpretationRandom ForestPrimary production model; OOB error used for validation
Results
ModelIn-Sample R²OOB / Out-of-Sample RMSERegression Tree——OLS——Random Forest——

Results to be filled in upon project completion.

Data

Source: housing_data_2016_2017.csv
Scope: Condos and co-ops in select Queens zip codes, sales up to $1M
Collected via Amazon MTurk — raw, requires extensive cleaning

Key Steps

Missing data imputation and error correction
Feature engineering from raw MTurk fields
Model training, tuning, and comparison
Out-of-sample validation against Zillow benchmark

Tech Stack

Language: R
Libraries: randomForest, rpart, ggplot2, dplyr

Course Context
Final project for MATH 342W — Data Science via Machine Learning, Queens College CUNY (Prof. Kapelner).
