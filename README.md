# 📊 Customer Segmentation with Machine Learning to Improve Customer Retention and Purchase Frequency for Olist E-Commerce

Segmenting Customers to Support Retention, Campaign Targeting, and Purchase Frequency Growth

**Data Source:** Olist Brazil E-Commerce Public Dataset [Dataset Source](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

# A. Business Context

Brazil’s e-commerce market is growing rapidly, driven by strong digital adoption, instant payment systems, and logistics improvements. Competition among platforms is increasing, making **customer retention and repeat purchase** critical growth drivers.

Olist is a major Brazilian marketplace that connects sellers and buyers with integrated logistics support. While transaction volume grows, long-term customer engagement remains a key challenge.

To compete effectively, the platform needs **data-driven customer segmentation** to support targeted marketing and retention strategies.

---

# B. Problem Statement

Transaction data shows that:

* Most customers purchase only once
* Repeat buying is very low
* Retention rate is below 1%
* Campaigns are not yet behavior-based

Without behavioral segmentation, marketing and retention efforts are less effective and inefficient.

---

# C. Goals

* Build customer segmentation using machine learning
* Identify key behavioral differences between customer groups
* Support retention & repeat purchase strategy
* Improve campaign targeting effectiveness
* Enable data-driven marketing decisions

---

# D. Analytical Approach

## Data Understanding

* Explore transaction, customer, product, payment, and review data
* Analyze order trend, revenue trend, time pattern, and geography
* Study delivery performance and review behavior

## Data Preprocessing & Feature Engineering

* Data cleaning & missing value handling
* Multi-table dataset merging
* Feature engineering (behavioral & transactional features)
* Encoding categorical variables
* Feature scaling

## Behavioral Analysis

* Order & revenue trends
* Time-of-day & day-of-week patterns
* Product category & payment behavior
* Delivery time vs review score
* Geographic concentration

## Customer Analysis & Modeling

* RFM Analysis
* Cohort Retention Analysis
* **KMeans Clustering for customer segmentation**

---

# E. Evaluation Metrics

Clustering quality evaluated using:

* **Elbow Method** — optimal cluster count via SSE curve
* **Silhouette Score** — cluster separation quality
* Business interpretability of each cluster profile

---

# F. Key Behavioral Insights

## Order & Time Pattern

* Highest orders: **Monday–Tuesday**
* Peak hours: **10:00–16:00**
* Strong spike during major promotion events (e.g., Black Friday)
* Orders and revenue show consistent growth trend

## Geographic Insight

* Orders highly concentrated in **Sao Paulo**. Large gap between metro vs non-metro demand.

## Product & Payment Behavior

* Top categories: **bed_bath_table** and **health_beauty**
* Dominant payment method: **credit card**
* Most transactions without installments

## Delivery & Review

* ~21% low reviews (score 1–3 are categorized as bad reviews in this analysis)
* Longer delivery → lower review score
* Main bottleneck at **last-mile delivery**

## RFM & Retention Rate (Cohort Analysis)

* Most customers have frequency = 1
* Retention rate < 1%
* Repeat purchase is the core business challenge

---

# G. Machine Learning Segmentation Result

Customer segmentation using **KMeans** produced 3 clusters.

## Main Segmentation Drivers

* Frequency
* Monetary
* Price
* Payment Installments

## Not Strong Differentiators

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

# H. Customer Segment Profiles

## Cluster 0 — Satisfied & Low-Spend Buyers

* Low transaction value
* Low price products
* Low installments
* High review score
* Dominant category: bed_bath_table

---

## Cluster 1 — High-Spend At-Risk Buyers

* Highest monetary value
* Low frequency
* Low review score
* Dominant category: office_furniture

---

## Cluster 2 — Premium Installment Buyers

* High product price
* High installments
* Large ticket size
* Mixed but generally good reviews
* Dominant category: watches_gift

---

# I. Tools (Tech Stack)

* Python
* Pandas, NumPy
* Scikit-Learn
* Matplotlib, Seaborn
* KMeans Clustering
* RFM & Cohort Analysis

---

# J. Conclusion

Customer retention and repeat purchase are the main business problems in Olist Ecommerce by 2017-2018 data, with most users buying only once. RFM and cohort analysis confirm extremely low retention. Machine learning clustering reveals three distinct behavioral segments driven mainly by transaction value, frequency, price level, and installment usage. These segments enable more precise, behavior-based marketing and retention strategies.

---

# K. Recommendations

## Business

* Focus campaigns on early-week peak hours
* Prioritize Sao Paulo for marketing & fulfillment efficiency
* Improve last-mile delivery performance to raise review scores
* Apply **cluster-based campaign & retention strategy**

## Model

* Compare with alternative clustering (DBSCAN, Hierarchical, GMM)
* Apply outlier treatment & log transformation
* Add behavioral features (AOV, CLV)
* Test cluster stability across time periods
