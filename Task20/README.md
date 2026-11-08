# Grid Search Cross-Validation

This task uses `GridSearchCV` to select Random Forest hyperparameters with
cross-validation on the training data.

## Objective

Practice defining a parameter grid, using stratified cross-validation to
compare candidate settings, and reporting the best parameters and mean
cross-validation accuracy without using the test set for model selection.

## Dataset and model

- **Dataset:** `iris.csv`, the Iris flower dataset
- **Features:** Sepal length, sepal width, petal length, and petal width
- **Target:** Iris species
- **Model:** `RandomForestClassifier`

The notebook makes a stratified 80/20 train-test split. `GridSearchCV` fits
only on the training split, using five shuffled stratified folds. It reports
the best hyperparameters, the best mean cross-validation accuracy, and the
accuracy of the selected model on the held-out test split.

With the included data and fixed random seeds, the best parameters are
`{'max_depth': None, 'min_samples_split': 5, 'n_estimators': 50}` and the
best mean cross-validation accuracy is **0.9667**. The held-out test accuracy
is **0.9667**.

## Parameter grid

| Hyperparameter | Values |
|---|---|
| `n_estimators` | `50`, `100` |
| `max_depth` | `None`, `5` |
| `min_samples_split` | `2`, `5` |

This grid evaluates eight combinations with five folds per combination.

## Requirements

```bash
pip install pandas scikit-learn jupyter
```

## Run

Open `grid_search_cross_validation.ipynb` in Jupyter Notebook or VS Code and
run all cells from top to bottom. Keep `iris.csv` in the same folder as the
notebook when possible. If the CSV is not found, the notebook loads the
equivalent built-in Iris dataset from scikit-learn. The test set is used only
for the final evaluation, not for tuning.
