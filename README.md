# 🔄 ETL Pipeline – Customer Churn Data Engineering

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
