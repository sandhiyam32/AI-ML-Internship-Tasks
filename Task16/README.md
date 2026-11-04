# Precision, Recall and F1 Score

This project evaluates a classification model using Precision, Recall and F1 Score with the Breast Cancer Dataset.

## Objective

The objective of this task is to understand classification evaluation metrics beyond simple accuracy and compare their performance.

## Dataset

The Breast Cancer Dataset is imported directly from Scikit-learn.

It contains numerical features related to breast cancer cases.

The dataset has two classes:

- Malignant
- Benign

## Model Used

Logistic Regression is used to train the classification model.

Feature scaling is performed using StandardScaler before training.

## Evaluation Metrics

### 1. Precision

Precision measures how many predicted positive cases are actually positive.

### 2. Recall

Recall measures how many actual positive cases are correctly identified.

### 3. F1 Score

F1 Score is the harmonic mean of Precision and Recall.

## Steps Performed

1. Imported the Breast Cancer Dataset.
2. Split the dataset into training and testing sets.
3. Scaled the numerical features.
4. Trained a Logistic Regression model.
5. Predicted the test data.
6. Calculated Precision, Recall and F1 Score.
7. Displayed the classification report.
8. Visualized the evaluation metrics.
9. Generated a confusion matrix.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib

## How to Run

Install the required libraries:

```bash
pip install pandas scikit-learn matplotlib
```

Run the program:

```bash
python precision_recall_f1.py
```

## Output

The program displays:

- Precision Score
- Recall Score
- F1 Score
- Classification Report
- Performance Metrics Graph
- Confusion Matrix


## Result

The classification model is evaluated using Precision, Recall and F1 Score. Graphical visualizations help compare the metrics and understand the model's classification performance.