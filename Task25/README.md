# Task 25 – Clustering Evaluation with Silhouette Score

## Objective

Compare K-Means clustering configurations without labeled targets. The notebook standardizes customer features, calculates the silhouette score for K=2 through K=10, selects the highest-scoring K, and plots a comparison chart.

## Dataset

`Mall_Customers.csv` — 36 customer records with three columns:

| Column | Description |
|---|---|
| `CustomerID` | Identifier (excluded from clustering) |
| `AnnualIncome_kUSD` | Annual income in thousands of USD |
| `SpendingScore` | Spending score (1–100) |

## Run

Open `silhouette_evaluation.ipynb` in Jupyter Notebook or JupyterLab with `Mall_Customers.csv` in the same folder, then run all cells top to bottom.

The notebook will:
1. Load and validate the CSV
2. Standardize `AnnualIncome_kUSD` and `SpendingScore` with `StandardScaler`
3. Fit K-Means for each K in the range and compute the silhouette score
4. Print a score table highlighting the best K
5. Save `silhouette_scores.png` and display the bar chart

## Interpreting the result

The silhouette score ranges from -1 to 1. A higher score means samples are better matched to their own cluster than to neighboring clusters. The K with the highest score is a useful starting point, not a definitive answer — domain knowledge should inform the final choice.

Silhouette evaluation is an internal measure: it uses only feature-space distances and requires no ground-truth labels.
