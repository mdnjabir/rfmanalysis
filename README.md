# 📊 Customer Segmentation Using RFM Analysis

## 📌 Problem Statement

**Customer Segmentation for Personalized Target Marketing of Existing Customers**

Businesses often struggle to allocate marketing resources effectively across a diverse customer base. Instead of treating all customers the same, it’s critical to identify which ones are the most loyal, which are at risk of leaving, and which need more attention. This project aims to segment existing customers based on their purchasing behavior using RFM (Recency, Frequency, and Monetary) analysis.

---

## 🧭 Approach & Why RFM?

RFM (Recency, Frequency, Monetary) analysis is a proven technique in customer analytics:

- **Recency (R):** How recently a customer made a purchase  
- **Frequency (F):** How often they make purchases  
- **Monetary (M):** How much money they've spent  

### Why RFM?

- Simple and effective behavioral segmentation method  
- Provides actionable insights using minimal data  
- Helps prioritize customer engagement based on value  

We used transaction history to create RFM scores and assigned each customer to a behavioral segment for targeted actions.

---

## 📂 Files Included

| File Name               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| `datacleaning_rfm.ipynb` | Prepares the dataset by cleaning and transforming transaction data         |
| `rfmanalysis.ipynb`      | Performs RFM metric calculation, scoring, and customer segmentation        |
| `README.md`              | Project documentation (this file)                                          |
| `cust_info.csv`          | Raw data contains the demographics details about the customer              |
| `cleaned_cust_info.csv`  | Cleaned version of cust_info.csv                                           |
| `transactions.csv`       | Raw data contains the transaction details of the customer                  |
| `cleaned_transactions.csv` | Cleaned version of transactions.csv                                      |
| `rfm_segments.csv`       | This file contains assigned segment and score of each customers            |

---

## 🔄 Process Overview

### 1. 🧹 Data Cleaning (`datacleaning_rfm.ipynb`)
- Removed null and invalid records (e.g., negative ages, missing IDs)
- Filtered active and valid customers for analysis

### 2. 🔄 Data Transformation
- Parsed `last_purchase_date` into datetime format
- Used a fixed **reference date** to compute **Recency**
- Aggregated `total_transactions` and `total_spent` to compute Frequency and Monetary values

### 3. 🧮 RFM Scoring (`rfmanalysis.ipynb`)
- Calculated individual RFM values for each customer
- Assigned **RFM scores** from 1 to 5 using quantile-based ranking
- Combined scores into a single string (e.g., `555`, `431`) for classification

## 💡 Recommendations for Existing Customer Segments

The following segments represent active or recently active customers who have made one or more purchases. These customers should be prioritized for personalized marketing and retention strategies:

| Segment Name           | Description                                | Recommended Strategy                                                                 |
|------------------------|--------------------------------------------|--------------------------------------------------------------------------------------|
| **Champions**          | Recent, frequent, and high-spending buyers | Offer loyalty rewards, exclusive previews, and early access to new products         |
| **Loyal**              | Consistently purchasing high-value buyers  | Upsell, cross-sell, and encourage referrals through loyalty programs                |
| **Potential Loyalist** | Fairly new but show promising patterns     | Nurture with special onboarding campaigns and product recommendations               |
| **Promising**          | Recent buyers with low spend/frequency     | Send personalized follow-ups and promotional offers to encourage repeat purchases   |
| **Need Attention**     | Regular buyers showing signs of inactivity | Re-engage with personalized “We miss you” messages or time-limited discounts        |
| **About To Sleep**     | Declining engagement with moderate value   | Use win-back email campaigns and survey-based feedback collection                   |
| **At Risk**            | High value in past but now disengaged      | Run targeted reactivation campaigns and offer strong incentives to return           |

These strategies focus on retaining value-generating customers and reducing churn by aligning outreach efforts with each customer segment’s behavior.


## 📒 Reference

All steps, code, and visualizations are documented in the following notebooks:
- [`datacleaning_rfm.ipynb`](./datacleaning_rfm.ipynb)
- [`rfmanalysis.ipynb`](./rfmanalysis.ipynb)

You can reproduce the process or adapt it to your own customer datasets.

---

## 🛠️ Tools Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Jupyter Notebook

---

## 📬 Connect

Created by [@mdnjabir](https://github.com/mdnjabir)

Feel free to contribute, fork, or reach out with suggestions!
