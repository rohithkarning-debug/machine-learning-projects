# Market Basket Analysis using Apriori Algorithm

## Overview
This project performs Market Basket Analysis using the Apriori algorithm to discover purchasing patterns from grocery transactions. The goal is to identify products that are frequently bought together and generate association rules that can support recommendation systems, cross-selling, and retail decision-making.

## Problem Statement
Retailers often want to understand customer purchasing behavior. By analyzing transaction history, this project answers questions such as:
- Which products are commonly purchased together?
- If a customer buys one product, what other products are they likely to buy?
- Which product combinations are valuable for promotions and store layout optimization?

## Dataset
**File:** `groceries.csv`

- ~9,835 customer transactions
- ~169 unique grocery products
- Each row represents one shopping basket with a variable number of purchased items.

## Workflow
1. Load transaction dataset
2. Preprocess transactions
3. Apply the Apriori algorithm
4. Generate association rules
5. Evaluate rules using Support, Confidence, and Lift
6. Display the strongest product associations

## Model Used
### Apriori Algorithm
Apriori is an unsupervised association rule learning algorithm used to discover frequent itemsets and generate association rules.

**Metrics**
- **Support:** Frequency of an itemset in all transactions.
- **Confidence:** Probability that customers buying the antecedent also buy the consequent.
- **Lift:** Strength of the association compared with random chance.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Apyori

## Folder Structure

```text
apriori-market-basket-analysis/
│
├── Apriori_Market_Basket_Analysis.ipynb
├── groceries.csv
└── README.md
```

## Results
The model discovers meaningful associations between grocery items that can be used for market basket analysis, recommendation systems, inventory planning, and targeted marketing.

## Author
**Rohith Karning**

Machine Learning • Artificial Intelligence • Data Science
