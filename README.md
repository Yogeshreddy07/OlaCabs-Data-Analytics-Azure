# README.md

## Ola Cabs Data Pipeline with Azure

### 🚀 Project Overview

This project addresses a critical business need by building a comprehensive data pipeline on Azure to analyze Ola Cabs ride data. The goal is to ingest ride and trip data from GitHub, transform it in the cloud, and generate actionable insights through a Power BI dashboard. The dashboard will highlight key performance indicators (KPIs) related to ride demand, fare patterns, and location-based trends, allowing stakeholders to filter and analyze data by date, location, and ride type.

### 📊 Business Requirements
The business wants to better understand ride demand and pricing behavior to improve service allocation and pricing strategies. The key requirements include:

- **Ride Demand & Revenue Analysis:** A dashboard showing total rides, revenue, and peak demand hours.
- **Location-Based Insights:** Ability to filter data by pickup/drop-off location and time.
- **User-Friendly Interface:** Stakeholders should have an intuitive interface for querying data.

### 🛠️ Solution Overview

#### Data Ingestion:
- Extract ride data from GitHub.
- Load the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

#### Data Transformation:
- Use Azure Databricks to clean, transform, and aggregate the data.
- Organize the data into Bronze, Silver, and Gold layers for raw, cleansed, and aggregated data.

#### Data Loading and Reporting:
- Load the transformed data into Databricks SQL Warehouse.
- Build a Power BI dashboard to visualize the data, enabling stakeholders to explore ride and pricing trends.

#### Automation:
- Schedule the pipeline to run daily to keep data and reports up-to-date.

### 🏗️ Technology Stack
- **Azure Data Factory (ADF):** For orchestrating data movement.
- **Azure Data Lake Storage (ADLS):** For storing raw and processed data.
- **Azure Databricks:** For data transformation and processing.
- **Databricks SQL Warehouse:** For warehousing and SQL-based analysis.
- **Power BI:** For data visualization.
- **Azure Key Vault:** For securely managing credentials.

### 🛠️ Setup Instructions

#### Prerequisites
- An Azure account with sufficient credits.
- Access to the Ola Cabs dataset on GitHub.

#### Step 1: Azure Environment Setup
1. **Create a Resource Group:** Set up a new resource group in Azure.
2. **Provision Services:**
   - Azure Data Factory instance.
   - Azure Data Lake Storage with bronze, silver, and gold containers.
   - Azure Databricks workspace and SQL Warehouse.
   - Azure Key Vault for secret management.

#### Step 2: Data Ingestion
1. **Clone the Dataset:** Clone the Ola Cabs dataset from GitHub.
2. **Ingest Data with ADF:** Create ADF pipelines to copy data from GitHub to the bronze layer in ADLS.

#### Step 3: Data Transformation
1. **Mount ADLS in Databricks:** Connect Databricks to access the data lake.
2. **Transform Data:** Use Spark to clean, transform, and aggregate data into silver and gold layers.

#### Step 4: Data Loading and Reporting
1. **Load Data into SQL Warehouse:** Load the gold-layer data into Databricks SQL Warehouse.
2. **Create Power BI Dashboard:** Connect Power BI to the warehouse and build visualizations.

#### Step 5: Automation and Monitoring
1. **Schedule Pipelines:** Use ADF to schedule the entire data pipeline.
2. **Monitor Runs:** Monitor pipeline executions using ADF and Databricks logs.

#### Step 6: Security and Governance
1. **Manage Access:** Set up role-based access control (RBAC) using Azure Entra ID.
2. **Secure Secrets:** Use Azure Key Vault to store connection strings and secrets.

#### Step 7: End-to-End Testing
1. **Trigger the Pipeline:** Add new records to the dataset and trigger the pipeline.
2. **Validate the Dashboard:** Ensure new records reflect correctly in the Power BI dashboard.

### 📘 Conclusion

This project provides a complete end-to-end solution for analyzing Ola Cabs ride data, helping the business optimize services through real-time, data-driven insights. The automated pipeline ensures that stakeholders always have access to the latest metrics, improving strategic decision-making.


