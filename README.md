# 📊 Customer Churn Analysis | Python, SQL & Data Visualization

## 📌 Project Overview

Customer churn is an important business metric that helps organizations understand why customers discontinue their subscriptions. Analyzing churn patterns enables businesses to identify at-risk customers, understand cancellation reasons, and develop strategies to improve customer retention.

This project analyzes customer, subscription, and support data using **Python, SQL (SQLite), Pandas, NumPy, Matplotlib, and Seaborn**. The analysis includes data cleaning, data integration, KPI calculation, churn-risk segmentation, and exploratory data visualization.

The goal is to transform raw customer data into meaningful insights that support data-driven business decisions.

## 🎯 Project Objectives

- Calculate overall customer churn and retention rates.
- Analyze churn across subscription plans and contract types.
- Identify common customer cancellation reasons.
- Examine customer tenure and monthly charges in relation to churn.
- Evaluate customer support escalations and satisfaction-related information.
- Segment customers into low-, medium-, and high-churn-risk categories.
- Visualize trends and patterns to support customer retention strategies.

## 🛠️ Tools & Technologies

| Technology | Purpose |
|---|---|
| Python | Data analysis and feature engineering |
| Pandas | Data cleaning, transformation, and merging |
| NumPy | Conditional calculations and numerical operations |
| SQLite | Database connectivity and data extraction |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive analysis and documentation |

## 🗂️ Dataset Description

The analysis uses three database tables stored in a SQLite database named `customer_churn.db`.

| Table | Description |
|---|---|
| `db_customer` | Customer details, including name, country, state, gender, and date of birth |
| `db_subscription` | Subscription dates, plan type, contract type, cancellation information, monthly charges, customer lifetime value (CLTV), and churn score |
| `db_support` | Customer complaint dates, support escalations, customer satisfaction scores, and complaint information |

The tables are connected using `customerid`. The data is cleaned and prepared before the customer, subscription, and support information is combined for analysis.

**Note:** The original SQLite database is a separate input file and must be supplied locally to reproduce the analysis.

## 🔄 Project Workflow

### 1. Database Connection & Data Extraction
- Connected Python to SQLite using `sqlite3`.
- Identified available database tables.
- Extracted table data into Pandas DataFrames.
- Inspected table structures, columns, and data types.

### 2. Data Cleaning & Preparation
- Standardized column names and gender categories.
- Converted date columns into appropriate datetime formats.
- Examined and handled missing values.
- Removed unnecessary columns.
- Reviewed duplicate customer-support records and retained the latest complaint record per customer for the merged analysis.

### 3. Data Integration
- Merged customer, subscription, and support information using `customerid`.
- Created a consolidated dataset for analysis.
- Exported the processed data to `exported_churn_data.csv`.

### 4. Feature Engineering
Created additional fields to support analysis:

- **Churn Flag:** Identifies whether a customer has a cancellation date.
- **Tenure:** Calculates the duration of a customer's subscription.
- **Churn Risk:** Classifies customers based on their churn score:
  - Low Risk: Score below 50
  - Medium Risk: Score from 50 to below 70
  - High Risk: Score of 70 or above
- **Complaint Count:** Calculates the number of support records per customer before selecting the latest record for the consolidated dataset.
- **Cancellation Month:** Supports monthly churn trend analysis.

### 5. KPI Analysis
Calculated key business metrics, including churn rate, retention rate, average monthly charges, revenue at risk, escalation rate, and average complaints per customer.

### 6. Exploratory Data Analysis & Visualization
Created visualizations to explore:

- Monthly customer churn trends.
- Churn rates by subscription plan.
- Churn rates by state.
- Churn rates by contract type.
- Customer cancellation reasons.
- Churn patterns by customer tenure.
- Monthly charges and customer lifetime value in relation to churn.
- Relationships among selected numerical and categorical features.

## 📈 Key Results

The following metrics were reported by the notebook for the analyzed dataset.

| KPI | Result |
|---|---:|
| Customer Churn Rate | 29.89% |
| Customer Retention Rate | 70.11% |
| Average Monthly Charges | 23.33 |
| Revenue at Risk | 138,780.15 |
| Support Escalation Rate | 31.12% |

*These results reflect the dataset and calculations used in the notebook. Revenue figures should be interpreted using the source dataset's currency and business definitions.*

### 🔍 Selected Findings

- **Overall churn:** Approximately 29.89% of customers were classified as churned.
- **Plan comparison:** The Standard plan showed a churn rate of approximately 30.23%, compared with 29.73% for Basic and 29.72% for Premium.
- **Contract comparison:** Monthly and annual contract customers had similar reported churn rates of 29.84% and 29.95%, respectively.
- **Cancellation reasons:** Poor streaming quality, forgotten trial cancellations, switching to competitors, high cost, and insufficient content were among the recorded reasons for churn.
- **Retention opportunity:** These patterns can help businesses prioritize service quality, customer communication, pricing, and retention initiatives for further investigation.

These are descriptive findings rather than proof that any individual factor causes churn.

## 💡 Business Value

This project demonstrates how customer data can be converted into actionable business information.

Potential applications include:

- Identifying customer segments that require closer monitoring.
- Prioritizing retention campaigns for customers with higher churn scores.
- Understanding cancellation patterns across plans, locations, and contract types.
- Investigating the relationship between customer support experiences and churn.
- Monitoring revenue exposure associated with customer cancellations.
- Supporting evidence-based customer retention planning.

## 🚀 Getting Started

### Prerequisites

Install Python and Jupyter Notebook. The following libraries are required:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

SQLite connectivity is provided by Python's built-in `sqlite3` module, so a separate Python package is not required for the notebook's database connection.



This structure is a suggested organization. Include the database, exported CSV, and chart files only if you have the actual files and permission to share them.

## 🔮 Future Improvements

- Build an interactive dashboard using Power BI or Tableau.
- Develop a machine-learning model to predict customer churn.
- Evaluate model performance using appropriate classification metrics.
- Automate data extraction and recurring KPI reporting.
- Investigate customer retention opportunities using cohort analysis.
- Improve data validation and test how missing or duplicate records affect results.

## 👨‍💻 Skills Demonstrated

**Python | SQL | SQLite | Pandas | NumPy | Data Cleaning | Data Wrangling | Feature Engineering | Exploratory Data Analysis (EDA) | KPI Analysis | Data Visualization | Business Insights**

