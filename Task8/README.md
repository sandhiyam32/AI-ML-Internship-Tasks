# Task 8 – One-Hot Encoding

## Description

This task demonstrates **One-Hot Encoding**. It converts categorical data into separate numerical columns so that it can be used for Machine Learning.

## Dataset

`One_Hot_Encoding_Dataset.csv`

The dataset contains student information such as:

* Gender
* Department
* City
* Age
* Marks

## Tools Used

* Python
* Pandas
* Jupyter Notebook

## What I Did

1. Loaded the student dataset.
2. Selected the categorical columns.
3. Applied One-Hot Encoding using `pd.get_dummies()`.
4. Compared the data before and after encoding.
5. Saved the encoded dataset as `One_Hot_Encoded_Output.csv`.

## Example

Before encoding:

```text
Gender   Department
Female   CSE
Male     ECE
```

After encoding:

```text
Gender_Female  Gender_Male  Department_CSE  Department_ECE
1              0            1               0
0              1            0               1
```

## Key Learning

One-Hot Encoding converts each category into a separate column containing `0` or `1`.

It is useful for categorical variables where there is no natural order between the categories.

## Conclusion

I learned how to convert categorical features into numerical columns using One-Hot Encoding and prepare the dataset for Machine Learning.
