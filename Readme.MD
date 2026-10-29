# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analytics project focused on understanding customer purchasing patterns, spending behavior, product preferences, subscription trends, and customer loyalty using **Python, SQL, and Power BI**.

The project analyzes 3,900 purchase records to identify meaningful business insights and help retailers improve customer engagement, marketing strategies, and long-term customer retention.

## 📌 Project Overview

Retail businesses need to understand what influences customers' purchasing decisions, how discounts affect spending, which products receive better ratings, and whether subscription programs encourage customer loyalty.

This project uses customer shopping data to answer important business questions through data preparation, SQL-based analysis, and interactive Power BI visualization.

### 🎯 Project Objectives

* Analyze customer spending patterns across genders and age groups.
* Identify high-spending customers who use discounts.
* Determine the highest-rated and most frequently purchased products.
* Compare purchasing behavior across shipping methods.
* Evaluate subscriber and non-subscriber spending.
* Analyze discount dependency across product categories.
* Segment customers based on their previous purchases.
* Investigate the relationship between repeat purchases and subscriptions.
* Develop actionable business recommendations from the findings.

## 🛠️ Technology Stack

| Technology       | Purpose                                               |
| ---------------- | ----------------------------------------------------- |
| Python           | Data cleaning, preprocessing, and feature engineering |
| Pandas           | Data manipulation and analysis                        |
| NumPy            | Numerical operations                                  |
| SQL (PostgreSQL) | Business queries and customer analysis                |
| Power BI         | Interactive dashboards and visualization              |
| CSV              | Dataset storage and data exchange                     |
| Git & GitHub     | Version control and project sharing                   |

## 📂 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── customer_shopping_behavior.csv
│
├── customer_behavior_sql_queries.sql
│
├── customer_behavior_dashboard.pbix
│
├── Customer_Shopping_Behavior_Analysis.pdf
│
├── Business_Problem_Document.pdf
│
├── Customer_Shopping_Behavior_Analysis.pptx
│
└── README.md
```

*Note: The filenames above are descriptive. The actual filenames in the repository may differ.*

## 📊 Dataset Description

The dataset contains **3,900 rows and 18 columns**, representing customer shopping transactions and purchasing preferences.

### Dataset Features

| Feature                | Description                             |
| ---------------------- | --------------------------------------- |
| Customer ID            | Unique customer identifier              |
| Age                    | Customer age                            |
| Gender                 | Customer gender                         |
| Item Purchased         | Product purchased                       |
| Category               | Product category                        |
| Purchase Amount (USD)  | Purchase amount in US dollars           |
| Location               | Customer location                       |
| Size                   | Product size                            |
| Color                  | Product color                           |
| Season                 | Purchase season                         |
| Review Rating          | Customer's product rating               |
| Subscription Status    | Whether the customer has a subscription |
| Shipping Type          | Selected shipping method                |
| Discount Applied       | Whether a discount was applied          |
| Promo Code Used        | Whether a promotional code was used     |
| Previous Purchases     | Number of previous purchases            |
| Payment Method         | Customer's payment method               |
| Frequency of Purchases | Customer's purchase frequency           |

### Data Quality

The project report identifies 37 missing values in the `Review Rating` column. The documented cleaning process fills these missing values using the median review rating for each product category.

Additional preprocessing includes standardizing column names, creating customer age groups, and engineering purchase-frequency features.

## 🐍 Python Data Preparation

The documented Python workflow includes:

* Loading and inspecting the dataset using Pandas.
* Exploring data types, descriptive statistics, and missing values.
* Handling missing review ratings using category-level median values.
* Standardizing column names into snake_case.
* Creating age groups for customer segmentation.
* Engineering purchase-frequency features.
* Examining the relationship between discount usage and promotional codes.
* Preparing the cleaned data for PostgreSQL analysis.

**Note:** The provided project archive contains the CSV dataset and supporting documentation, but does not include a standalone Python preprocessing script.

## 🗄️ SQL Business Analysis

The SQL queries use customer transaction data to investigate ten business questions.

### 1. Revenue by Gender

Compare total revenue generated by male and female customers.

### 2. High-Spending Discount Users

Identify customers who used discounts but spent at least the average purchase amount.

### 3. Top 5 Products by Review Rating

Find products with the highest average customer review ratings.

### 4. Shipping Type Comparison

Compare average purchase amounts for Standard and Express shipping.

### 5. Subscribers vs. Non-Subscribers

Compare customer counts, average spending, and total revenue by subscription status.

### 6. Discount-Dependent Products

Identify products with the highest percentage of discounted purchases.

### 7. Customer Segmentation

Classify customers into New, Returning, and Loyal segments using previous purchase counts.

### 8. Top Products by Category

Find the three most purchased products within each product category.

### 9. Repeat Buyers and Subscriptions

Examine subscription status among customers with more than five previous purchases.

### 10. Revenue by Age Group

Calculate the revenue contribution of different customer age groups.

## 📈 Power BI Dashboard

The project includes a Power BI dashboard designed to present customer shopping behavior in a visual and accessible format.

The analysis supports exploration of:

* Customer purchasing patterns.
* Spending and revenue distribution.
* Product popularity and customer ratings.
* Discount usage.
* Subscription behavior.
* Customer loyalty and repeat purchases.
* Demographic purchasing trends.
* Shipping preferences.

The dashboard helps transform transaction-level data into insights that can support retail business decisions.

## 🚀 How to Use This Project

### Step 1: Download the Repository

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

Navigate to the project directory:

```bash
cd Customer-Shopping-Behavior-Analysis
```

### Step 2: Explore the Dataset

Install the core Python libraries:

```bash
python -m pip install pandas numpy matplotlib seaborn
```

Load the CSV file in Python:

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")

print(df.head())
print(df.shape)
print(df.info())
print(df.isnull().sum())
```

### Step 3: Run the SQL Analysis

1. Install PostgreSQL if it is not already installed.
2. Create a database for the project.
3. Import `customer_shopping_behavior.csv` into a table named `customer`.
4. Standardize the column names or update the SQL queries to match your table schema.
5. Open `customer_behavior_sql_queries.sql` in your SQL client.
6. Execute the queries to answer the business questions.

**Important:** The provided SQL queries expect columns such as `purchase_amount`, `customer_id`, and `age_group`. Ensure the imported table uses the corresponding cleaned column names before executing the queries.

### Step 4: Open the Power BI Dashboard

1. Open Power BI Desktop.
2. Open `customer_behavior_dashboard.pbix`.
3. Check the dataset source and update its location if necessary.
4. Refresh the data model.
5. Explore the available visualizations and insights.

## 💡 Business Recommendations

Based on the project's analytical objectives, the following strategies can be investigated:

**1. Improve Subscription Adoption**
Explore subscription benefits and targeted campaigns to encourage customer sign-ups.

**2. Strengthen Customer Loyalty**
Develop loyalty programs and personalized offers for repeat customers.

**3. Optimize Discount Strategies**
Evaluate discount usage alongside purchase amounts and profitability before changing promotional policies.

**4. Promote Popular Products**
Use product ratings and purchase frequency to identify products worth highlighting in marketing campaigns.

**5. Personalize Marketing**
Use customer age groups, purchasing preferences, and spending patterns to develop relevant campaigns.

**6. Improve Shipping Strategy**
Compare shipping preferences and spending behavior to understand customer expectations.

These recommendations should be validated against the actual SQL results and Power BI findings before implementation.

## 🔮 Future Improvements

* Add a reproducible Python data-cleaning script.
* Automate data loading into PostgreSQL.
* Develop customer segmentation models.
* Build a customer purchase prediction model.
* Add automated data-quality checks.
* Publish an interactive online analytics application.
* Improve dashboard reporting with additional business KPIs.

## 👨‍💻 Author

**Yashraj Rajput**

B.Tech in Data Science | Aspiring Data Analyst

**Technical Interests:** Data Analytics | SQL | Python | Power BI | Business Intelligence

---

⭐ If you find this project useful, feel free to explore the repository and share feedback.
