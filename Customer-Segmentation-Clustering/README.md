# Customer Segmentation using K-Means and Hierarchical Clustering

## Overview
This project performs customer segmentation on the Online Retail dataset using two unsupervised machine learning algorithms:
- K-Means Clustering
- Hierarchical (Agglomerative) Clustering

Customer behavior is summarized using the RFM (Recency, Frequency, Monetary) framework. The features are standardized before clustering, and PCA is used to visualize customer segments.

## Dataset
**File:** `Online Retail.xlsx`

The dataset contains transactional records from an online retail store, including invoice details, customer IDs, quantities, unit prices, and purchase dates.

## Project Workflow
1. Data loading and cleaning
2. Exploratory Data Analysis
3. RFM feature engineering
4. Feature scaling
5. K-Means clustering
6. Elbow Method and Silhouette Score
7. Hierarchical (Agglomerative) clustering
8. Cluster analysis
9. PCA-based visualization

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy

## Results
The notebook compares K-Means and Hierarchical Clustering to identify meaningful customer segments based on purchasing behavior.

## Folder Structure
```
Customer-Segmentation-Clustering/
├── Customer_Segmentation_using_K_Means_and_Hierarchical_Clustering.ipynb
├── Online Retail.xlsx
└── README.md
```

## Author
**Rohith Karning**
