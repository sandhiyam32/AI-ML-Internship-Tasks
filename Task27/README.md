# Task 27: Handling Class Imbalance

## Objective

Compare a logistic regression classifier before and after applying a class-imbalance treatment. The experiment focuses on the minority-class precision, recall, and F1 score rather than accuracy alone.

## Dataset

`customer_churn.csv` is a deterministic, synthetic customer-churn dataset included with this task. It contains 2,000 customer records and a binary `Churn` target (`0` = stayed, `1` = churned). It is designed for this exercise and does not contain real customer information.

Features include tenure, monthly charges, support calls, contract type, internet service, payment method, and paperless billing.

| Churn | Meaning | Records | Percentage |
|---|---|---:|---:|
| 0 | Stayed | 1,541 | 77.05% |
| 1 | Churned | 459 | 22.95% |

The majority-to-minority ratio is approximately 3.36:1. The notebook calculates these values from the CSV when it runs.

## Imbalance treatment

The notebook compares two logistic regression models:

1. **Baseline:** default class weighting.
2. **Treated:** `class_weight="balanced"`, which weights classes inversely according to their frequency in the training data.

Both models use the same stratified train/test split. Numeric scaling and categorical one-hot encoding are fit only on the training data through a scikit-learn pipeline, preventing preprocessing leakage. The test data is never resampled or used to fit preprocessing or the models.

## Run

Open `churn_class_imbalance.ipynb` in Jupyter Notebook or JupyterLab and run all cells from the `Task27` folder. The notebook requires Python, pandas, NumPy, Matplotlib, and scikit-learn.

## Outputs

The notebook reports the original class distribution, baseline and balanced-model classification metrics, a side-by-side comparison of test-set precision/recall/F1/accuracy, confusion matrices, and a conclusion based on the observed results.

## Result and conclusion

With the included data and notebook's fixed stratified split, the held-out test results are:

| Model | Churn precision | Churn recall | Churn F1 | Accuracy |
|---|---:|---:|---:|---:|
| Baseline | 0.45 | 0.22 | 0.29 | 0.76 |
| Class-weighted | 0.35 | 0.70 | 0.47 | 0.63 |

Balanced class weights substantially improve detection of churners and the churn-class F1 score, but lower precision and overall accuracy. The treatment is useful when missed churners are more costly, though the additional false positives and outreach costs should be considered. These results are specific to this synthetic dataset and split.
