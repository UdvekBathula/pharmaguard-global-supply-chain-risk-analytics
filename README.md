# 💊 PharmaGuard: Global Supply Chain Risk Analytics

## 📌 Overview

**PharmaGuard: Global Supply Chain Risk Analytics** is an end-to-end data analytics project that investigates vulnerabilities in the global pharmaceutical supply chain and identifies patterns associated with counterfeit and substandard medicines.

Using a realistic synthetic dataset, the project demonstrates how **SQL, Python, Pandas, NumPy, and Power BI** can be leveraged to analyze complex supply chain operations, detect anomalies, and generate actionable business insights through interactive dashboards.

The project is designed to simulate the responsibilities of a **Forensic Data Analyst**, helping pharmaceutical companies and regulatory organizations identify high-risk routes, vulnerable transit nodes, and counterfeit drug activities.

---

# 🎯 Problem Statement

Counterfeit and substandard medicines represent one of the most critical challenges facing global healthcare systems. These products enter legitimate supply chains through unauthorized distributors, weak regulatory checkpoints, and vulnerable logistics networks, resulting in financial losses and serious public health risks.

The objective of **PharmaGuard** is to analyze pharmaceutical shipment data to uncover hidden supply chain risks and provide data-driven recommendations for improving supply chain security.

---

# 🚀 Project Objectives

* Generate a realistic pharmaceutical supply chain dataset
* Clean and preprocess large-scale shipment data
* Perform Exploratory Data Analysis (EDA)
* Analyze supply chain vulnerabilities using SQL
* Detect counterfeit indicators through pricing and logistics anomalies
* Evaluate cold-chain failures for temperature-sensitive medicines
* Develop a shipment risk scoring framework
* Build an interactive Power BI dashboard for business stakeholders

---

# 🛠️ Tech Stack

| Category                  | Technologies     |
| ------------------------- | ---------------- |
| Programming Language      | Python           |
| Data Manipulation         | Pandas, NumPy    |
| Database                  | SQL              |
| Data Visualization        | Power BI         |
| Version Control           | Git & GitHub     |
| Notebook Environment      | Jupyter Notebook |
| Synthetic Data Generation | Python & AI      |
| Documentation             | Markdown         |

---

# 📂 Project Workflow

```text
Synthetic Data Generation
            │
            ▼
      Raw Dataset Creation
            │
            ▼
 Data Cleaning & Preprocessing
    (Python + Pandas + NumPy)
            │
            ▼
    Feature Engineering
            │
            ▼
      SQL Database Analysis
            │
            ▼
 Exploratory Data Analysis
            │
            ▼
     Shipment Risk Scoring
            │
            ▼
   Interactive Power BI Dashboard
            │
            ▼
 Business Insights & Recommendations
```

---

# 📁 Project Structure

```text
PharmaGuard/

├── data/
│   ├── raw/
│   ├── cleaned/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_generation.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda.ipynb
│   └── 04_sql_analysis.ipynb
│
├── sql/
│   ├── schema.sql
│   ├── analysis_queries.sql
│   └── views.sql
│
├── src/
│   ├── data_generator.py
│   ├── cleaning.py
│   ├── feature_engineering.py
│   └── risk_score.py
│
├── powerbi/
│   └── PharmaGuard.pbix
│
├── docs/
│   ├── problem_statement.md
│   ├── project_scope.md
│   ├── data_dictionary.md
│   ├── methodology.md
│   ├── business_questions.md
│   ├── architecture.md
│   ├── dashboard_guide.md
│   └── insights.md
│
├── README.md
└── requirements.txt
```

---

# 📊 Dataset Description

The project uses a synthetic dataset representing global pharmaceutical shipments across manufacturers, transit hubs, and destination countries.

### Sample Features

* Batch ID
* Drug Name
* Drug Category
* Manufacturer Country
* Destination Country
* Transit Nodes
* Expected Transit Time
* Actual Transit Time
* Market Price
* Selling Price
* Required Temperature
* Recorded Temperature
* Reporting Source
* Lab Test Result
* Shipment Status
* Risk Score

---

# ❓ Business Questions

This project seeks to answer several real-world business questions:

* Which drugs are most frequently counterfeited?
* Which transit ports or airports exhibit the highest counterfeit rates?
* Does shipment delay increase counterfeit probability?
* How do cold-chain failures impact medicine quality?
* Which countries receive the highest number of counterfeit shipments?
* Which reporting channels identify counterfeit products most effectively?
* Are significant price discounts indicators of counterfeit activity?
* Which global supply routes carry the highest operational risk?

---

# 🔍 Exploratory Data Analysis

The EDA phase includes:

* Data quality assessment
* Missing value analysis
* Duplicate detection
* Outlier identification
* Drug distribution analysis
* Country-wise shipment analysis
* Counterfeit pattern analysis
* Transit delay analysis
* Price drift evaluation
* Temperature anomaly detection
* Correlation analysis
* Trend analysis over time

---

# 🗄️ SQL Analysis

Advanced SQL is used to:

* Identify high-risk transit nodes
* Rank countries by counterfeit occurrence
* Analyze shipment delays
* Detect abnormal pricing behavior
* Evaluate cold-chain failures
* Generate analytical views
* Perform route-level aggregation
* Apply window functions for ranking and trend analysis

---

# ⚠️ Risk Scoring Framework

Each shipment is assigned a custom risk score based on:

* Transit delays
* Temperature deviations
* Pricing anomalies
* Transit node vulnerability
* Historical counterfeit frequency

The resulting score helps prioritize shipments that require immediate investigation.

---

# 📈 Power BI Dashboard

The interactive dashboard provides:

## Executive Overview

* Total Shipments
* Counterfeit Percentage
* Substandard Percentage
* Average Transit Delay
* Overall Risk Score

## Global Risk Map

Visualizes international shipment routes with color-coded risk levels.

## Drug Target Analysis

Highlights medicines experiencing the highest counterfeit activity.

## Transit Node Analytics

Ranks ports and airports based on counterfeit occurrence.

## Cold Chain Monitoring

Tracks temperature deviations across shipments.

## Early Warning System

Flags shipments with abnormal delays, pricing anomalies, or temperature violations.

---

# 💡 Expected Business Insights

The analysis aims to uncover:

* High-risk international shipping corridors
* Frequently targeted pharmaceutical products
* Vulnerable logistics hubs
* Pricing patterns associated with counterfeit distribution
* Cold-chain failures affecting medicine quality
* Supply chain inefficiencies requiring corrective action

---

# 🔮 Future Enhancements

Potential future improvements include:

* Machine Learning–based counterfeit prediction
* Real-time shipment monitoring
* Automated anomaly detection
* Geospatial route optimization
* API integration with logistics systems
* Time-series forecasting of emerging risks
* Interactive web application deployment

---

# 📚 Learning Outcomes

This project demonstrates practical experience in:

* End-to-End Data Analytics
* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Advanced SQL
* Feature Engineering
* Business Intelligence
* Risk Analytics
* Dashboard Development
* Data Storytelling
* GitHub Project Management

---

# ⚠️ Disclaimer

This project uses synthetic data generated solely for educational and portfolio purposes. It does not contain any confidential pharmaceutical records or real-world shipment information. Any resemblance to actual organizations or supply chains is purely coincidental.

---

# 👨‍💻 Author

**Udvek Bathula**

**Aspiring Data Analyst | Data Scientist**

Focused on building scalable data solutions and transforming raw data into meaningful business insights.

---

#  Acknowledgements

This project was developed as part of a continuous data analytics and engineering learning journey. It draws inspiration from industry-standard practices in data analytics, supply chain intelligence, business intelligence reporting, and modern data engineering architectures.

The project showcases the practical application of SQL, Python, Pandas, NumPy, and Power BI to solve a realistic business problem through an end-to-end analytical workflow.
