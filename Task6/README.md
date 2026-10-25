# Feature Engineering Basics

This project demonstrates **Feature Engineering** using the **Titanic Dataset** with Python.

## Objective

The objective of this task is to create new and meaningful features from the existing Titanic dataset. These engineered features can provide additional information that can be useful for **data analysis and machine learning**.

## Dataset

The Titanic dataset is imported from an online CSV file using **Pandas**.

The dataset contains passenger information such as:

* Name
* Age
* SibSp
* Parch
* Fare
* Passenger Class
* Survival

## Features Created

### 1. Family Size

The `Family_Size` feature combines the number of siblings/spouses and parents/children.

```text
Family_Size = SibSp + Parch + 1
```

It represents the total number of people in the passenger's immediate family group.

### 2. Is Alone

The `Is_Alone` feature identifies whether a passenger travelled alone.

```text
1 = Passenger travelled alone
0 = Passenger travelled with family
```

### 3. Fare Per Person

The `Fare_Per_Person` feature calculates the approximate fare paid by each family member.

```text
Fare_Per_Person = Fare / Family_Size
```

### 4. Age Group

The `Age` feature is converted into meaningful age categories:

* **Child** – 0 to 12
* **Teenager** – 13 to 18
* **Adult** – 19 to 60
* **Senior** – 61 to 100

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**

## Libraries Used

```python
import pandas as pd
import numpy as np
```

## How the Program Works

1. The Titanic dataset is loaded using Pandas.
2. The original dataset and its shape are displayed.
3. `Family_Size` is created using `SibSp` and `Parch`.
4. `Is_Alone` is created to identify passengers travelling alone.
5. `Fare_Per_Person` is calculated from the fare and family size.
6. `Age_Group` is created from the passenger's age.
7. The original and engineered features are displayed.
8. The engineered dataset is saved as a CSV file.

## How to Run

Install the required libraries:

```bash
pip install pandas numpy
```

Run the program:

```bash
python feature_engineering.py
```

## Output

The program displays:

* Original Titanic dataset
* Dataset shape
* Engineered features
* Feature explanations
* Original vs engineered features

## Result

The project successfully demonstrates how **existing Titanic dataset columns can be transformed into new meaningful features**. These features can be used as additional inputs for further **data analysis and machine learning tasks**.
