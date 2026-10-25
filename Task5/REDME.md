# Advanced Data Cleaning

This project focuses on cleaning a real-world customer dataset using **Python and Pandas**.

## Objective

The main objective is to identify and fix common data-quality problems before using the dataset for analysis or machine learning.

## Cleaning Steps

* Checked the dataset structure and data types
* Identified missing values
* Removed duplicate records
* Cleaned column names
* Removed unnecessary spaces
* Standardized categorical values
* Converted age and salary into numeric format
* Handled missing numerical values using the median
* Handled missing categorical values using the mode
* Standardized city names
* Cleaned email addresses
* Standardized phone numbers
* Saved the cleaned dataset as a new CSV file

## Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook

## Dataset

The project uses a customer dataset containing information such as:

* Name
* Gender
* Age
* City
* Salary
* Email
* Phone Number

The original dataset contains intentionally messy values to demonstrate real-world data-cleaning techniques.

## Files

```text
Advanced-Data-Cleaning/
│
├── customer_data.csv
├── cleaned_customer_data.csv
├── advanced_data_cleaning.py
├── Advanced_Data_Cleaning.ipynb
└── README.md
```

## How to Run

Install the required libraries:

```bash
pip install pandas numpy
```

Run the Python program:

```bash
python advanced_data_cleaning.py
```

## Output

The program produces:

```text
cleaned_customer_data.csv
```

The cleaned dataset contains standardized and corrected values with duplicates and major data-quality issues removed.

## Result

This task demonstrates how **data cleaning and preprocessing** can improve the quality and reliability of data before performing **data analysis or machine learning**.
