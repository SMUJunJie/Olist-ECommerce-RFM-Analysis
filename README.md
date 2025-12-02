# Olist E-Commerce Customer Segmentation (RFM Analysis)

## 📌 Project Overview
This project analyzes customer behavior data from Olist (Brazilian E-Commerce) to identify high-value customers and at-risk users. 
Using the **RFM Model (Recency, Frequency, Monetary)**, we segmented 100,000+ customers to provide actionable marketing strategies.

**Key Business Problem:** How to differentiate between "one-time buyers" and "high-value loyalists" in a low-frequency marketplace environment?

## 🛠️ Tech Stack
* **Language**: Python (Pandas)
* **Database Engine**: DuckDB (In-memory SQL)
* **Techniques**: 
    * Complex SQL Queries (CTEs, Joins)
    * Window Functions (`NTILE`, `RANK`)
    * Weighted Scoring Logic (`CASE WHEN`)

## 📊 Methodology (The RFM Approach)
We calculated three key metrics for each user using SQL:
1.  **Recency (R)**: Days since last purchase.
2.  **Frequency (F)**: Total number of orders.
3.  **Monetary (M)**: Total spend.

**Weighted Scoring:**
Given the nature of the dataset (low frequency), we applied a weighted score:
> **Final Score = R * 30% + F * 20% + M * 50%**

## 💡 Key Insights & Results
*(See the full code in `RFM_Analysis_Olist_ECommerce.ipynb`)*

**Snapshot of the Analysis Result:**
![Result Screenshot](result_snapshot.png)

**Strategic Recommendations:**
1.  **💎 Core VIPs (Whales)**: Customers with high Spend & Recency. 
    * *Action*: Priority customer service, Early access to new products.
2.  **💤 High Value Churn**: Customers who spent a lot (> $1000) but haven't visited in 300+ days.
    * *Action*: Aggressive win-back campaigns (Coupons/Emails).
3.  **🛒 Regular Users**: Standard behavior.
    * *Action*: Upselling recommendations.

## 🚀 How to Run
1.  Download the dataset from Kaggle (Olist Brazilian E-Commerce).
2.  Install dependencies: `pip install pandas duckdb`
3.  Run the Jupyter Notebook.

---
*Author: Junjie Qu*
*SMU Master of IT in Business (MITB) Candidate*
