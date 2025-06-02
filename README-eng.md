# Sales Strategy Analysis for "Pens and Printers"
Analysis of 3 new different sales methods in online store for office supplies
## Project Overview
This project focuses on analyzing new sales methods for a recently launched product line in an online stationery store - Pens and Printers. The company, founded in 1984, offers a wide range of office supplies from trusted manufacturers. As customer purchasing behaviors evolve, the company aims to optimize sales strategies for better efficiency and profitability.
### This project was completed as the practical component of the Data Analyst certification offered by DataCamp 

## Projekt Goals
Evaluate the effectiveness of three different sales strategies - Email, Phone Call, and Email + Call — used to promote a new product line focused on creativity and brainstorming tools.

## Objectives
- Clean and preprocess the dataset using SQLL, Python.
- Analyze spread of customers overall and for each method, difference of revenue for each method, define the most effective sales method. 
- Visualize key insights to uncover trends and patterns.
- 
## Dataset Summary
Dataset product_sales is uploaded

The dataset consists of 15,000 customer records with attributes including:

Customer ID

Sales Method

Revenue

Years as Customer

Region

Date of Contact

### 🔧 Data Cleaning & Preprocessing

Cleaned dataset is uploaded

✔️ Data Validation

Loaded and inspected the dataset in Google Colab.

Checked for missing values and outliers.

✔️ Missing Revenue Handling

1,074 missing values (~7.16%) in the revenue column.

Assumed MCAR (Missing Completely At Random).

Filled missing values using mean imputation.

✔️ Outlier Correction

Two outliers in years_as_customer (47 and 63 years).

Replaced with 41 (maximum possible value, based on company history).

✔️ Categorical Standardization

Standardized sales_method values (e.g., 'em + call' → 'Email + Call') for consistency.

### 📈 Analysis & Visualizations

Performed analysis and created interactive dashboards using Power BI, including:

Customer Count by Sales Method

Revenue Distribution

Revenue by Sales Method

Revenue Over Time by Method

### Key Insight: Sales Method Efficiency
Sales Method: Email (7,466 Customers,  $723,418	Total Revenue, $96.9 ARPC (Avg Revenue/Customer))

Sales Method: Phone Call (4,962 Customers,  $244,566 Total Revenue, $49.29 ARPC (Avg Revenue/Customer))

Sales Method: Email + Call (2,572 Customers,  $441,040 Total Revenue, $171.48 ARPC (Avg Revenue/Customer))

Email was the most scalable but less profitable per customer.

Email + Call generated the highest ARPC, indicating strong engagement.

Phone Calls required the most time (30 min/customer) but yielded the lowest ARPC.

### 📐 Metric for Ongoing Monitoring

Metric: Average Revenue per Customer (ARPC) by Sales Method

Formula:
ARPC = Total Revenue by Method / Number of Customers in Method

Why ARPC?

- Normalizes revenue across sales methods.
- Simple to calculate and track.
- Allows meaningful comparison over time.

### 📌 Recommendations
Prioritize "Email + Call" method for high-value clients due to highest revenue efficiency.

Reduce or eliminate "Phone Call" only strategy - high time cost, low returns.

Improve Email campaigns - initial results were strong, but effectiveness declined over time. Investigate and optimize.

### 🛠️ Tools Used
DBeaver (SQL) - for data cleaning, preprocessing and analysis

Google Colab (Python (Pandas, NumPy, Matplotlib)) - for data cleaning, preprocessing and analysis

Power BI (for interactive dashboarding)

GitHub (for version control)

## 📁 Folder Structure
├── product_sales.csv                      # Original dataset

├── cleaned_product_sales.csv              # Raw and cleaned datasets

├── Practical_Exam_DataCamp.ipynb          # Jupyter/Colab analysis files

├── visuals/ Customers_by_approach.png     # Screenshots or reports from Power BI

├──           Overall_Revenue_Distribution.png
            
├──          Revenue_by_sales_method.png
            
├──          Revenue_by_week_and_method.png

├── Presentatation Product Sales.pdf      # Overview presentation for Head of Analytic
            
├── README.md                # Project overview

### 🚀 Future Work
 - Automate dashboard updates via cloud data pipelines.
 - Include A/B testing for new sales methods.
 - Further segment customers by region or industry.
