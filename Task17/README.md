# ROC Curve and AUC

This task evaluates a binary classification model using a Receiver Operating Characteristic (ROC) curve and Area Under the Curve (AUC).

## Objective

Understand how well a classification model distinguishes between two classes at different decision thresholds.

## Dataset and Model

- **Dataset:** `breast_cancer.csv` (Breast Cancer Wisconsin dataset)
- **Model:** Logistic Regression
- **Positive class:** Malignant

The features are scaled before training, and the dataset is split into training and testing sets.

## Metrics

- **ROC curve:** Shows the true positive rate against the false positive rate across thresholds.
- **AUC:** Summarizes the ROC curve as a single value. A higher AUC indicates stronger class separation.

## Requirements

Install the required libraries:

```bash
pip install pandas scikit-learn matplotlib
```

## Run

Keep `breast_cancer.csv` in the same folder as `roc_auc.ipynb`. Open the notebook in Jupyter Notebook or VS Code and run the cells from top to bottom. The notebook prints the AUC score and displays the ROC curve.
