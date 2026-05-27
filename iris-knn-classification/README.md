
Iris Species Classification using K-Nearest Neighbors ML Model (K-NN)

 Project Overview
This project uses the K-Nearest Neighbors (K-NN) Machine Learning algorithm to classify Iris flower species based on flower measurements.

The model predicts whether a flower belongs to:
- Iris-setosa
- Iris-versicolor
- Iris-virginica

This project demonstrates ml workflow including:
- Data preprocessing
- Train-test splitting
- Feature scaling
- K-NN classification
- Confusion matrix evaluation
- Accuracy score calculation
- Decision boundary visualization



Problem Statement
The goal of this project is to classify Iris flowers into different species using measurements such as:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

Since this is a supervised classification problem, the model learns from labeled examples and predicts the species of unseen flowers.

---

## Dataset Information
- Dataset: Iris Dataset
- Source: https://www.kaggle.com/datasets/uciml/iris
- Total Records: 150
- Features Used:
  - SepalLengthCm
  - SepalWidthCm
  - PetalLengthCm
  - PetalWidthCm
- Target Variable:
  - Species



Algorithm Used — K-Nearest Neighbors (K-NN)

K-NN is a supervised machine learning classification algorithm.

 How K-NN Works
1. Choose the number of neighbors (K)
2. Calculate distance between data points
3. Find the nearest K neighbors
4. Assign the class based on majority voting

In this project:
- Feature scaling was applied using StandardScaler
- Euclidean distance was used for classification (minkowski metric mentioned in code)
- The model predicts flower species based on nearest neighboring flowers


Machine Learning Workflow

1. Import Dataset
2. Data Preprocessing
3. Train-Test Split
4. Feature Scaling
5. K-NN Model Training
6. Prediction on Test Set
7. Confusion Matrix Evaluation
8. Accuracy Score Calculation
9. Visualization of Decision Boundaries



 Model Performance

- Accuracy Achieved: 96%
- Confusion Matrix showed strong classification performance
- The K-NN model performed very well on the Iris dataset


## Project Structure

iris-knn-classification/
│
├── dataset/
│   └── Iris.csv
│
├── notebook/
│   └── iris_knn_classification.ipynb
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore



Conclusion
This project demonstrates how K-Nearest Neighbors can effectively classify Iris flower species using flower measurements.
The model achieved high accuracy.
