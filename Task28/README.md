# Task 28: Scikit-learn Pipeline

## Objective

Combine missing-value handling, categorical encoding, numeric scaling, and model training into one reproducible scikit-learn workflow. The evaluation uses a held-out test set; the preprocessing steps are fitted only on the training data.

## Dataset

`titanic.csv` contains 891 passenger records from the Titanic dataset. The target is `survived` (`0` = did not survive, `1` = survived). The input features are passenger class, sex, age, family counts, fare, embarkation port, and whether the passenger was alone.

The bundled CSV is a reduced version of the Titanic dataset published in the [seaborn-data repository](https://github.com/mwaskom/seaborn-data/blob/master/titanic.csv). The notebook handles missing age and embarkation values in its pipeline.

## Pipeline

- Numeric features: median imputation followed by standard scaling.
- Categorical features: most-frequent imputation followed by one-hot encoding.
- Classifier: logistic regression.
- Split: stratified 80/20 train/test split with a fixed random seed.

## Run

Open `titanic_pipeline.ipynb` in Jupyter Notebook, JupyterLab, or VS Code and run all cells. Install the requirements if needed:

```bash
pip install pandas scikit-learn jupyter
```

The notebook reports accuracy, precision, recall, F1 score, a classification report, and a confusion matrix on the held-out test data.

## Evaluation results

With the included dataset and fixed stratified split, the test-set results were:

| Metric | Score |
|---|---:|
| Accuracy | 0.816 |
| Precision (survived) | 0.810 |
| Recall (survived) | 0.681 |
| F1 score (survived) | 0.740 |

Confusion matrix (rows are actual labels; columns are predicted labels):

|  | Predicted: did not survive | Predicted: survived |
|---|---:|---:|
| Actual: did not survive | 99 | 11 |
| Actual: survived | 22 | 47 |

The results demonstrate the complete pipeline on one held-out split; different library versions may cause small score changes.
