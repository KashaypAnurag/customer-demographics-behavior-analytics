# customer-demographics-behavior-analytics

# Enterprise Customer Demographics & Behavioral Analytics

A comprehensive data analytics repository engineered to process customer profiles, track transaction frequencies, and extract consumer purchasing patterns. This project combines exploratory data analysis (EDA), automated data cleaning pipelines, and customer segmentation matrices to deliver actionable marketing intelligence and optimize lifetime account value.

---

## 1. Project Objective & Core Business Impacts

The goal of this framework is to analyze underlying demographic trends, map account enrollment velocities, and isolate core behaviors across our active customer network:

*   **Total Customer Footprint:** Comprehensive demographic and tracking profiles analyzed across the active database base.
*   **Multi-Dimensional Attributes:** Deep feature tracking mapping ages, gender distribution, marital status, income brackets, and transaction behaviors.
*   **Operational Intent:** Transitioning raw database records into clear customer segments to optimize marketing campaigns and drive data-backed retention plays.

---

## 2. Project Directory Structure

The repository files are organized according to clean production standards:

```text
customer-demographics-behavior-analytics/
│
├── data/
│   ├── Customer_Master_Data.csv       # Primary customer demographic profiles
│   ├── Customer_Master_Data.csv      # Master spreadsheet reference matrix
│   └── Customer_Transactions.csv      # Complete customer transactional logs
│   └── Customer_Master_Data.xlsx
|
├── customer_behavior_analytics.ipynb   # Exploratory Python analytics notebook
└── customer_behavior_executive_report.pdf # Ready-to-read executive data report

```

---

## 3. Data Cleaning & Engineering Ingestion Pipeline

To ensure all analytical calculations and downstream models are backed by clean, unpolluted data vectors, the notebook runs a rigorous data cleansing pipeline using **Pandas and NumPy**:

*   **Data Typing Standardization:** Programmatically formats dates (`JoinDate`) into standardized datetime objects to track cohort enrollment timelines.
*   **Null and Missing Value Management:** Defensively screens dataset arrays to locate missing values or null vectors, applying mathematical fill rules or isolating incomplete customer profiles.
*   **String Uniformity Mapping:** Standardizes categorical text columns (such as gender markers, marital statuses, and city strings) by stripping trailing whitespaces and fixing casing errors to protect grouping calculations.

---

## 4. Programmatic RFM Segmentation Architecture

To group our customer profiles into clear behavioral tiers, the analytics pipeline runs an RFM (Recency, Frequency, Monetary) scoring matrix. The system scores metrics from 1 to 5, groups them into text patterns, and maps them to target business brackets using conditional regular expressions:

<div align="center">
  <img src="https://private-user-images.githubusercontent.com/50950725/659422249-9a732053-964c-4384-988d-86061d3c0da0.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTA0MjQ1MDQsIm5iZiI6MTc5MDQyNDIwNCwicGF0aCI6Ii81MDk1MDcyNS82NTk0MjIyNDktOWE3MzIwNTMtOTY0Yy00Mzg0LTk4OGQtODYwNjFkM2MwZGEwLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTI2VDEyMDMyNFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTFlMDhmYzIwMjZmOWY2OWZlNWUzODk5ZmE5NTY0MDA3ODg5MGMzYzQ2YTA2ODIwMzRhODY5NmRkYWM2NGQ3MDYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.ZX2Mttvf8CDE3JEezInfCWCliTBaS2EqfnABqYs-uRI" width="100%" alt="Step 5: Quantile RFM Scoring Matrix" style="margin-bottom: 15px;" />
  <br>
  <img src="https://private-user-images.githubusercontent.com/50950725/659422246-6d79ce49-1220-4fb4-9353-b3b754923b5b.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTA0MjQ1MDQsIm5iZiI6MTc5MDQyNDIwNCwicGF0aCI6Ii81MDk1MDcyNS82NTk0MjIyNDYtNmQ3OWNlNDktMTIyMC00ZmI0LTkzNTMtYjNiNzU0OTIzYjViLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTI2VDEyMDMyNFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTY2YThmZjEzMjI1NTEwNDAyNWUxODU0YzczMzZkY2Y4ODUyNGJiMjRhYTI1ZTFiZjg3MGQ0NmVmN2E4ZjQxZjUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.ohbYvmEq-DZ6i9N_Iznt-4dfv8UNUlob1_Oaqcv3PLU" width="49%" alt="Step 6: Segment Concatenation Framework" style="margin: 5px;" />
  <img src="https://private-user-images.githubusercontent.com/50950725/659422248-0517c887-f936-4320-91ee-4052a0e428b5.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTA0MjQ1MDQsIm5iZiI6MTc5MDQyNDIwNCwicGF0aCI6Ii81MDk1MDcyNS82NTk0MjIyNDgtMDUxN2M4ODctZjkzNi00MzIwLTkxZWUtNDA1MmEwZTQyOGI1LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTI2VDEyMDMyNFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWYyYmRhOTYzNzNiZDRiODRlY2JiYWJlMzk4NDkxZTg1ODRjOTMxNzk4NjZhYjA3M2MxY2VlOWRiYWY4NzQzNDAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.Xz-jlUtJV_ZDkDAyoSatWZ8xiUS4J3sxMK8orqo_yBM" width="49%" alt="Step 7: Regex Label Mapping Engine" style="margin: 5px;" />
</div>

---

## 5. Core Business Insights & Visual Metrics Ledger

### Customer Volume vs. Gross Financial Impact
Our segment mapping reveals a classic business trend where a small core group of high-value profiles generates the overwhelming majority of network cash flows:

<div align="center">
  <img src="https://private-user-images.githubusercontent.com/50950725/659422247-94ab85d8-4767-4056-be77-0148a562b878.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTA0MjUxMzIsIm5iZiI6MTc5MDQyNDgzMiwicGF0aCI6Ii81MDk1MDcyNS82NTk0MjIyNDctOTRhYjg1ZDgtNDc2Ny00MDU2LWJlNzctMDE0OGE1NjJiODc4LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTI2VDEyMTM1MlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTNmYzg2YWVlNDRlZjgyZGY2YzRjZDg3OTU0ZGRlZjQ5MDY1NWVkOTNlZjA2ODRhYTMzYmM1Yjc1NTA1NTBlMzAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.TJtG8TWFOKSdGXtUrgajDhWXXvZDCeIvi-ZClVBoW5g" width="100%" alt="Customer Demographics vs Revenue Contribution" style="margin-bottom: 15px;" />
</div>

*   **The Pareto Principal Proven:** Our analysis confirms that roughly **73% of our total customer base generates 76% of all gross network revenue**. 
*   **The High-Exposure Target:** While "Visitors" represent our largest segment volume at **28.9%**, they contribute a smaller relative share of revenue (**23.5%**). Conversely, "Champions" and "Loyal Customers" represent a combined tier that anchors our core financial stability.

### Recency vs. Monetary Distribution
The distribution plot maps out customer spending values against their recent connection timelines to isolate retention patterns:

<div align="center">
  <img src="https://private-user-images.githubusercontent.com/50950725/659422251-55dcaaef-6a50-47ad-ae89-6ee646010fd7.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3OTA0MjUxMzIsIm5iZiI6MTc5MDQyNDgzMiwicGF0aCI6Ii81MDk1MDcyNS82NTk0MjIyNTEtNTVkY2FhZWYtNmE1MC00N2FkLWFlODktNmVlNjQ2MDEwZmQ3LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTI2VDEyMTM1MlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWRlZTI2ZTQwMzBjNWIwMmEyZTk2YTkxZDk4NjVlODIwZGExYTUwOTEwOWNmZjVhYWFmNGVmYmRkN2JjMWQyODAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.WORqv8IRKKwUY1s5GKIRpEe1v_36v68Shl4tVZEqfwk" width="100%" alt="Recency vs Monetary Segmentation Matrix" style="margin-top: 15px;" />
</div>

> **Production Optimization Note:** *The underlying model currently processes time gaps in nanosecond tracking dimensions due to raw timedelta datetime states. A post-launch optimization update is scheduled to extract explicit `.dt.days` integer properties to normalize the X-axis tracking metrics.*

---

## 6. Strategic Business Recovery Plan

Based on our segment findings, we established direct, actionable marketing playbooks to maximize customer lifetime value:

1.  **First-Time Consumer Campaign:** Launch entry-tier offers targeted directly at the high-volume **Visitor** bracket to increase transaction frequencies and build brand trust.
2.  **VIP Retention Campaigns:** Provide exclusive priority service upgrades and early sales access to **Champions** and **Loyal Customers** to protect our core revenue anchors from competitor poaching.
3.  **Accounts Re-Activation Channels:** Deploy automated email surveys and low-overhead value bundles to **Hibernating** accounts to revive inactive profiles without increasing customer service operating costs.

---

## 7. Deployment Architecture

*   **Data Aggregation Core:** Engineered entirely within a Jupyter Notebook pipeline using Python.
*   **Data Manipulation Toolkits:** Managed using Pandas dataframes and NumPy array select structures.
*   **Visual Presentation Graphics:** Rendered using Matplotlib and Seaborn plotting engines.
