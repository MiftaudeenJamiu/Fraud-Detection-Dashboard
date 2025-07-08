# Fraud-Detection-Dashboard

## Table of Contents 
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data analysis](data-analysis)
- [Visualisations and report](Visualisation-and-reports)
- [Results and Findings](#results-and-findings)
- [Conclusions](#conclusions)
- [Limitations](#limitations)

  
### Project Overview
---
This end-to-end fraud detection analytics project demonstrates the use of Python, SQL, and Power BI to simulate, clean, and analyse transactional data for over 10,000 users. It includes a custom-generated dataset with realistic patterns (e.g., weekend fraud spikes, payment method risks), a structured SQL data model, and an interactive Power BI dashboard that highlights fraud trends, user behaviours, and risk insights.

### Data Sources
---
The dataset [fraud_model_data.xlsx](https://github.com/user-attachments/files/21126499/fraud_model_data.xlsx) was custom-generated in Jupyter Notebook using Python to simulate over 10,000 realistic financial transactions for fraud analysis. Key fraud patterns were intentionally embedded, including weekend spikes, elevated risk associated with specific payment methods (e.g., credit cards), and a consistent 9% fraud rate to ensure analytical relevance. The data spans five years and includes randomised user demographics, device types, timestamps, and IP addresses, enabling robust fraud detection modelling. This controlled environment enables the testing and validation of end-to-end analytics workflows, simulating real-world scenarios without compromising data privacy or requiring access to sensitive information. 

### Tools
---
- Jupyter Notebook(Python) - Data Generation and Extraction
- Excel - Data Cleaning
- SQL Server - Data Analysis
- PowerBI - Creating Reports and Dashboards

### Data Cleaning 
---
The raw dataset generated in Python was cleaned using Excel before importing it into Power BI. The following steps were taken:
1.  Data Loading & Initial Review
   Opened each sheet (transactions, users, devices), scanned for blank fields, unusual values, and structural issues

2. Handling Missing Values
   Filtered and removed rows with missing UserID, TransactionAmount, or DeviceID
   Replaced nulls in optional fields (e.g., Gender, IP_Address) with "Unknown" or default values

3. Formatting
  Ensured TransactionDate was in the proper date-time format
  Formatted numeric columns (e.g., Transaction Amount, Age) consistently
  Standardised text case for categorical columns like PaymentMethod

4. Data Cleaning
 Removed duplicate entries across all sheets
 Checked for invalid or negative values and corrected them
 Verified IDs were consistent across related tables
 Preparation for Power BI
 Confirmed columns had appropriate headers

### Exploratory Data Analysis 
---
EDA involved identifying patterns, detecting outliers, analysing relationships between features, and verifying assumptions about fraud behaviour,  and to answer key questions such as;

-  How is fraud distributed over time?
-  Which users are most affected or involved in fraud?
-  Are certain payment methods more vulnerable to fraud?
-  What is the overall scale and impact of fraud?
-  What patterns exist across user profiles and behaviours?
-  Are fraud risks increasing or decreasing over time?
-  What device types and payment methods are most frequently used in fraudulent transactions?
-  Which demographic segments (e.g., age, gender, account status) are most associated with higher fraud rates?

### Data Analysis
---
As part of the data preparation process to create a report and dashboard in Power BI, some key activities are done, including;
- Initial Data Inspection: Queried tables to understand structure, row counts, and value distributions.
- Data Cleaning: Removed null or inconsistent entries (e.g., missing user IDs or transaction dates) and standardised column formats (e.g., dates, text casing).
- Data Integrity Checks: Ensured foreign key relationships (e.g., between users and transactions). Verified uniqueness of primary keys (like TransactionID, UserID).
- Feature Enhancement: Added and transformed columns, such as unique device and Fraud attempted rate by user.


### Visualisations and Reports
---
This section shows the Power BI dashboards built to detect fraud and analyse user activity. Each visual is designed to surface specific patterns, such as when fraud occurs, which users are involved, and which payment methods are most at risk, using actual transaction data.

- Fraud Detection Dashboard
1. Fraud Over Time: Line and column charts display monthly and daily trends in fraud volume.
2. Fraud by Payment Method: Visualises risk associated with different payment types (e.g., credit card, PayPal).
3. Fraud Count by User: Identifies high-risk users with frequent fraud attempts. 
4. KPI cards show overall transaction volume, fraud loss, YOY and MOM fraud amount and rates.

 See the shots below for an overview of the fraud detection dashboard
 
![Fraud Detection Dashboard](https://github.com/user-attachments/assets/bd3f4c18-66eb-495f-b179-e3bd03e44861)


- Users Insights
 Designed to drill into individual user activity:
  1. User-Level KPIs: First and latest transaction, total transactions, total fraud.
  2. Anomaly Score Trend: Line chart showing risk score variations.
  3. User Profile Table: Includes age, gender, IP address, device used, fraud attempts, and payment method.

 See the shots below for an overview of the user insights dashboard

![Users Insiights](https://github.com/user-attachments/assets/9e3536ef-a2bb-4ee5-93a4-8f3488c28ced)


### Results and Findings
---
This section outlines the major insights derived from the Power BI dashboards and analysis:
- Weekend Fraud Spikes: Fraudulent transactions consistently increased on weekends, indicating targeted timing.
- Payment Method Risk: PayPal had the highest fraud cases, followed by bank transfers, with credit cards showing the least.
- Repeat Offenders: A few users were responsible for most fraud attempts, pointing to repeated behaviour or compromised accounts.
- Device Usage: Mobile devices were the most common in fraud cases, compared to desktop or tablet access.
- Location & IP Patterns: Specific cities and IP ranges had more fraud activity, suggesting location-based targeting.
- High-Value Frauds: Fraudulent transactions often involve higher amounts, making them more financially damaging.
- Month-over-Month Change: Monthly fraud rates and amounts were tracked to monitor trends or new fraud surges.
- User-Level Reports: Drillthrough pages show each user’s full activity, including fraud history, demographics, and transaction behaviour.

### Conclusions
---
This project focused on simulating, analysing, and visualising transaction fraud using a complete data pipeline. I created a realistic dataset using Python, cleaned and structured the data in Excel, ran validation and exploration using SQL, and built the model and visuals in Power BI. The analysis uncovered specific fraud patterns, such as weekend-based spikes, high-risk payment methods, and user or device-level anomalies.

Visual dashboards in Power BI made these patterns easy to track. Users with repeated fraud attempts, mobile-based vulnerabilities, and high-value fraudulent transactions were all clearly identified. Drill-through reports allowed for the investigation of individual user behaviour across several attributes.

The goal was to build a practical fraud detection dashboard that can support decision-making and highlight where action is needed. The result is a working solution that demonstrates the ability to generate insights from raw data using real analytics tools.


### Limitations
---
Real financial data wasn’t available due to privacy restrictions, so the project uses simulated transactions. While patterns like weekend fraud and high-risk payment methods were replicated, real systems rely on richer data (e.g., device fingerprinting, and login history). This limits real-world accuracy, but the project effectively demonstrates key fraud analytics concepts and technical execution.

