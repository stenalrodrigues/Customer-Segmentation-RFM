
## Customer Segmentation & RFM Analysis

📌 Project Overview

This project analyzes retail transaction data to understand customer purchasing behavior and identify meaningful customer segments.

The project combines SQL and Python to perform data cleaning, exploratory analysis, RFM analysis, and customer segmentation using K-Means clustering.

## 🎯 Business Objectives
Identify high-value customers
Understand customer purchasing behavior
Analyze Recency, Frequency, and Monetary value
Identify inactive customers
Segment customers based on purchasing behavior
Generate actionable customer retention strategies

## 🛠️ Tools & Technologies
SQL / MySQL
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
K-Means Clustering

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

## The SQL analysis covers:

Database and table creation
Data-quality checks
Missing-value analysis
Duplicate checks
Cancelled transaction analysis
Quantity and price validation
Data cleaning
Revenue analysis
Customer-level RFM calculation
RFM scoring
Rule-based customer segmentation
Revenue by customer segment
Top customer and product analysis
Monthly sales analysis

The SQL workflow creates RFM scores and classifies customers into segments such as Champions, Cannot Lose Them, At Risk, Loyal Customers, Potential Loyalists, New Customers, Lost Customers, Hibernating, and Needs Attention.

## 🐍 Python / Jupyter Notebook

The Jupyter Notebook includes:

Data cleaning and preprocessing
Feature engineering
Exploratory Data Analysis
Revenue and sales analysis
RFM analysis
RFM visualization
Log transformation
Feature scaling
K-Means clustering
Silhouette Score analysis
Customer segment profiling
Business recommendations

## Segmentation Approach

Two segmentation approaches were used in this project. SQL-based RFM scoring was used to create interpretable, rule-based customer segments such as Champions, Loyal Customers, At Risk, and Lost Customers. 
Python was then used to apply K-Means clustering to the RFM features and identify natural customer groupings. The optimal K-Means solution was K=2 with a Silhouette Score of 0.4328.

## 📊 Key Results

The analysis identified 4,338 customers for customer-level segmentation.

Different values of K were evaluated using the Silhouette Score. The best result was:

Optimal K: 2

Silhouette Score: 0.4328

Final Customer Segments
Customer Segment	Customers	Avg. Recency	Avg. Frequency	Avg. Monetary
High-Value Loyal Customers	1,666	25.89 days	8.44	£4,539.60
Inactive Low-Value Customers	2,672	134.09 days	1.67	£495.59
💡 Business Insights
High-Value Loyal Customers

These customers purchase more frequently, have purchased more recently, and generate significantly higher monetary value.

## Recommended strategies:

Loyalty rewards
Personalized offers
VIP programs
Cross-selling and upselling
Inactive Low-Value Customers

This segment represents a large portion of the customer base and shows lower purchasing frequency and monetary value.

## Recommended strategies:

Win-back campaigns
Personalized discounts
Re-engagement emails
Targeted product recommendations
📂 Repository Structure
Customer-Segmentation-RFM/
│
├── README.md
├── customer_segmentation_rfm.ipynb
└── customer_segmentation_rfm.sql

customer_segmentation_rfm.ipynb

Python-based analysis, visualization, RFM analysis, and K-Means customer segmentation.

customer_segmentation_rfm.sql

SQL-based data cleaning, business analysis, RFM scoring, and rule-based customer segmentation.

👤 Author

Stenal Rodrigues

Data Analyst | Aspiring Data Scientist | Master's Student in Data Science
