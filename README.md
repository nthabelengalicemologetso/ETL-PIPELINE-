# 🔄 ETL Pipeline – Customer Churn Data Engineering


<img width="1650" height="698" alt="Screenshot 2026-09-23 230247" src="https://github.com/user-attachments/assets/80fd9688-2e3d-4932-9b30-ef11f516ad3c" />
<img width="1358" height="575" alt="Screenshot 2026-09-23 225858" src="https://github.com/user-attachments/assets/3f0be851-e8ea-47c8-a743-42fa12785635" />



## 📌 Overview

This project demonstrates an automated **ETL (Extract, Transform, Load) pipeline** built using **Databricks Free Edition**.

The pipeline prepares customer churn data for downstream **data analysis and machine learning**. It takes raw data from the `churn_modelling` Delta table, performs data cleaning and transformation, and publishes the processed datasets as **materialized views** that can be used for analytics and modelling.

The project focuses on applying practical data engineering concepts such as:

- Data extraction
- Data transformation
- Data cleaning
- Data quality preparation
- Delta tables
- Materialized views
- Automated pipeline orchestration
- Databricks workflows

---

## 🏗️ ETL Pipeline Architecture

```text
             ┌─────────────────────┐
             │   Raw Churn Data    │
             │  churn_modelling    │
             │    Delta Table      │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │       EXTRACT       │
             │                     │
             │ Read raw data from  │
             │ Delta table         │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │     TRANSFORM       │
             │                     │
             │ • Clean data        │
             │ • Handle data types │
             │ • Transform fields  │
             │ • Prepare features  │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │        LOAD         │
             │                     │
             │ Materialized views  │
             │ for analytics & ML  │
             └──────────┬──────────┘
                        │
                        ▼
             ┌─────────────────────┐
             │ Analytics /         │
             │ Machine Learning    │
             └─────────────────────┘
