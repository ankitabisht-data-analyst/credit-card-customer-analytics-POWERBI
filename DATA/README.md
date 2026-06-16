# 📁 Data Folder

This folder contains the raw source data used in this project.

| File | Description | Rows | Key Columns |

| `credit_card.csv` | Card-level transaction & usage data per customer | 10,000+ | 
Client_Num, Card_Category, Annual_Fees, Credit_Limit, Total_Revolving_Bal, Total_Trans_Amt, Total_Trans_Vol, Avg_Utilization_Ratio, Use_Chip, Exp_Type, Interest_Earned, Delinquent_Acc |


| `cust_add.csv` | Customer demographic & profile data | 10,000+ | 
Client_Num, Customer_Age, Gender, Dependent_Count, Education_Level, Marital_Status, State_cd, Zipcode, Car_Owner, House_Owner, Personal_loan, Customer_Job, Income, Cust_Satisfaction_Score |

Both files share `Client_Num` as the common key and are joined in MySQL (see [`/sql`](../sql)) to build the unified data model used in Power BI.

**Note:** Data is anonymized/sample data for portfolio and analysis purposes only.
