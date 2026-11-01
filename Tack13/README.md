# K-Nearest Neighbors Classification

This project demonstrates **K-Nearest Neighbors (KNN) classification** using the Iris Dataset.

## Objective

The objective of this task is to understand distance-based classification and observe how different values of K affect the performance of a KNN model.

## Dataset

The **Iris Dataset** is imported directly from `scikit-learn`.

It contains measurements of iris flowers and three different flower species:

* Setosa
* Versicolor
* Virginica

## Steps Performed

1. Loaded the Iris Dataset.
2. Split the dataset into training and testing data.
3. Scaled the features using StandardScaler.
4. Tested different K values.
5. Calculated accuracy for each K.
6. Compared the results.
7. Selected the best K value.
8. Plotted K values against accuracy.

## K Values Used

```text
1, 3, 5, 7, 9
```

Odd values are used to reduce the possibility of ties between classes.

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
python knn_classification.py
```

## Output

The program displays:

* Dataset information
* Accuracy for each K value
* K value comparison table
* Best K value
* Accuracy comparison graph

The results are also saved as:

```text
knn_k_comparison.csv
```

## Project Structure

```text
KNN-Classification/
│
├── knn_classification.py
├── knn_k_comparison.csv
└── README.md
```

## Result

The experiment shows how changing the **K value** can affect the accuracy of a KNN classifier. The K value with the highest accuracy is selected as the best K for this experiment.
