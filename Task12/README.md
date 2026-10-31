# Random Forest Classification

This project demonstrates **Random Forest Classification** using the Breast Cancer Dataset from scikit-learn.

## Objective

The objective of this task is to build a Random Forest classifier and compare its performance with a Decision Tree classifier.

## Dataset

The **Breast Cancer Dataset** is imported directly from `scikit-learn`.

The dataset contains numerical features related to breast cancer cases. The target has two classes:

* Malignant
* Benign

## Models Used

### Decision Tree

A Decision Tree Classifier makes predictions using a tree-like structure based on different conditions in the data.

### Random Forest

Random Forest is an **ensemble learning algorithm** that combines multiple decision trees to make predictions.

Using multiple trees generally makes the model more robust than using a single decision tree.

## Evaluation

Both models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score

The same train-test split is used for both models to make the comparison fair.

## Technologies Used

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook

## Libraries Used

```python
import pandas as pd

from sklearn.datasets import load_breast_cancer
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report
```

## How to Run

Install the required libraries:

```bash
pip install pandas scikit-learn
```

Run the program:

```bash
python random_forest_classification.py
```

## Output

The program displays:

* Dataset information
* Decision Tree accuracy
* Random Forest accuracy
* Classification report for both models
* Best-performing model

The model comparison is also saved as:

## Result

The project demonstrates how **Random Forest**, an ensemble learning algorithm, can be compared with a single **Decision Tree** using the same dataset and evaluation method.
