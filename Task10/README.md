# Train Multiple Regression Models

This project compares three different **regression models** using the **California Housing Dataset**.

## Objective

The objective is to train multiple regression algorithms on the same dataset and compare their performance using evaluation metrics.

## Models Used

### 1. Linear Regression

Linear Regression is a basic regression algorithm that finds a linear relationship between input features and the target value.

### 2. Decision Tree Regression

Decision Tree Regression uses a tree-like structure to make predictions based on different conditions in the data.

### 3. Random Forest Regression

Random Forest Regression combines multiple decision trees to produce a more reliable prediction.

## Dataset

The **California Housing Dataset** is imported from `scikit-learn`.

The dataset contains information about California housing areas and their corresponding house values.

## Evaluation Metrics

The models are evaluated using:

* **MAE (Mean Absolute Error)** – Measures the average prediction error.
* **MSE (Mean Squared Error)** – Measures the average squared prediction error.
* **R² Score** – Measures how well the model explains the target values.

For MAE and MSE, a lower value is better.

For R² Score, a higher value is better.

## Technologies Used

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook



## Output

The program displays:

* Dataset information
* Performance of each regression model
* MAE
* MSE
* R² Score
* Best-performing model

## Result

The three regression models are trained using the same training and testing data. Their performance is compared using MAE, MSE, and R² Score to identify the best-performing model.
