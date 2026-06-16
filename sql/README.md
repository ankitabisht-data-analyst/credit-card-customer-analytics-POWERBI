# 📁 SQL Folder

Contains the database schema used to store and structure the raw data before loading it into Power BI.

| File | Description |
|---|---|
| `CC_AND_CUST_TABLE_CREATION.sql` | Creates the `CCDB` MySQL database with two tables: `cc_detail` (card/transaction data) and `cust_detail` (customer demographic data), matching the structure of the files in [`/data`](../data). |

**How to use:** Run this script in MySQL Workbench (or any MySQL client) first, then import the corresponding CSVs from `/data` into each table.
