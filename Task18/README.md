# K-Fold Cross-Validation

This task compares the accuracy of a classification model evaluated with one 80/20 train-test split against its accuracy across five cross-validation folds.

## Objective

Understand why evaluating a model on several different subsets of the data provides a more reliable performance estimate than relying on a single train-test split.

## Dataset and Model

- **Dataset:** `iris.csv`, containing the Iris dataset from Scikit-learn
- **Features:** Sepal length, sepal width, petal length, and petal width
- **Target:** Iris species
- **Model:** Logistic Regression with feature scaling

The notebook uses a stratified train-test split and `StratifiedKFold` with five shuffled folds. Stratification preserves the class proportions in each split, while shuffling with a fixed random seed makes the results reproducible.

## Evaluation

The notebook reports:

- Accuracy for the single 80/20 train-test split
- Accuracy for each of the five cross-validation folds
- Mean and standard deviation of the cross-validation scores

The mean summarizes performance across the folds. The standard deviation indicates how much the result varies depending on which samples are used for validation.

## Requirements

Install the required libraries:

```bash
pip install pandas scikit-learn jupyter
```

## Run

Open `k_fold_cross_validation.ipynb` in Jupyter Notebook or VS Code, and run all cells from top to bottom. Keep `iris.csv` in the same folder as the notebook.
