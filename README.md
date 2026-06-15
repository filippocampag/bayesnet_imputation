# Heart Disease Data: imputation and prediction
**Authors**: Filippo Campagnolo, Giuseppe Pianeti
**Course**: Advanced Machine Learning - Master in Statistical and Economic Methods for Decision Making, University of Turin
**Teacher**: Luciana Dalla Valle
**Academic year**: 2025/2026
## Overview
This project applies machine learning classification algorithms to predict the presence of heart disease using the UCI Heart Disease Dataset. Moving beyond classical predictive analysis, this project heavily focuses on handling Missing Not At Random (MNAR) data across different global clinics using Bayesian Network imputation. 

A comprehensive sensitivity analysis was conducted across five distinct data configurations to test the transferability of the structural distributions learned from complete cases (Cleveland clinic) to incomplete cases (clinics in Hungary, Switzerland, and VA Long Beach).

You can download the data from the [UCI repository](https://archive.ics.uci.edu/dataset/45/heart+disease).
## Repository Structure
The analysis pipeline is split into four sequential R scripts to ensure reproducibility:

1. `data_loading_cleaning.R`: Loads, cleans, and formats the data from the four distinct clinics into five testing scenarios.
2. `data_imputation.R`: Splits the data into train/test sets and imputes missing values using a cross-validated Bayesian Network to minimize reconstruction error.
3. `models_fitting.R`: Fits the five machine learning models (Random Forests, BART, Bayesian Network, Naive Bayes, Tree-Augmented NB) on the imputed data, tuning hyperparameters via nested cross-validation, and evaluates them using Balanced Accuracy.
4. `data_storing.R`: Stores the final model results and performance metrics for reporting.

Please download the data from the [UCI repository](https://archive.ics.uci.edu/dataset/45/heart+disease) and place it in the `data/` folder.