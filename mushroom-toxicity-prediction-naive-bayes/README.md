# Mushroom Toxicity Prediction using Naive Bayes

## Overview

This project applies the **Naive Bayes Classification Algorithm** to predict whether a mushroom is **edible** or **poisonous** based on its physical characteristics.

Using the Mushroom Dataset from the UCI Machine Learning Repository, the model learns probabilistic relationships between mushroom attributes and toxicity, allowing it to classify unseen samples with high accuracy.

---

## Dataset Information

**Dataset:** Mushroom Dataset
**Source:** UCI Machine Learning Repository

The dataset contains descriptions of hypothetical mushroom samples belonging to species in the Agaricus and Lepiota family.

### Dataset Statistics

| Attribute       | Value       |
| --------------- | ----------- |
| Total Instances | 8,124       |
| Total Features  | 22          |
| Feature Type    | Categorical |
| Target Classes  | 2           |

### Target Variable

| Value | Meaning   |
| ----- | --------- |
| 0     | Edible    |
| 1     | Poisonous |

### Sample Features

* Cap Shape
* Cap Surface
* Cap Color
* Bruises
* Odor
* Gill Color
* Gill Size
* Stalk Shape
* Veil Color
* Ring Type
* Population
* Habitat

---

## Why Naive Bayes?

Naive Bayes was chosen for this project because it is particularly effective for classification tasks involving categorical data.

### Advantages

* Fast and computationally efficient
* Performs well on high-dimensional datasets
* Simple and easy to interpret
* Works effectively after categorical encoding
* Provides strong baseline performance

Since the Mushroom Dataset consists entirely of categorical attributes, Naive Bayes serves as a suitable and efficient classification model.

---

## Data Preprocessing

The following preprocessing steps were performed:

### 1. Data Loading

The mushroom dataset was imported into a Pandas DataFrame.

### 2. Feature Naming

Descriptive column names were assigned to improve readability and analysis.

### 3. Target Conversion

The original target values were converted as follows:

* e → 0 (Edible)
* p → 1 (Poisonous)

### 4. Label Encoding

Since all attributes are categorical, Label Encoding was applied to convert text categories into numerical representations suitable for machine learning algorithms.

### 5. Train-Test Split

The dataset was divided into:

* Training Set: 75%
* Testing Set: 25%

This ensures that model performance is evaluated on unseen data.

---

## Model Used

### Gaussian Naive Bayes

The Gaussian Naive Bayes classifier from Scikit-Learn was trained using the processed training dataset.

Although the dataset is categorical, Gaussian Naive Bayes still provides a strong baseline and demonstrates the effectiveness of probabilistic classification methods.

---

## Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1 Score

---

## Results

### Accuracy Score

**91.43%**

This means the model correctly classified approximately 91 out of every 100 mushrooms in the testing dataset.

### Performance Summary

* Accuracy: **91.43%**
* Strong classification performance
* Effective separation of edible and poisonous mushrooms
* Demonstrates the usefulness of probabilistic learning methods on categorical datasets

---

## Visualizations Included

The project includes the following visualizations:

### Confusion Matrix

Shows the number of correct and incorrect classifications.

### Class Distribution Plot

Displays the distribution of edible and poisonous mushrooms.

### Accuracy Visualization

Provides a visual representation of model performance.

These visualizations help interpret both the dataset and the classifier's effectiveness.

---

## Project Structure

```text
Mushroom_Toxicity_Prediction_Naive_Bayes/
│
├── Mushroom_Toxicity_Prediction_using_Naive_Bayes.ipynb
├── agaricus-lepiota.data
└── README.md
```



## Conclusion

This project demonstrates how the Naive Bayes algorithm can successfully solve a real-world classification problem involving categorical data. By leveraging probabilistic learning, the model achieved an accuracy of **91.43%**, showing that Naive Bayes remains a powerful and efficient baseline classifier for structured classification tasks.
