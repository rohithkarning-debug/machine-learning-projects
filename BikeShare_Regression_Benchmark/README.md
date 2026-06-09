# BikeShare Regression Benchmark

## Overview

BikeShare Regression Benchmark is a machine learning project that evaluates and compares the performance of multiple regression algorithms on the UCI Bike Sharing Dataset. The objective is to predict hourly bike rental demand and determine which regression model provides the most accurate predictions.

Demand forecasting is an important real-world problem in transportation and urban mobility systems. Accurate demand prediction can help bike-sharing operators optimize bike allocation, improve customer experience, and better manage resources.

This project investigates how different regression techniques perform on the same dataset under identical preprocessing and evaluation conditions.

---

## Project Objectives

The primary objectives of this project are:

* Understand the complete machine learning workflow for regression problems.
* Apply data preprocessing and feature engineering techniques.
* Compare multiple regression algorithms on the same dataset.
* Evaluate model performance using standard regression metrics.
* Identify the most suitable model for bike rental demand prediction.
* Gain practical experience with Scikit-Learn and regression model benchmarking.

---

## Dataset Information

### Dataset Source

**UCI Machine Learning Repository**

Dataset Name: **Bike Sharing Dataset**
Link: https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset

The dataset contains hourly rental records from a bike-sharing system together with weather, seasonal, and temporal information.

### Dataset Used

```text
hour.csv
```

### Number of Records

```text
17,379 observations
```

### Prediction Target

```text
cnt
```

The target variable represents the total number of bike rentals recorded during a specific hour.

---

## Features Used

The following features were used for training the models:

| Feature    | Description                    |
| ---------- | ------------------------------ |
| season     | Season of the year             |
| yr         | Year indicator                 |
| mnth       | Month                          |
| hr         | Hour of day                    |
| holiday    | Whether the day is a holiday   |
| weekday    | Day of week                    |
| workingday | Whether it is a working day    |
| weathersit | Weather situation              |
| temp       | Normalized temperature         |
| atemp      | Normalized feeling temperature |
| hum        | Humidity                       |
| windspeed  | Wind speed                     |

---

## Features Removed

Several columns were removed before model training.

### instant

A unique identifier for each observation.

Reason:

* Contains no meaningful predictive information.

### dteday

Date column stored as text.

Reason:

* Not required for this benchmark.
* Additional date feature engineering was outside the scope of this project.

### casual

Number of casual bike rentals.

### registered

Number of registered bike rentals.

Reason:

The target variable is calculated as:

```text
cnt = casual + registered
```

Including these variables would introduce target leakage and produce unrealistically high accuracy scores.

---

## Data Preprocessing

The following preprocessing steps were performed:

### 1. Dataset Loading

The dataset was loaded using Pandas.

### 2. Feature Selection

Irrelevant and leakage-prone columns were removed.

### 3. Train-Test Split

The dataset was divided into:

```text
Training Set: 80%
Testing Set: 20%
```

Configuration:

```python
random_state = 42
```

This ensures reproducible results.

### 4. Feature Scaling

StandardScaler was applied to standardize numerical features.

```python
from sklearn.preprocessing import StandardScaler
```

Standardization helps algorithms such as:

* Multiple Linear Regression
* Polynomial Regression
* Support Vector Regression

perform more effectively.

---

## Regression Models Evaluated

### 1. Multiple Linear Regression

Multiple Linear Regression serves as the baseline model.

The model assumes a linear relationship between the independent variables and bike rental demand.

Characteristics:

* Fast training
* Easy interpretation
* Limited ability to model non-linear patterns

---

### 2. Polynomial Regression

Polynomial Regression extends Multiple Linear Regression by creating polynomial feature interactions.

Configuration:

```python
PolynomialFeatures(degree=2)
```

This allows the model to capture more complex relationships between variables.

---

### 3. Support Vector Regression (SVR)

Support Vector Regression is a kernel-based algorithm capable of learning non-linear decision boundaries.

Configuration:

```python
SVR(
    kernel="rbf",
    C=100
)
```

The hyperparameter C was tuned to improve performance over the default configuration.

---

### 4. Decision Tree Regression

Decision Trees recursively partition the feature space into decision regions.

Advantages:

* Captures non-linear relationships
* No assumptions about data distribution
* Easy visualization

Limitations:

* Can overfit training data

---

### 5. Random Forest Regression

Random Forest is an ensemble learning algorithm that combines multiple decision trees.

Configuration:

```python
RandomForestRegressor(
    n_estimators=100,
    random_state=42
)
```

Advantages:

* Reduces overfitting
* Improves generalization
* Handles non-linear relationships effectively

---

## Evaluation Metrics

Model performance was evaluated using four standard regression metrics.

### R² Score

Measures the proportion of variance explained by the model.

Higher values indicate better performance.

### Mean Absolute Error (MAE)

Measures the average magnitude of prediction errors.

Lower values indicate better performance.

### Mean Squared Error (MSE)

Measures the average squared prediction error.

Lower values indicate better performance.

### Root Mean Squared Error (RMSE)

Square root of MSE.

Provides error measurements in the same units as the target variable.

Lower values indicate better performance.

---

## Experimental Results

| Model                           | R² Score | MAE    | RMSE   |
| ------------------------------- | -------- | ------ | ------ |
| Multiple Linear Regression      | 0.388    | 104.80 | 139.21 |
| Polynomial Regression           | 0.542    | 91.25  | 120.43 |
| Support Vector Regression (SVR) | 0.597    | 67.94  | 112.92 |
| Decision Tree Regression        | 0.892    | 34.20  | 58.35  |
| Random Forest Regression        | 0.944    | 24.89  | 42.06  |

---

## Results Analysis

### Multiple Linear Regression

Multiple Linear Regression provided the weakest performance among the evaluated models.

The relatively low R² score indicates that bike rental demand cannot be adequately modeled using only linear relationships.

---

### Polynomial Regression

Polynomial Regression significantly improved performance by introducing interaction and squared terms.

This demonstrates the presence of non-linear relationships within the dataset.

---

### Support Vector Regression

After hyperparameter tuning, SVR outperformed both linear and polynomial models.

The RBF kernel successfully captured more complex patterns in rental demand.

---

### Decision Tree Regression

Decision Trees achieved a dramatic improvement in predictive performance.

The model effectively learned hierarchical relationships between weather conditions, time-related features, and rental demand.

---

### Random Forest Regression

Random Forest achieved the highest predictive accuracy.

The ensemble approach successfully reduced variance and improved generalization, resulting in an R² score above 0.94.

This model emerged as the best-performing algorithm in the benchmark.

---

## Key Findings

* Bike rental demand exhibits strong non-linear behavior.
* Linear models are insufficient for accurately modeling rental demand.
* Feature interactions significantly improve predictive performance.
* Kernel-based learning methods outperform traditional linear techniques.
* Tree-based ensemble methods achieve the highest accuracy.
* Random Forest Regression was the most effective model evaluated.

---

## Technologies Used

### Programming Language

* Python

### Libraries

* NumPy
* Pandas
* Matplotlib
* Scikit-Learn

### Development Environment

* Google Colab

---

## Repository Structure

```text
BikeShare_Regression_Benchmark/
│
├── BikeShare_Regression_Benchmark.ipynb
├── hour.csv
├── README.md
g
```

---

## Future Improvements

Potential enhancements include:

* Hyperparameter tuning using GridSearchCV
* Cross-validation for more robust evaluation
* XGBoost implementation
* LightGBM implementation
* Feature importance analysis
* Automated benchmarking framework
* Time-series forecasting approaches
* Advanced feature engineering from date variables

---

## Conclusion

This project demonstrates the importance of model selection in machine learning regression tasks. Five different regression algorithms were trained and evaluated on the UCI Bike Sharing Dataset using a consistent preprocessing and evaluation pipeline.

The results show that bike rental demand contains strong non-linear patterns that cannot be fully captured by traditional linear methods. Tree-based algorithms substantially outperformed linear approaches, with Random Forest Regression achieving the best overall performance.

The benchmark highlights how model complexity, feature interactions, and ensemble learning techniques can dramatically improve predictive accuracy in real-world demand forecasting problems.
