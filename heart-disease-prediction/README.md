Heart Disease Prediction using Logistic Regression

Overview:

Heart disease is one of the leading causes of death worldwide.  
Early prediction of heart disease can help in timely medical intervention and reduce health risks.

This project uses Machine Learning and Logistic Regression to predict whether a patient is likely to have heart disease based on medical attributes such as age, cholesterol level, chest pain type, maximum heart rate, and more.

The project demonstrates a complete end-to-end machine learning workflow including:
- Data preprocessing
- Feature scaling
- Logistic Regression model training
- Prediction and evaluation
- Confusion Matrix analysis
- Cross Validation

---

Problem Statement

The objective of this project is to build a machine learning model capable of predicting:
Whether a patient has heart disease or not

This is a binary classification problem where:

- 1 → Heart Disease Present
- 0 → No Heart Disease

The model learns patterns from patient medical records and predicts the probability of heart disease.


 Dataset Information

The dataset used in this project was obtained from Kaggle.

Dataset Source:
https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

The dataset contains medical information collected from patients.

 Dataset Statistics

- Total Records: 1025
- Total Features: 13
- Target Column: target

---

# Features Used

| Feature | Description |
|---|---|
| age | Age of the patient |
| sex | Gender of the patient |
| cp | Chest pain type |
| trestbps | Resting blood pressure |
| chol | Cholesterol level |
| fbs | Fasting blood sugar |
| restecg | Resting electrocardiographic results |
| thalach | Maximum heart rate achieved |
| exang | Exercise induced angina |
| oldpeak | ST depression induced by exercise |
| slope | Slope of peak exercise ST segment |
| ca | Number of major vessels |
| thal | Thalassemia value |
| target | Output prediction column |

---

 Why Logistic Regression?

Logistic Regression is one of the most commonly used machine learning algorithms for binary classification problems.

It predicts the probability of an event occurring using the sigmoid function.

In this project, Logistic Regression is used to predict:

Probability of Heart Disease



If the predicted probability is greater than 0.5:
- Model predicts heart disease and target value become 1

Otherwise:
- Model predicts no heart disease and target value becomes 0


 Interpretation

- 77 Correct Negative Predictions
- 100 Correct Positive Predictions
- 21 False Positives
- 7 False Negatives

---

# Model Performance

| Metric | Value |
|---|---|
| Accuracy | ~84% |
| Cross Validation Accuracy | ~84% |
| Standard Deviation | ~4% |

The model achieved stable and reliable performance on the dataset.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

# Project Structure

```text
heart-disease-prediction/
│
├── dataset/
│   └── heart.csv
│
├── notebook/
│   └── heart_disease_prediction.ipynb
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---


# Conclusion

This project demonstrates how Logistic Regression can be applied to healthcare datasets for binary classification problems.

The model successfully predicts the likelihood of heart disease using patient medical information and achieves strong performance on the dataset.