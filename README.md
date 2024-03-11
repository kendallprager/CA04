CA04 - Ensemble Models
Overview

This assignment focuses on building and evaluating ensemble machine learning models, specifically Random Forest, AdaBoost, Gradient Boost, and XGBoost classifiers. The goal is to understand the impact of the n_estimators hyperparameter on model performance, specifically in terms of accuracy and AUC (Area Under the ROC Curve).
Dataset

The dataset is sourced from the Census Bureau and encompasses demographic information along with salary data, divided into two classes ('>50K' and '<=50K'). It includes:

    Number of target classes: 2
    Labels: 1 ('>50K'), 0 ('<=50K')
    Number of attributes (Columns): 7
    Number of instances (Rows): 48,842

The dataset can be accessed at the following URL: census_data.csv.

A specific column indicates which rows are to be used for training and testing. You will need to programmatically separate these into training and testing datasets.
Assignment Tasks

    Data Preparation: Re-use the data cleaning and transformation code from CA03. No DQA is needed as it was completed in the previous assignment.

    Hyperparameter Tuning: Determine the optimal value for the n_estimators hyperparameter by plotting:
        Accuracy vs. n_estimators
        AUC vs. n_estimators

    Random Forest Model: Train a Random Forest model using the specified range of n_estimators values. Analyze the model's behavior and identify an optimal n_estimators value.

    Boosting Models: Repeat the process for AdaBoost, Gradient Boost, and XGBoost classifiers. Determine the optimal n_estimators value for each.

    Performance Comparison: Compile the best accuracy and AUC values for each of the four models into a comparison table.

    Observations and Conclusions: Provide insights on the classifiers' behavior with respect to the number of estimators and identify the optimal estimator values within the given range.
