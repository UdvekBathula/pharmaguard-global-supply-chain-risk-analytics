# 📂 Data Directory

This directory contains all datasets used in the **PharmaGuard: Global Supply Chain Risk Analytics** project.

The datasets are organized according to different stages of the data pipeline, from raw synthetic data generation to cleaned and normalized datasets used for analysis and visualization.

---

## 📁 Directory Structure

```text
data/
├── raw/
│   ├── Countries.csv
│   ├── Drugs.csv
│   ├── Manufacturer.csv
│   ├── Shipments.csv
│   └── Transit_Nodes.csv
│
│
└── processed/
    └── Shipments_Modified.csv
```

---

# 📦 Raw Data (`raw/`)

The `raw` folder contains the original synthetic datasets generated for the project. These files are preserved in their original form and serve as the source of truth for all preprocessing and analysis.

| Dataset               | Description                                                                                                                   | Primary Use                                                                     |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Countries.csv**     | Country-level reference data containing geographic, economic, and regulatory information.                                     | Geographic analysis, country mapping, and risk assessment.                      |
| **Drugs.csv**         | Master dataset containing pharmaceutical products, therapeutic classes, storage requirements, and standard market prices.     | Drug dimension table for joins, pricing analysis, and therapeutic segmentation. |
| **Manufacturer.csv**  | Information about pharmaceutical manufacturers including company type, establishment year, GMP certification, and risk score. | Manufacturer-level analysis and supply chain evaluation.                        |
| **Shipments.csv**     | Original shipment transaction dataset generated for the project before normalization.                                         | Source dataset for ETL, preprocessing, and feature engineering.                 |
| **Transit_Nodes.csv** | Information about ports, airports, and logistics hubs through which pharmaceutical shipments travel.                          | Supply chain route analysis and transit vulnerability assessment.               |

---

# 🧹 Processed Data (`processed/`)

The `processed` folder contains cleaned and transformed datasets created after preprocessing.

## Shipments_Modified.csv

`Shipments_Modified.csv` is the normalized version of the original shipment dataset.

The dataset has been redesigned following dimensional modeling principles by replacing redundant descriptive fields with foreign keys that reference dedicated dimension tables.

### Key Improvements

* Replaced `drug_name` with `drug_id`
* Replaced `manufacturer_name` with `manufacturer_id`
* Replaced `destination_country` with `destination_country_code`
* Removed duplicate attributes already available in dimension tables
* Reduced redundancy and improved data consistency
* Optimized for SQL joins and Power BI relationships

### Current Schema

| Column                   | Description                                  |
| ------------------------ | -------------------------------------------- |
| batch_id                 | Unique shipment identifier                   |
| shipment_date            | Shipment dispatch date                       |
| drug_id                  | Foreign key referencing `Drugs.csv`          |
| manufacturer_id          | Foreign key referencing `Manufacturer.csv`   |
| destination_country_code | Foreign key referencing `Countries.csv`      |
| quantity                 | Number of units shipped                      |
| selling_price            | Actual selling price per unit                |
| total_value              | Total shipment value                         |
| expected_transit_days    | Planned transit duration                     |
| actual_transit_days      | Actual transit duration                      |
| delay_days               | Transit delay in days                        |
| temperature_recorded     | Recorded shipment temperature                |
| temperature_deviation    | Difference from required storage temperature |
| cold_chain_failure       | Indicates cold-chain violation               |
| reporting_source         | Source of incident reporting                 |
| lab_result               | Authentic / Substandard / Counterfeit        |
| risk_level               | Assigned shipment risk level                 |
| inspection_required      | Indicates whether inspection is required     |
| created_timestamp        | Record creation timestamp                    |

---

# 🔗 Dataset Relationships

The project follows a **star schema** architecture.

```text
                 Countries
             ┌──────────────┐
             │ country_code │
             └──────▲───────┘
                    │
                    │
      ┌─────────────┴─────────────┐
      │                           │
      ▼                           ▼
Manufacturers              Shipments_Modified
┌──────────────┐          ┌────────────────────┐
│manufacturer_id│────────▶│manufacturer_id     │
│country_code   │         │drug_id             │
└──────────────┘          │destination_country │
                          └─────────▲──────────┘
                                    │
                                    │
                                    ▼
                               Drugs
                         ┌────────────────┐
                         │ drug_id        │
                         │ drug_name      │
                         │ category       │
                         └────────────────┘
```

This design minimizes redundancy while maintaining referential integrity across datasets.

---

# 🔄 Data Processing Workflow

```text
Synthetic Data Generation
            │
            ▼
     Raw CSV Files
            │
            ▼
    Data Cleaning & Validation
            │
            ▼
   Normalization & Feature Engineering
            │
            ▼
   Shipments_Modified.csv
            │
            ▼
 SQL Analysis • Python EDA • Power BI
```

---

# 🎯 Use Cases

The datasets in this directory support a variety of analytical tasks, including:

* Counterfeit drug detection and trend analysis
* Cold-chain logistics monitoring
* Transit delay and supply chain performance evaluation
* Geographic risk mapping
* Price anomaly and market deviation analysis
* Manufacturer risk assessment
* SQL-based business intelligence queries
* Interactive Power BI dashboards
* Exploratory Data Analysis (EDA)
* Machine learning feature engineering and predictive modeling

---

# ⚠️ Disclaimer

All datasets included in this project are **synthetically generated for educational and portfolio purposes**. They do not represent real pharmaceutical shipments, manufacturers, or regulatory records and should not be used for operational or clinical decision-making.
