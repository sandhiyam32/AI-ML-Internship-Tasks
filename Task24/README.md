# Task 24 – Selecting K with the Elbow Method

## Description

This task uses the Elbow Method to choose a suitable number of clusters for
K-Means. It fits models with several values of K, compares their inertia, and
plots the results.

## Dataset

`Mall_Customers.csv` is a compact Mall Customer-style sample with 36 records.
The analysis uses `AnnualIncome_kUSD` and `SpendingScore`; `CustomerID` is an
identifier and is not included in clustering.

## Requirements

```bash
pip install pandas scikit-learn matplotlib
```

## Run the notebook

Open a terminal in the `Task24` folder, start Jupyter with `jupyter notebook`,
then open `elbow_method.ipynb` and run all cells from top to bottom. Keep
`Mall_Customers.csv` in the same folder as the notebook. The notebook loads it
with `pd.read_csv("Mall_Customers.csv")`.

The notebook displays the inertia values and elbow curve inline and saves
`elbow_curve.png` next to the dataset.

## Run the Python script

From this folder, run:

```bash
python elbow_method.py
```

The program prints the inertia for K=1 through K=10, saves the elbow plot as
`elbow_curve.png`, and displays the plot. To save the plot without opening a
window, run:

```bash
python elbow_method.py --no-show
```

## Result and explanation

The selected value is **K=3**. On the standardized features, inertia falls
sharply from about 32.554 at K=2 to 3.364 at K=3, then decreases more gradually
to about 2.680 at K=4. The bend at K=3 indicates that adding more clusters
after that point gives diminishing improvement for this sample.

Inertia measures the sum of squared distances from samples to their assigned
cluster centers. It always decreases as K grows, so the elbow is a practical
trade-off rather than proof that one K is universally best.
