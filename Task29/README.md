# Task 29: ColumnTransformer Preprocessing

## Objective

Build a preprocessing workflow that handles numerical and categorical columns separately with scikit-learn's `ColumnTransformer`.

## Dataset

`titanic.csv` contains 891 passenger records and 9 columns. The target is `survived` (`0` = did not survive, `1` = survived). The input features include passenger class, sex, age, family counts, fare, embarkation port, and whether the passenger was alone. Some age and embarkation values are missing, so the notebook demonstrates imputation.

The CSV is a reduced version of the Titanic dataset published in the [seaborn-data repository](https://github.com/mwaskom/seaborn-data/blob/master/titanic.csv).

## Preprocessing and evaluation

- Numerical features: median imputation followed by `StandardScaler`.
- Categorical features: most-frequent imputation followed by `OneHotEncoder`.
- `ColumnTransformer` applies the matching preprocessing to each feature group.
- A `Pipeline` combines preprocessing with logistic regression.
- A stratified 80/20 train/test split keeps preprocessing fitted on training data only.
- The notebook reports accuracy, precision, recall, F1 score, a classification report, and a confusion matrix on the held-out test data.

## Run

Open `column_transformer_preprocessing.ipynb` in Jupyter Notebook, JupyterLab, or VS Code, with `Task29` as the working folder, and run all cells. Install the requirements if needed:

```bash
pip install pandas scikit-learn jupyter
```

## Key learning

`ColumnTransformer` makes it possible to define independent transformations for different column types, while a `Pipeline` ensures that preprocessing and model fitting stay together and avoid data leakage.
