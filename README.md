# Customer Segmentation & RFM Analysis

## 📌 Project Overview

I worked on this project to understand how customers behave based on their purchase history.

I used **SQL and Python** to clean and analyze retail transaction data, calculate **RFM (Recency, Frequency, Monetary)** values, create customer segments, and apply **K-Means clustering** to see whether customers could be grouped based on their purchasing behavior.

Through this project, I wanted to answer a few questions:

* Who are the most valuable customers?
* Which customers have not purchased recently?
* How often do customers make purchases?
* Which customers should a business focus on for retention?
* Can customers be grouped based on their buying behavior?

At the end, I used the results to suggest some simple customer retention and re-engagement strategies.


## 🎯 Business Objectives

The main objectives of this project were to:

* Identify high-value customers
* Understand customer purchasing patterns
* Calculate Recency, Frequency, and Monetary values
* Find inactive customers
* Create meaningful customer segments
* Compare rule-based segmentation with K-Means clustering
* Suggest possible strategies for different customer groups


## 🛠️ Tools & Technologies

* **SQL / MySQL**
* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **K-Means Clustering**


## 📂 Dataset

I used the **Online Retail Dataset** from the UCI Machine Learning Repository.

The original dataset contains **541,909 transaction records** from a UK-based online retailer between **December 2010 and December 2011**.

Since the original dataset is large, I have not included the complete dataset in this repository. I have included a sample file called `Online Retail DATA - Sample.csv` for reference.

The full dataset was used for the analysis and the results shown in this project.

**Dataset Source:**
[UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)


# 🔄 Project Workflow

```text
Raw Retail Data
       ↓
Data Quality Checks
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
RFM Analysis
       ↓
RFM Scoring
       ↓
Customer Segmentation
       ↓
K-Means Clustering
       ↓
Segment Analysis
       ↓
Business Insights
```

# 🗄️ SQL Analysis

I used SQL for the initial data cleaning, analysis, and customer segmentation.

### Data Cleaning & Quality Checks

I performed checks for:

* Missing values
* Duplicate records
* Cancelled transactions
* Invalid quantities
* Invalid prices
* Missing customer information
* Revenue calculation

### Business Analysis

I also used SQL to analyze:

* Monthly sales
* Revenue by customer
* Top customers
* Top-selling products
* Customer purchasing behavior

### RFM Analysis

I calculated three metrics for each customer:

**Recency**
How recently the customer made a purchase.

**Frequency**
How often the customer made purchases.

**Monetary**
How much the customer spent.

I then used these values to assign RFM scores and create customer segments.

Some of the segments included:

* Champions
* Cannot Lose Them
* At Risk
* Loyal Customers
* Potential Loyalists
* New Customers
* Lost Customers
* Hibernating
* Needs Attention

# 🐍 Python Analysis

I used Python for the exploratory analysis and machine-learning part of the project.

The notebook includes:

* Loading and understanding the data
* Data cleaning
* Feature engineering
* Exploratory Data Analysis
* Revenue analysis
* Customer-level analysis
* RFM calculation
* RFM visualizations
* Log transformation
* Feature scaling
* K-Means clustering
* Silhouette Score analysis
* Customer cluster profiling
* Business recommendations

# 🎯 Customer Segmentation

I used two different approaches to segment customers.

## 1. SQL-Based RFM Segmentation

The first approach uses predefined RFM rules.

For example, customers who purchase frequently, spend more, and have purchased recently can be considered high-value customers.

I used this approach because it makes the customer groups easier to understand from a business point of view.

The SQL analysis creates segments such as:

* Champions
* Loyal Customers
* At Risk
* Lost Customers
* Potential Loyalists
* Hibernating
* Needs Attention

## 2. K-Means Clustering

For the second approach, I used **K-Means clustering** to group customers based on their RFM values.

Before applying K-Means, I:

1. Created the RFM features
2. Checked the feature distributions
3. Applied log transformation where needed
4. Scaled the features
5. Tested different values of K
6. Compared the Silhouette Scores
7. Selected the best-performing K
8. Looked at the characteristics of each cluster

Among the K values I tested, **K = 2 gave the highest Silhouette Score of 0.4328**.

I then looked at the average Recency, Frequency, and Monetary values of each cluster to understand what type of customers were in each group.

The cluster names are my interpretation of the customer behavior. K-Means itself only creates the clusters; it does not give them names such as "High-Value Loyal Customers."


# 📊 Key Results

After data cleaning and customer-level filtering, **4,338 customers** were included in the segmentation analysis.

### K-Means Results

| Metric             | Result |
| ------------------ | -----: |
| Customers Analyzed |  4,338 |
| Best K             |      2 |
| Silhouette Score   | 0.4328 |

### Customer Segments

| Customer Segment             | Customers | Avg. Recency | Avg. Frequency | Avg. Monetary |
| ---------------------------- | --------: | -----------: | -------------: | ------------: |
| High-Value Loyal Customers   |     1,666 |   25.89 days |           8.44 |     £4,539.60 |
| Inactive Low-Value Customers |     2,672 |  134.09 days |           1.67 |       £495.59 |

# 💡 What I Found

## ⭐ High-Value Loyal Customers

This group contains **1,666 customers**.

Compared with the other group, these customers:

* Purchased more recently
* Purchased more frequently
* Generated much more revenue

I would consider these customers important for the business because they already show strong purchasing behavior.

### Possible strategies

* Loyalty rewards
* VIP offers
* Personalized discounts
* Cross-selling and upselling
* Product recommendations
* Early access to new products

The main focus would be to **keep these customers engaged and encourage them to continue purchasing**.


## 💤 Inactive Low-Value Customers

This group contains **2,672 customers**.

These customers had:

* Higher recency
* Lower purchase frequency
* Lower monetary value

This suggests that many customers in this group have not purchased recently and may need some re-engagement.

### Possible strategies

* Win-back campaigns
* Re-engagement emails
* Personalized offers
* Limited-time discounts
* Product recommendations
* Special offers for returning customers

The main goal would be to **try to bring some of these customers back**.


# 📈 Business Takeaways

One of the main things I learned from this project is that customers do not all behave in the same way.

A smaller group of customers is purchasing more frequently, purchasing more recently, and generating much higher revenue. These customers could be targeted with loyalty and retention strategies.

A larger group of customers is less active and contributes less revenue. Instead of sending the same campaign to everyone, a business could use customer segments to target different groups differently.


# 🔍 SQL Segmentation vs K-Means

I used both approaches because they helped me look at the customers in two different ways.

| Approach             | What it does                                             |
| -------------------- | -------------------------------------------------------- |
| SQL RFM Segmentation | Groups customers using predefined business rules         |
| K-Means Clustering   | Groups customers based on similarities in their behavior |

The two approaches do not have to produce the same segments.

The SQL approach is based on **rules that can be explained easily**, while K-Means is a **machine-learning approach that finds groups from the data**.

Using both approaches helped me understand the difference between business-based segmentation and unsupervised machine learning.


# 📂 Repository Structure

```text
Customer-Segmentation-RFM/
│
├── README.md
├── customer_segmentation_rfm.ipynb
├── customer_segmentation_rfm.sql
└── Online Retail DATA - Sample.csv
```

### `customer_segmentation_rfm.ipynb`

The notebook contains:

* Data cleaning
* Exploratory Data Analysis
* RFM analysis
* Visualizations
* Feature engineering
* K-Means clustering
* Silhouette Score analysis
* Customer profiling
* Business recommendations

### `customer_segmentation_rfm.sql`

The SQL file contains:

* Data quality checks
* Data cleaning
* Revenue analysis
* Monthly sales analysis
* RFM calculation
* RFM scoring
* Rule-based segmentation
* Customer analysis
* Product analysis

# 🎓 What I Learned

Working on this project helped me practice both technical and business-related skills.

I learned how to:

* Clean and work with a real-world retail dataset
* Use SQL to analyze customer and sales data
* Calculate RFM metrics
* Perform exploratory data analysis in Python
* Prepare data for machine learning
* Apply K-Means clustering
* Use Silhouette Score to compare clustering results
* Interpret customer segments
* Connect data analysis results with possible business strategies


# 👤 About Me

**Stenal Rodrigues**

**Data Analyst | Aspiring Data Scientist 

I created this project to practice my SQL, Python, and machine-learning skills using a real-world retail dataset. It helped me understand how customer transaction data can be analyzed and turned into useful business insights.
