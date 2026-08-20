# Customer Segmentation & RFM Analysis

## 📌 Project Overview

This project analyzes retail transaction data to understand customer purchasing behavior and identify meaningful customer segments.

The project combines **SQL and Python** to perform data cleaning, exploratory analysis, RFM analysis, and customer segmentation using **K-Means clustering**.

---

## 🎯 Business Objectives

* Identify high-value customers
* Understand customer purchasing behavior
* Analyze **Recency, Frequency, and Monetary (RFM)** value
* Identify inactive customers
* Segment customers based on purchasing behavior
* Generate actionable customer retention strategies

---

## 🛠️ Tools & Technologies

* SQL / MySQL
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* K-Means Clustering

## 📂 Dataset

This project uses the **Online Retail Dataset** from the UCI Machine Learning Repository.

The dataset contains **541,909 transaction records** from a UK-based online retailer between December 2010 and December 2011.

Due to the large size of the original dataset, the complete dataset is not included in this repository. 
A representative sample of the dataset is provided in the repository as Online Retail DATA - Sample.csv for reference and reproducibility.

The full dataset was used for the analysis and customer segmentation results reported in this project.

**Dataset Source:**  
[UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)


---

## 🔄 Project Workflow

**Raw Retail Data**  
⬇️  
**Data Quality Checks**  
⬇️  
**Data Cleaning & Preprocessing**  
⬇️  
**Exploratory Data Analysis**  
⬇️  
**RFM Analysis**  
⬇️  
**RFM Scoring**  
⬇️  
**Customer Segmentation**  
⬇️  
**K-Means Clustering**  
⬇️  
**Segment Profiling**  
⬇️  
**Business Insights & Recommendations**


---

## 🗄️ SQL Analysis

The SQL analysis covers:

* Database and table creation
* Data quality checks
* Missing-value analysis
* Duplicate checks
* Cancelled transaction analysis
* Quantity and price validation
* Data cleaning
* Revenue analysis
* Customer-level RFM calculation
* RFM scoring
* Rule-based customer segmentation
* Revenue by customer segment
* Top customer and product analysis
* Monthly sales analysis

The SQL workflow creates RFM scores and classifies customers into interpretable, rule-based segments such as:

* Champions
* Cannot Lose Them
* At Risk
* Loyal Customers
* Potential Loyalists
* New Customers
* Lost Customers
* Hibernating
* Needs Attention

---

## 🐍 Python / Jupyter Notebook

The Jupyter Notebook includes:

* Data cleaning and preprocessing
* Feature engineering
* Exploratory Data Analysis
* Revenue and sales analysis
* RFM analysis
* RFM visualization
* Log transformation
* Feature scaling
* K-Means clustering
* Silhouette Score analysis
* Customer segment profiling
* Business recommendations

---

## 🎯 Segmentation Approach

SQL RFM Segmentation uses business-defined rules to create interpretable behavioral segments, while Python K-Means Clustering uses an unsupervised machine-learning approach to identify natural groupings in customer behavior. 
The two approaches serve different analytical purposes and are not expected to produce identical segment labels.
---
## 📊 Key Results

The analysis identified **4,338 customers** for customer-level segmentation.

Different values of **K** were evaluated using the Silhouette Score, with **K = 2** producing the best clustering result.

### K-Means Results
| Metric | Result |
|---|---:|
| Customers Analyzed | 4,338 |
| Optimal K | 2 |
| Silhouette Score | 0.4328 |

### Final Customer Segments

| Customer Segment | Customers | Avg. Recency | Avg. Frequency | Avg. Monetary |
|---|---:|---:|---:|---:|
| High-Value Loyal Customers | 1,666 | 25.89 days | 8.44 | £4,539.60 |
| Inactive Low-Value Customers | 2,672 | 134.09 days | 1.67 | £495.59 |
---

## 💡 Business Insights

### ⭐ High-Value Loyal Customers

These customers purchase more frequently, have purchased more recently, and generate significantly higher monetary value.

**Recommended strategies:**

* Loyalty rewards
* Personalized offers
* VIP programs
* Cross-selling and upselling
* Exclusive product access

### 💤 Inactive Low-Value Customers

This segment represents a large portion of the customer base and shows lower purchasing frequency and monetary value.

**Recommended strategies:**

* Win-back campaigns
* Personalized discounts
* Re-engagement emails
* Targeted product recommendations
* Limited-time offers
---
## 📂 Repository Structure

```text
Customer-Segmentation-RFM/
│
├── README.md
├── customer_segmentation_rfm.ipynb
└── customer_segmentation_rfm.sql
```

### `customer_segmentation_rfm.ipynb`

Python-based analysis covering:

* Data cleaning
* Exploratory analysis
* Visualization
* RFM analysis
* Feature engineering
* K-Means clustering
* Customer segmentation
* Business recommendations

### `customer_segmentation_rfm.sql`

SQL-based analysis covering:

* Data quality checks
* Data cleaning
* Revenue analysis
* RFM calculation
* RFM scoring
* Rule-based customer segmentation
* Business analysis

---

## 👤 Author

**Stenal Rodrigues**

**Data Analyst | Aspiring Data Scientist | Master's Student in Data Science**
