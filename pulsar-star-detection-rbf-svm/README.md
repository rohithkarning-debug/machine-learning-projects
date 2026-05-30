# Pulsar Star Detection using RBF Kernel SVM

## Overview

This project uses a Radial Basis Function (RBF) Kernel Support Vector Machine to classify radio telescope signals as either pulsars or non-pulsars using the HTRU2 dataset.

Pulsars are highly magnetized rotating neutron stars that emit beams of electromagnetic radiation. The objective is to identify genuine pulsar candidates from noisy astronomical observations.

---

## Dataset

**HTRU2 Pulsar Star Dataset**
Source: https://archive.ics.uci.edu/dataset/372

- Samples: 17,898
- Features: 8
- Classes: 2 (Pulsar / Non-Pulsar)

### Target Classes

| Class | Meaning |
|---------|---------|
| 0 | Non-Pulsar |
| 1 | Pulsar |

---

## Project Workflow

1. Load and preprocess the dataset
2. Split data into training and testing sets
3. Scale features using StandardScaler
4. Train an RBF Kernel SVM model
5. Generate predictions on the test set
6. Evaluate model performance
7. Visualize decision boundaries using PCA

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

---

## Repository Structure

```text
pulsar-star-detection-rbf-svm/
│
├── data/
│   └── HTRU_2.csv
│
├── notebooks/
│   └── Pulsar_Signal_Classification_with_RBF_SVM.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---



## Author

Rohith Karning
