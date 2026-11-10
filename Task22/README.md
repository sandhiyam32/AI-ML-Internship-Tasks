# Principal Component Analysis (PCA)

This task standardizes the numerical features in the Iris dataset, transforms
them into principal components, reports explained variance, and visualizes the
first two components.

## Dataset

- **File:** `iris.csv`
- **Samples:** 150 Iris flowers
- **Features:** Sepal length, sepal width, petal length, and petal width
- **Label:** `species` (used only to color the plot; it is not included in PCA)

## Requirements

Install the required libraries with:

```bash
pip install pandas scikit-learn matplotlib notebook
```

NumPy is installed as a dependency of scikit-learn.

## Run

Open `pca_analysis.ipynb` in Jupyter Notebook or VS Code, then run all cells
from top to bottom. The notebook uses `iris.csv` when it can find it. If the
notebook's working directory cannot locate the file, it automatically uses
Scikit-learn's built-in Iris dataset instead.

The notebook displays the scaled dataset, PCA-transformed data, explained
variance table, and 2D scatter plot inline. The `species` label is used only
to color the plot; it is not included in PCA.

The first two components retain approximately **95.8%** of the dataset's
variance.
