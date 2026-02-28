# 💳 Credit Card Customer Segmentation

> Unsupervised machine learning project using GMM clustering to identify 7 distinct behavioral segments from credit card usage data, with full profiling and business strategy recommendations per segment.

---

## 📌 Overview

This project segments credit card customers into **7 distinct behavioral clusters** using **Gaussian Mixture Models (GMM)**. The analysis covers the full data science pipeline — from cleaning and preprocessing through to cluster profiling and business recommendations — helping financial institutions better understand their customer base and design targeted strategies.

Both **K-Means** and **GMM** were applied and compared. K-Means suggested an optimal of 8 clusters while GMM converged on 7. **GMM was selected** as the final model due to its probabilistic nature, which provides softer, more realistic cluster boundaries and better captures the overlapping behavioral patterns in financial data.

---

## 🗂️ Repository Structure

```
├── data/
│   └── CC_GENERAL.csv             # Raw dataset
├── customer_segmentation.ipynb    # Full analysis notebook
├── cluster_portfolio.pdf          # Segment portfolio report (PDF)
└── README.md
```

---

## 📊 Dataset Features

| Feature | Description |
|---|---|
| `BALANCE` | Balance amount left in account to make purchases |
| `PURCHASES` | Total amount of purchases made from account |
| `ONEOFF_PURCHASES` | Maximum purchase amount done in one-go |
| `CASH_ADVANCE` | Cash in advance given by the user |
| `CASHADVANCE_TRX` | Number of transactions made with cash in advance |
| `PURCHASES_TRX` | Number of purchase transactions made |
| `PAYMENTS` | Amount of payment done by user |
| `MINIMUM_PAYMENTS` | Minimum amount of payments made by user |
| `PRC_FULL_PAYMENT` | Percent of full payment paid by user |
| `CREDIT_LIMIT` | Limit of credit card for user |

---

## 🤖 Methodology

1. **Data Reading** — Loaded `CC_GENERAL.csv` and explored the structure
2. **Data Cleaning** — Handled inconsistencies and irrelevant columns
3. **Missing Value Treatment** — Identified and imputed missing values
4. **Log Transformation** — Applied log transform to right-skewed features to normalize distributions
5. **Feature Scaling** — Standardized all features before clustering
6. **K-Means Clustering** — Applied K-Means, optimal k = **8** clusters (via Elbow / Silhouette)
7. **GMM Clustering** — Applied Gaussian Mixture Model, optimal k = **7** clusters 
8. **Model Selection** — Chose **GMM** for its probabilistic soft assignments and superior cluster quality
9. **Cluster Profiling** — Analyzed mean feature values per cluster to build behavioral personas

---

## 📈 Model Comparison

GMM was preferred because it models clusters as Gaussian distributions with flexible shapes, making it more suitable for financial behavioral data where customer segments naturally overlap.

---

## 🧩 Identified Segments

| Cluster | Segment Name | Key Trait |
|---|---|---|
| 0 | Cash Advance Reliant | High cash advance, low full payment |
| 1 | High Balance Revolvers | Highest minimum payments, revolving debt |
| 2 | Low Activity Users | Minimal purchases and engagement |
| 3 | Active Big Spenders | Highest purchases and transaction count |
| 4 | Inactive Credit Holders | Near-zero card usage |
| 5 | Responsible Transactors | Regular purchases, pays mostly in full |
| 6 | Affluent Full Payers | High credit limit, highest full-payment rate |

For the full segment analysis including behavioral profiles and recommended strategies, see [`cluster_portfolio.pdf`](./cluster_portfolio.pdf).

---

## 🛠️ Technologies Used

- **Python** — pandas, numpy, scikit-learn, matplotlib, seaborn
- **Clustering** — `sklearn.cluster.KMeans`, `sklearn.mixture.GaussianMixture`
- **Preprocessing** — `sklearn.preprocessing.StandardScaler`, `numpy.log1p`
- **Visualization** — matplotlib, seaborn
- **Environment** — Jupyter Notebook

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/Mahmouuuddd/Customer-Segmentation-for-Credit-Card-Customers.git
cd Customer-Segmentation-for-Credit-Card-Customers

# 2. Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

# 3. Launch the notebook
jupyter notebook customer_segmentation.ipynb
```

---

## 📄 Portfolio Report

A full PDF portfolio summarizing all 7 clusters with metrics, behavioral profiles, and business strategies is available here → [`cluster_portfolio.pdf`](./cluster_portfolio.pdf)

---

<p align="center">Made by <a href="https://github.com/Mahmouuuddd">Mahmoud</a></p>