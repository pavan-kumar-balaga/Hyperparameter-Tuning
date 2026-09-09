# Hyperparameter Tuning Project

This project demonstrates hyperparameter tuning of a Random Forest classification model using Grid Search and cross-validation.

## Folder Structure
```text
hyperparameter-tuning/
├── README.md
|── Hyperparameter_Tuning_Report.md
|── hyperparameter_tuning.ipynb
```

## Work Completed
- Loaded and cleaned the supplied dataset.
- Handled missing values.
- One-hot encoded categorical features.
- Split data into 80% training and 20% testing sets.
- Built a Random Forest classifier.
- Applied GridSearchCV with 3-fold cross-validation.
- Tuned `max_depth` and `min_samples_split`.
- Selected the best hyperparameters using validation accuracy.
- Evaluated the final tuned model on unseen test data.

## Notebook
The notebook is already executed and includes its outputs. To reproduce it in Google Colab, upload the notebook and the supplied CSV dataset to the Colab session, then run the cells.
