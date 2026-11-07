# Hyperparameter Experimentation

This task explores how selected Random Forest hyperparameters affect classification performance on the Iris dataset.

## Objective

Understand the difference between model parameters and hyperparameters, and observe how changing hyperparameters affects a model's training and test accuracy.

- **Model parameters** are learned from training data during `fit`, such as the split thresholds in a fitted decision tree.
- **Hyperparameters** are chosen before training, such as the number of trees (`n_estimators`) and the maximum tree depth (`max_depth`).

## Dataset and model

- **Dataset:** Iris, loaded from scikit-learn
- **Features:** Four measurements of each flower
- **Target:** Iris species
- **Model:** `RandomForestClassifier`

The notebook uses a stratified 80/20 train-test split with a fixed random seed. Each experiment reuses the same split and changes one hyperparameter at a time.

## Experiments

The notebook compares values of:

- `n_estimators` — number of trees in the forest
- `max_depth` — maximum depth of each tree
- `min_samples_split` — minimum samples required to split a node
- `max_features` — number of features considered when splitting

For each setting, it reports training and test accuracy. Training accuracy helps show whether a setting fits the training data more closely; test accuracy shows performance on held-out data. Test results are for comparison in this exercise; repeatedly choosing settings based on the test set can bias the final estimate. In practice, tune with cross-validation on the training data, then evaluate the selected model on the test set once.

## Run

Install the requirements:

```bash
pip install pandas scikit-learn matplotlib jupyter
```

Open `hyperparameter_experimentation.ipynb` in Jupyter Notebook or VS Code and run all cells from top to bottom.
