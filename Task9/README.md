# Task 9 – Feature Scaling

## Description

This task demonstrates **Feature Scaling** using the Iris Dataset.

Two scaling techniques are used:

* StandardScaler
* MinMaxScaler

## Dataset

Iris Dataset from Scikit-learn.

```python
from sklearn.datasets import load_iris
```

## Tools Used

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook

## What I Did

1. Loaded the Iris dataset from Scikit-learn.
2. Applied StandardScaler.
3. Applied MinMaxScaler.
4. Compared the original and scaled values.
5. Compared the value ranges.

## StandardScaler

StandardScaler transforms the data so that the values are centered around 0 with a standard deviation of 1.

## MinMaxScaler

MinMaxScaler transforms the values into a range between 0 and 1.

## Key Learning

Feature scaling is important because different features may have different ranges. Scaling helps many Machine Learning algorithms work better with the data.

## Conclusion

In this task, I learned how to apply StandardScaler and MinMaxScaler to numerical features and compare the transformed data.
