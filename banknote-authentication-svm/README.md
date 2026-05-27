
 Banknote Authentication using Support Vector Machine (SVM)

Overview

This project uses a Support Vector Machine (SVM) classifier to determine whether a banknote is genuine or fake based on statistical image features.

The model is trained using numerical features extracted from banknote images through wavelet transformations.



 Problem Statement

Counterfeit currency detection is an important problem in banking and finance.

The objective of this project is to build a machine learning model capable of classifying banknotes as:
- Genuine
- Fake

using statistical image data.



 Dataset Information

Dataset: Banknote Authentication Dataset 
Source: https://archive.ics.uci.edu/dataset/267/banknote+authentication

Features used:
- Variance
- Skewness
- Curtosis
- Entropy

Target:
- 0 → Genuine banknote
- 1 → Fake banknote



Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook



Workflow

1. Data preprocessing
2. Train-test split
3. Feature scaling using StandardScaler
4. Training the SVM classifier
5. Model prediction
6. Confusion matrix and accuracy evaluation
7. Decision boundary visualization



 Results

The SVM Model achieved approximately:

 Accuracy: 98%



 Visualization

The project includes a decision boundary graph that visualizes how the SVM separates genuine and fake banknotes using selected features.



# Project Structure

banknote-authentication-svm/
│
├── data/
│   └── banknote_authentication.csv
│
├── notebooks/
│   └── Banknote_authentication_using_SVM_ML_Model.ipynb
│
├── requirements.txt
│
└── README.md



Author

Rohith Karning
