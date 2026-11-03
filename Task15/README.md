# Model Performance Comparison

This project compares the performance of four different classification algorithms using the Iris Dataset.

## Objective

The objective is to train multiple classification models on the same dataset and compare their performance using different evaluation metrics.

## Dataset

The **Iris Dataset** is imported directly from `scikit-learn`.

It contains information about three types of iris flowers:

* Setosa
* Versicolor
* Virginica

## Models Used

* Logistic Regression
* Decision Tree
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)

## Evaluation Metrics

The models are compared using:

* Accuracy
* Precision
* Recall
* F1 Score

The model with the highest accuracy is selected as the best-performing model.

## Steps Performed

1. Load the Iris Dataset.
2. Split the data into training and testing sets.
3. Train four classification models.
4. Predict the test data.
5. Calculate performance metrics.
6. Compare the models.
7. Display an accuracy comparison graph.
8. Select the best-performing model.


## Technologies Used

* Python
* Pandas
* Scikit-learn
* Matplotlib

## How to Run

Install the required libraries:

```bash
pip install pandas scikit-learn matplotlib
```

Run the program:

```bash
python model_performance_comparison.py
```

## Output

The program displays:

* Model performance comparison table
* Accuracy
* Precision
* Recall
* F1 Score
* Best-performing model
* Accuracy comparison graph

The comparison results are saved as:

```text
model_comparison_results.csv
```


## Conclusion

The performance of four classification algorithms is compared using the same dataset and test data. The model with the best evaluation performance is selected as the final model.
