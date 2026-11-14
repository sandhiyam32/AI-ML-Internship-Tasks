# Task 26: Imbalanced Dataset Analysis

## Description
Analyze a classification dataset with imbalanced classes and investigate how class imbalance affects model performance.

## Objective
Understand the problems caused by imbalanced target classes using the Credit Card Fraud Detection dataset.

## Dataset
- **File:** `creditcard.csv`
- **Source:** Credit Card Fraud Detection (Kaggle)
- **Shape:** 284,807 transactions × 31 features
- **Target:** `Class` — 0 (Legitimate), 1 (Fraud)

## Class Distribution
| Class | Count | Percentage |
|-------|-------|------------|
| Legitimate (0) | 284,315 | 99.83% |
| Fraud (1) | 492 | 0.17% |

Imbalance ratio: ~578:1

## Tools Used
- Python, Pandas, Scikit-learn, Matplotlib, Seaborn, Jupyter Notebook

## Notebook Structure
1. **Class Distribution Analysis** — value_counts, bar chart, pie chart
2. **Preprocessing** — StandardScaler on Amount & Time, stratified train-test split
3. **Baseline Model** — Logistic Regression
4. **Metrics** — Accuracy, Precision, Recall, F1 Score + Confusion Matrix
5. **Discussion** — Why accuracy is misleading and how to handle imbalance

## Key Findings
- Accuracy (~99%) is misleading due to severe class imbalance
- Recall on the fraud class is the critical metric — missing fraud is costly
- Precision, Recall, and F1 on the minority class reveal true model performance
- Strategies like SMOTE, undersampling, or `class_weight='balanced'` are needed for improvement

## How to Run
```bash
jupyter notebook imbalanced_dataset_analysis.ipynb
```
