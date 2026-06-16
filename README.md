# 💳 Credit Card & Customer Insights Dashboard | Power BI Project

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/excel)

## 📌 Project Overview
This project is an end-to-end **Credit Card Transactions & Customer Analytics** solution built with **MySQL, Excel, and Power BI**. It analyzes 10,000+ customer credit card records to uncover revenue trends, transaction behavior, customer demographics, and credit risk indicators — packaged into two interactive executive dashboards (Transaction Report and Customer Report) with cross-filtering, drill-downs, and KPI cards.

**Goal:** Help a financial services stakeholder identify which card categories, customer segments, and channels drive revenue and risk, in order to support credit limit, marketing, and retention decisions.

## 🎯 Business Problem
Credit card issuers need visibility into who their profitable customers are, which products generate the most revenue/interest, and where delinquency or low engagement risk is concentrated. This dashboard answers:
- Which card category (Blue/Silver/Gold/Platinum) drives the most revenue and interest income?
- How does revenue trend by quarter, week, and transaction channel (Swipe/Chip/Online)?
- Which customer segments (age, income, education, job, marital status, state) generate the most value?
- How do dependents, income group, and credit limit relate to revenue and satisfaction?

## 🗂️ Dataset
Two relational tables, created in a MySQL database (`CCDB`) and joined on `Client_Num`:

| Table | Description | Rows | Key Fields |
|---|---|---|---|
| `cc_detail` | Card-level transaction data | ~10,000+ | Card_Category, Credit_Limit, Total_Trans_Amt, Total_Revolving_Bal, Interest_Earned, Use_Chip, Exp_Type |
| `cust_detail` | Customer demographic data | ~10,000+ | Customer_Age, Gender, Income, Education_Level, Marital_Status, State_cd, Cust_Satisfaction_Score |

Raw data: [`/data`](./data) · Schema: [`/sql/CC_AND_CUST_TABLE_CREATION.sql`](./sql/CC_AND_CUST_TABLE_CREATION.sql)

## 🛠️ Tech Stack & Process
1. **MySQL** – Designed schema and created the `CCDB` database with `cc_detail` and `cust_detail` tables (see `/sql`).
2. **Excel** – Initial data cleaning, validation, and exploratory checks (see `/excel`).
3. **Power BI** – Data modeling (star-schema join on Client_Num), DAX measures (Sum of Revenue, Total Interest Earned, Avg Utilization Ratio), and dashboard design with slicers for Quarter, Week, Gender, Income Group, and Card Category.

## 📊 Dashboard 1 — Credit Card Transaction Report
![Credit Card Transaction Dashboard]("C:\Users\Tanub\OneDrive\Documents\PowerBI Dashboards\power bi dashbaord2\cedit card dashboard.png")

**Key Insights:**
- Total Revenue: **55.32M** | Transaction Amount: **45M** | Total Interest: **7.84M** | Transaction Count: **656K**
- **Blue** card category alone drives **₹4.61 Crore+ (4,61,39,397.74)** in revenue — the dominant product line.
- Revenue and transaction volume both **peak in Q3** before declining in Q4.
- **Swipe** is the leading transaction channel, far ahead of Chip and Online.
- **Bills** and **Entertainment** are the top spending categories by revenue.

## 👤 Dashboard 2 — Credit Card Customer Report
![Customer Dashboard](./images/customer_dashboard.png)

**Key Insights:**
- Total Income across customers: **576M** | Customer Satisfaction Score (CSS): **3.19**
- **Male customers (30M)** generate higher revenue than female customers (25M).
- **40–50 age group** is the highest revenue-generating segment.
- **Texas, New York, and California** are the top 3 revenue-generating states.
- **High-income** customers contribute the largest revenue share (22M) vs. medium and low-income groups.
- **Married** customers outspend Single and Unknown marital-status groups.

## 🚀 How to Use This Project
```bash
git clone https://github.com/<your-username>/credit-card-customer-analytics-powerbi.git
```
1. Create a MySQL database named `CCDB` and run [`CC_AND_CUST_TABLE_CREATION.sql`](./sql/CC_AND_CUST_TABLE_CREATION.sql) to create the schema.
2. Import `data/credit_card.csv` and `data/cust_add.csv` into the `cc_detail` and `cust_detail` tables (e.g. via MySQL Workbench's Table Data Import Wizard).
3. Open [`powerbi/credit_card-report.pbix`](./powerbi/credit_card-report.pbix) in Power BI Desktop and refresh the data source to point to your local MySQL connection.

## 📈 Skills Demonstrated
`MySQL` `Data Modeling` `DAX` `Power BI` `Data Cleaning` `Excel` `ETL` `Data Visualization` `Business Analytics` `Dashboard Design` `KPI Reporting`

## 📬 Contact
**Ankita Bisht** — Data Analyst
[LinkedIn](https://www.linkedin.com/in/ankita-bisht09) 
