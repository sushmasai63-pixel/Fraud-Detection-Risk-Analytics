# Fraud Detection & Risk Analytics Dashboard

**SQL + Power BI | Fraud Detection, Risk Analysis & Investigation**

## Project Overview

This project analyzes transaction-level data to identify fraud patterns and risk indicators using **SQL Server and Power BI**.

The analysis focuses on transaction characteristics such as payment method, country, device risk, IP risk, account age, transaction velocity, and chargeback history.

The goal is to demonstrate how SQL-based analysis and Power BI visualization can support **fraud monitoring, risk investigation, and data-driven decision making**.

## Tools & Technologies

* SQL Server
* SQL
* Power BI
* DAX
* Excel / CSV

## Dataset

The dataset contains transaction-level records with fields including:

* Transaction ID
* Transaction Date
* Customer ID
* Country
* Device Type
* Payment Method
* Transaction Amount
* Account Age
* Previous Transactions
* Failed Login Count
* IP Risk Score
* Device Risk Score
* 24-hour Transaction Velocity
* Chargeback History
* Fraud Flag

## SQL Analysis

SQL was used to:

1. Calculate overall fraud metrics.
2. Analyze fraud by payment method.
3. Identify customers with elevated fraud activity.
4. Analyze individual risk indicators.
5. Develop a rule-based Fraud Risk Score.
6. Create a reusable SQL view for Power BI.

### Risk Score Logic

| Risk Indicator       | Condition             | Points |
| -------------------- | --------------------- | -----: |
| IP Risk              | Score > 70            |     20 |
| Device Risk          | Score > 70            |     20 |
| Transaction Velocity | > 10 transactions/24h |     20 |
| Account Age          | < 30 days             |     15 |
| Failed Logins        | > 5                   |     10 |
| Chargeback History   | Yes                   |     15 |

## Power BI Dashboard

The dashboard includes:

* Total Transactions
* Fraud Transactions
* Total Transaction Value
* Fraud Transaction Value
* Fraud Rate
* Fraud by Payment Method
* Fraud by Country
* Fraud Trend Over Time
* Fraud by Device Type
* Risk Level Distribution
* Risk Score Analysis
* Transaction-level investigation table
* Interactive filters

## Key Insights

* **IP Risk:** High IP-risk transactions had a **4.95% fraud rate**, compared with **2.07%** for normal IP-risk transactions.

* **Device Risk:** High device-risk transactions had a **3.98% fraud rate**, compared with **2.13%** for normal device-risk transactions.

* **Payment Method:** **Digital Wallet** transactions had the highest fraud rate at **2.36%**, followed by Debit Card at **2.31%** and Credit Card at **2.18%**.

* **Country:** **Australia** had the highest fraud rate at **2.55%**, while **India** had the highest number of fraud transactions (**174**) because of its larger transaction volume.

* **Investigation Approach:** Multiple transaction and account-level indicators were segmented and compared to identify areas requiring further investigation.

## Business Value

This project demonstrates how fraud data can be transformed into actionable analytical outputs by:

* Identifying higher-risk transaction segments
* Comparing fraud rates across transaction attributes
* Creating rule-based risk scoring
* Supporting investigation prioritization
* Converting SQL analysis into interactive Power BI dashboards
* Presenting transaction-level data for further review

## Skills Demonstrated

**SQL:** Data aggregation, CASE statements, GROUP BY, fraud-rate calculations, risk segmentation, SQL Views

**Power BI:** Dashboard development, KPI cards, interactive slicers, data visualization, risk analysis

**DAX:** Measures, calculated columns, conditional calculations

**Fraud & Risk Analytics:** Fraud pattern analysis, risk indicators, transaction monitoring, investigation prioritization, rule-based risk scoring
