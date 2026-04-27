# UPI Transaction Analysis Dashboard

## Project Overview

This project is a **Power BI dashboard** designed to analyze UPI transaction data.  
The dashboard provides insights into transaction amount, transaction volume, payment methods, banks, cities, customer behavior, and overall UPI usage patterns.

The main aim of this project is to convert raw transaction data into meaningful visual insights that can help in understanding digital payment trends.

---

## Project File

- **Project Name:** UPI Transaction Analysis
- **Tool Used:** Microsoft Power BI
- **File Type:** `.pbix`
- **Dashboard Type:** Business Intelligence / Data Analytics Dashboard

---

## Objectives

The main objectives of this project are:

- To analyze UPI transaction trends.
- To identify total transaction amount and transaction count.
- To compare transactions across different banks and payment methods.
- To understand customer transaction behavior.
- To visualize city-wise and category-wise UPI usage.
- To create an interactive Power BI dashboard for easy decision-making.

---

## Tools and Technologies Used

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **Data Cleaning**
- **Data Visualization**
- **Business Intelligence**

---

## Key Features of the Dashboard

- Interactive dashboard with filters and slicers.
- Analysis of total transaction amount.
- Transaction count analysis.
- Bank-wise transaction comparison.
- City-wise UPI transaction insights.
- Payment method-based analysis.
- Monthly or date-wise transaction trend visualization.
- Clean and user-friendly dashboard design.

---

## Dashboard Insights

This dashboard helps to understand:

- Which bank has the highest number of UPI transactions.
- Which city contributes the most to UPI payments.
- Which payment method is used most frequently.
- How transaction amount changes over time.
- Customer behavior in digital payment usage.
- Overall growth and performance of UPI transactions.

---

## Data Cleaning and Transformation

The dataset was cleaned and transformed using **Power Query** in Power BI.

Major steps included:

- Removing duplicate records.
- Handling missing values.
- Correcting data types.
- Formatting date columns.
- Creating calculated columns.
- Preparing data for visualization.

---

## DAX Measures Used

Some common DAX measures used in this project are:

```DAX
Total Transaction Amount = SUM('UPI Transactions'[Transaction Amount])

Total Transactions = COUNT('UPI Transactions'[Transaction ID])

Average Transaction Amount = AVERAGE('UPI Transactions'[Transaction Amount])

Success Transactions = 
CALCULATE(
    COUNT('UPI Transactions'[Transaction ID]),
    'UPI Transactions'[Transaction Status] = "Success"
)

Failed Transactions = 
CALCULATE(
    COUNT('UPI Transactions'[Transaction ID]),
    'UPI Transactions'[Transaction Status] = "Failed"
)

Success Rate = 
DIVIDE(
    [Success Transactions],
    [Total Transactions],
    0
)
