# Task 25 – Clustering Evaluation with Silhouette Score

## Objective

Compare K-Means clustering configurations without labeled targets. The program standardizes the customer features, calculates the silhouette score for multiple values of K, selects the highest-scoring configuration, and creates a comparison chart.

## Dataset

`Mall_Customers.csv` contains 36 sample customer records. The analysis uses `AnnualIncome_kUSD` and `SpendingScore`. `CustomerID` is an identifier and is not used as a clustering feature.

## Requirements

Python 3.9 or later, plus:

```bash
pip install pandas scikit-learn matplotlib
```

## Run

From this folder:

```bash
python silhouette_evaluation.py
```

The program prints scores for K=2 through K=10, marks the highest-scoring configuration, saves `silhouette_scores.png`, and displays the chart. To save the chart without opening a window:

```bash
python silhouette_evaluation.py --no-show
```

You can set a different K range or CSV path:

```bash
python silhouette_evaluation.py --min-k 2 --max-k 8 --data Mall_Customers.csv --no-show
```

The CSV must include `AnnualIncome_kUSD` and `SpendingScore` columns.

## How to interpret the result

The silhouette score ranges from -1 to 1. A higher score generally means samples are closer to their assigned cluster than to neighboring clusters. A low or negative score can indicate overlapping or poorly separated clusters. The highest score in the tested range is a useful selection guide, not proof that the configuration is best for every use case.

Silhouette evaluation is an internal clustering measure: it compares distances in the feature space and does not require known labels. It is different from classification evaluation, which compares predictions against target labels.

## Run the Jupyter notebook

Open silhouette_evaluation.ipynb in Jupyter Notebook or JupyterLab with Mall_Customers.csv in the same folder, then run all cells from top to bottom. The notebook displays the score table and comparison chart and saves silhouette_scores.png in the folder.


The notebook searches the current folder and common Task25 parent-folder locations for the CSV, so it can be opened from Jupyter started in the project folder or the Task25 folder.
