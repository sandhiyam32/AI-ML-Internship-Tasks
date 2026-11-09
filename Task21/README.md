# Task 21 – Feature Importance Analysis

**Veda Technology – AI & ML Internship | Level 2 – Day 21**

## Description

Train a tree-based model and identify which features contribute most strongly
to its predictions.

## Objective

Understand basic feature importance and model interpretability.

## Tools

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Deliverables

1. Trained tree-based model
2. Feature importance table
3. Feature importance visualization
4. Interpretation

## Hints / Mini Guide

- Use `RandomForestClassifier` or `DecisionTreeClassifier`.
- Access `feature_importances_`.
- Sort features by importance.

## Suggested Dataset

The suggested dataset is the Breast Cancer dataset. The included
`breast_cancer.csv` contains 30 numeric measurement features and a `diagnosis`
target column (`malignant` or `benign`).

## Program

The notebook `feature_importance_analysis.ipynb` trains a Random Forest
classifier, evaluates it on a held-out test set, displays a sorted feature
importance table, plots the top 15 features, and prints an interpretation of
the results.

## Requirements

```bash
pip install pandas scikit-learn matplotlib jupyter
```

## Run

Open `feature_importance_analysis.ipynb` in Jupyter Notebook or VS Code and run
all cells from top to bottom. Keep `breast_cancer.csv` in this folder.
