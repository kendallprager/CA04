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
    With the output you've provided in the screenshot, we can see the accuracy and AUC for four different classifiers: Random Forest, AdaBoost, Gradient Boost, and XGBoost. Based on the provided table, here are some observations and conclusions about the behavior of the classifiers concerning the number of estimators and the possible optimal values within the tested range:
Observations:

    Random Forest:
        The Random Forest model shows a good balance between accuracy and AUC, but it does not have the highest values in this output. This suggests that it benefits from the number of estimators but perhaps up to a certain point. Appears to have a peak in AUC around 400 estimators. Accuracy fluctuates, suggesting a complex relationship between the number of estimators and accuracy. The AUC graph suggests around 400 might be optimal, but this isn't definitive without knowing if the trend continues beyond 500.


    AdaBoost:
        AdaBoost has higher accuracy compared to Random Forest but a similar AUC. This indicates that while it may be predicting the classes more correctly, its ability to rank predictions isn't vastly improved. Accuracy is stable across the range of estimators, while AUC is high at a low number of estimators and then decreases slightly but remains fairly stable. Since performance doesn't seem to improve with more estimators, the optimal value might be at the lower end, as low as 50, which achieves high AUC and accuracy.

    Gradient Boost:
        Gradient Boost has the highest accuracy among the models listed but doesn't have the highest AUC. This could suggest that Gradient Boosting is very sensitive to the number of estimators for accuracy, but increasing the number of estimators does not linearly improve its ranking capability as much. Accuracy decreases with more estimators, while AUC increases initially and then plateaus, suggesting an optimal range might be around 200-300 estimators. The optimal range could be around 200-300 estimators, balancing the increase in AUC with a decrease in accuracy.

    XGBoost:
        XGBoost shows a slightly lower accuracy compared to the other boosting methods but has the highest AUC. This suggests that XGBoost might be more effective at ranking predictions correctly, which can be especially beneficial in imbalanced classification problems. The optimal number of estimators for XGBoost is likely at the lower end of the range. An optimal number of estimators is likely at the lower end of the range due to the decrease in both accuracy and AUC with more estimators.
