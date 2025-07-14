# Databricks mini project

This repository contains an end-to-end mini project built using **Databricks**, covering data ingestion, transformation, scheduling, ETL pipelines, dashboarding, and Power BI reporting. It serves as both a **placeholder for notebooks** and **documentation** of the workflow.

---

## 🔍 Project Overview

This project demonstrates a full data engineering lifecycle on Databricks using two different source systems: **CRM** and **ERP**. It includes:

- Data ingestion from CSV source files
- Building Bronze, Silver, and Gold Delta tables
- Creating Jobs for scheduled and manual runs
- Implementing Delta Live Tables (DLT) ETL pipelines
- Visualising results via Databricks SQL Dashboard
- Connecting Gold tables to **Power BI** for reporting

---

## 📁 Source Systems

- **CRM**: Customer, product, and sales details
- **ERP**: Customer demographics, product categories, and location info

---

## 🛠️ Layers Implemented

### 🔹 Bronze Layer
- Raw ingestion from CSVs using DLT
- Schema inferred, minimal transformation
- Stored as Delta tables

### ⚪ Silver Layer
- Cleaned and enriched data from Bronze
- CRM and ERP processed in separate notebooks

### 🟡 Gold Layer
- Final dimension and fact tables ready for reporting
  - `dim_customers`
  - `dim_products`
  - `fact_sales`

---

## ⚙️ Jobs & Scheduling

- **Chained Job** created to orchestrate:
  1. Bronze DLT pipeline
  2. Silver DLT pipeline
  3. Gold DLT pipeline
- Supports **manual and scheduled runs**
- Includes job **success/failure notifications**

---

## 🧱 ETL Pipelines (DLT)

- Built using **Delta Live Tables**
- Modular design with clear lineage
- Each layer defined in its own notebook

---

## 📊 Dashboarding

### Databricks SQL Dashboard
- Queries executed on Gold tables
- Interactive charts and tables
- E.g. customer count by country, product sales by category

### Power BI Integration
- **DirectQuery** connection to Databricks SQL warehouse
- Gold tables used as the data source
- Enables advanced visualisations and self-service analytics

---

## 📂 Repository Contents

| Folder/File              | Description                          |
|--------------------------|--------------------------------------|
| `bronze/`                | Bronze layer DLT notebooks           |
| `silver/`                | Silver layer DLT notebooks           |
| `gold/`                  | Gold layer DLT notebooks             |
| `jobs/`                  | Notes on Job configuration           |
| `README.md`              | Project overview (this file)         |

---

## 💡 Notes

- All notebooks are version-controlled in this repository.
- The project showcases a clean data pipeline workflow from raw data to business-ready dashboards.
- Power BI adds additional value for external reporting and stakeholder use.

---
