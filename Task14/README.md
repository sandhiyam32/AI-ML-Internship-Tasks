# Support Vector Machine (SVM) Classification

A simple SVM program that predicts breast cancer classes using the built-in Breast Cancer dataset from scikit-learn.

## What the program does

1. Loads the dataset and splits it into training and testing data.
2. Scales the features and trains an SVM classifier.
3. Prints the accuracy and classification report.
4. Displays a confusion-matrix graph.

Feature scaling is used because SVM works with distances between data points.

## Requirements

* Python 3
* Jupyter Notebook
* pandas
* scikit-learn
* matplotlib

Install the packages:

```bash
python -m pip install pandas scikit-learn matplotlib notebook
```

## Run

Open `support_vector_machine_classification.ipynb` in Jupyter Notebook or Visual Studio Code and choose **Run All**.

The dataset is downloaded from scikit-learn in the notebook; no separate CSV file is required.

> This is an educational example and is not intended for medical diagnosis.
