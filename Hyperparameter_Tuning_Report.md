# Hyperparameter Tuning Report

## 1. Objective
The objective was to optimize a machine learning model by testing different hyperparameter combinations and selecting the configuration that produced the best validation performance.

## 2. Dataset
The supplied dataset contains customer and campaign information from a bank marketing problem. The prediction target is **deposit**, indicating whether the customer subscribed to a term deposit.

Preprocessing included median imputation for numerical missing values, mode imputation for categorical missing values, one-hot encoding of categorical predictors, and an 80/20 stratified train-test split.

## 3. Model and Tuning Method
A **Random Forest Classifier** was selected. Grid Search systematically evaluated the following settings using 3-fold cross-validation:

| Hyperparameter | Values |
|---|---|
| `n_estimators` | 100, 200 |
| `max_depth` | 10, 20, None |
| `min_samples_split` | 2, 5 |

A total of 8 hyperparameter combinations were evaluated.

## 4. Best Configuration
The best configuration was **{'max_depth': 5, 'min_samples_split': 2}**.

Best 3-fold cross-validation accuracy: **0.9007**

Held-out test accuracy: **0.8984**

## 5. Results
The tuned model was evaluated on the test set only after hyperparameter selection. The executed notebook contains the complete classification report and confusion matrix.

The tuning process shows how tree depth, number of trees, and minimum split size can affect the balance between model complexity, stability, and generalization.

## 6. Conclusion
Grid Search provided a systematic and reproducible method for selecting Random Forest hyperparameters. Cross-validation reduced dependence on a single validation split, while the separate test set provided an unbiased final performance check.
