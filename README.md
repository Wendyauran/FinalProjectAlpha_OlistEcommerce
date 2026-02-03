# Customer Segmentation with Machine Learning to Improve Customer Retention and Purchase Frequency for Olist E-Commerce

Segmenting Customers to Support Retention, Campaign Targeting, and Purchase Frequency Growth

**Data Source:** Olist Brazil E-Commerce Public Dataset [Dataset Source](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

# A. Business Context

Brazil’s e-commerce market is growing rapidly, driven by strong digital adoption, instant payment systems, and logistics improvements. Competition among platforms is increasing, making **customer retention and repeat purchase** critical growth drivers.

Olist is a major Brazilian marketplace that connects sellers and buyers with integrated logistics support. While **transaction volume grows, long-term customer retention rate and engagement remains a key challenge**.

To compete effectively, the platform needs **data-driven customer segmentation** to support targeted marketing and retention strategies to **improve retention rate and repeat purchases**.

---

# B. Problem Statement

Transaction data shows that:

* Most customers purchase only once
* Repeat buying is very low
* Retention rate is below 1%
* Campaigns are not yet behavior-based

Without behavioral segmentation, marketing and retention efforts and budget are less effective and inefficient.

---

# C. Goals

* Identify key behavioral differences between customer groups
* Support retention & repeat purchase strategy
* Improve campaign targeting effectiveness
* Build customer segmentation using machine learning

---

# D. Analytical Approach

- EDA: Data exploration and behavioral pattern analysis
- Data cleaning, merging, and feature engineering (feature selection and scalling)
- RFM and Cohort analysis (Retention Rate)
- Modelling and Interpretation:
  - Customer segmentation using KMeans clustering
  - Optimal cluster selection using Elbow & Silhouette methods
  - Cluster interpretation for business strategy
- Conclusion & Recommendation
  
---

# E. Evaluation Metrics

Clustering quality evaluated using:

* **Elbow Method** — optimal cluster count via SSE curve
* **Silhouette Score** — cluster separation quality
* Business interpretability of each cluster profile
  
Both methods indicate the optimal number of clusters at K = 3, resulting in three customer clusters (0, 1, 2).

---

# F. Key Behavioral Insights

- Order volume peaks on Monday–Tuesday and during 10:00–16:00 hours
- Revenue and order volume show steady growth with strong spikes during major promo events
- Orders and customers are highly concentrated in Sao Paulo
- Top product categories: bed_bath_table and health_beauty
- ~21% low reviews (score 1–3). Longer delivery → lower review score. Main bottleneck at last-mile delivery

# G. RFM & Retention

- Most customers have frequency = 1
- Retention rate < 1%
- Repeat purchase is low

---

# H. Machine Learning Segmentation Result

Customer segmentation using **KMeans** produced 3 clusters.

## Main Segmentation Drivers

* Frequency
* Monetary
* Price
* Payment Installments

## Other Features But Not The Strong Differentiators

* Recency (relatively uniform)
* Payment method
* Customer city

## Cluster Distribution

| Cluster   | Share  |
| --------- | ------ |
| Cluster 0 | 97.27% |
| Cluster 1 | 0.03%  |
| Cluster 2 | 2.70%  |

---

# I. Customer Segment Profiles

- Cluster 0 — Satisfied & Low-Spend Buyers: Low transaction value, low price products, low installment usage, high satisfaction.
- Cluster 1 — High-Spend At-Risk BuyersL Very high spending, low frequency, lower review scores, churn risk.
- Cluster 2 — Premium Installment Buyers: High price products, high installment usage, premium-oriented purchases.

---

# I. Tools (Tech Stack)

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* KMeans Clustering

---

# J. Conclusion

Customer retention and repeat purchase are the main business problems in Olist Ecommerce by 2017-2018 data, with most users buying only once. RFM and cohort analysis confirm extremely low retention. Machine learning clustering reveals three distinct behavioral segments driven mainly by transaction value, frequency, price level, and installment usage. These segments enable more precise, behavior-based marketing and retention strategies.

---

# K. Recommendations

## Business
- Run campaigns during early-week peak hours
- Focus operational and marketing efforts in Sao Paulo
- Improve last-mile delivery performance
- Apply segment-based retention and campaign strategies

## Model
- Test alternative clustering methods (DBSCAN, Hierarchal Clustering and Gaussian Mixture Models
- Apply a more systematic treatment of extreme values, such as log transformation, to prevent them from distorting the clustering results.
- Add behavioral value features (AOV, CLV)
- Apply stronger outlier treatment and stability testing
- Test alternative clustering methods
- Add behavioral value features (AOV, CLV)
- Apply stronger outlier treatment and stability testing
