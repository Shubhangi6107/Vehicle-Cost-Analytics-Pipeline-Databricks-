# 🚗 Vehicle Cost Analytics Pipeline using Databricks (Medallion Architecture)

An end-to-end Vehicle Cost Analytics solution built on **Databricks** using the **Medallion Architecture (Bronze → Validation → Silver → Gold)**. This project demonstrates how raw vehicle, fuel, and usage data can be transformed into business-ready insights through an automated ETL pipeline, KPI generation, interactive dashboards, and workflow orchestration.

---

### Dashboard Preview

![Vehicle Dashboard](images/Dashboard_Preview.png)


# 📌 Project Objective

Organizations often receive vehicle-related data from multiple sources, making it difficult to generate accurate business insights due to inconsistent formatting, missing values, and invalid records.

The objective of this project is to:

- Build a scalable ETL pipeline using Databricks
- Implement Medallion Architecture for data processing
- Validate and clean raw data before transformation
- Generate business-ready KPI tables
- Build an interactive dashboard for decision-making
- Automate the entire pipeline using Databricks Workflows

---

# ⭐ Why This Project Stands Out

Unlike a traditional dashboard project, this solution demonstrates a complete enterprise-grade data engineering workflow.

### Key Highlights

✔ End-to-End ETL Pipeline

✔ Medallion Architecture Implementation

✔ Data Validation Layer

✔ Automated Data Quality Checks

✔ Business KPI Generation

✔ Interactive Dashboard

✔ Databricks Workflow Automation

✔ SQL-based Transformations

✔ Production-style Pipeline Design

---

# 🏗 Project Architecture

```
                    Raw CSV Files
                          │
                          ▼
                  Bronze Layer
             (Raw Data Ingestion)
                          │
                          ▼
              Data Validation Layer
       (Quality Checks & Error Detection)
                          │
                          ▼
                  Silver Layer
      (Cleaning & Standardization)
                          │
                          ▼
                   Gold Layer
        (Business Metrics & KPIs)
                          │
                          ▼
              Interactive Dashboard
                          │
                          ▼
           Databricks Workflow Automation
```

---

# 📂 Project Structure

```
Vehicle-Cost-Analytics/
│
├── datasets/
│      vehicle_master.csv
│      fuel_prices.csv
│      vehicle_usage.csv
│
├── notebooks/
│      01_Bronze_Load
│      02_Data_Validation
│      03_Silver_Transformation
│      04_Gold_KPI_Creation
│
├── dashboard/
│      Vehicle Cost Analytics Dashboard
│
├── workflow/
│      Databricks Workflow

```

---

# ⚙ Technologies Used

- Databricks
- SQL
- Unity Catalog
- Databricks SQL Dashboard
- Databricks Workflows
- Medallion Architecture

---

# 📊 Dataset Description

The project uses three datasets:

### 1. Vehicle Master

Contains:

- Vehicle ID
- Vehicle Name
- Region
- Fuel Type
- Mileage

---

### 2. Fuel Prices

Contains:

- Region
- Year
- Fuel Price per Liter

---

### 3. Vehicle Usage

Contains:

- Vehicle ID
- Year
- KM Driven

---

# 🔄 ETL Pipeline

## Bronze Layer

Purpose:

- Load raw CSV files
- Preserve original data
- Create Bronze tables

Output:

- vehicle_master_bronze
- fuel_prices_bronze
- vehicle_usage_bronze

---

## Data Validation Layer

Purpose:

Perform quality checks before transformation.

Validation includes:

- Null value checks
- Duplicate detection
- Invalid mileage detection
- Invalid fuel price detection
- Failed record identification

Output:

- validation_report
- validation_failed_records

---

## Silver Layer

Purpose:

Clean and standardize validated data.

Transformations performed:

- Remove unwanted spaces
- Standardize text formatting
- Handle missing values
- Create consistent schema
- Improve data quality

Output:

- vehicle_master_silver
- fuel_prices_silver
- vehicle_usage_silver

---

## Gold Layer

Purpose:

Generate business-ready datasets.

Business calculations:

- Fuel Consumed
- Total Fuel Cost
- Cost Per KM
- Aggregated Business KPIs

Output:

- vehicle_cost_gold
- kpi_dashboard_summary

---

# 📈 Dashboard

The dashboard provides key business insights including:

### KPI Cards

- Total Vehicles
- Total Fuel Cost
- Total KM Driven
- Average Cost per KM

---

### Visualizations

- Fuel Cost Trend by Year
- Region-wise Fuel Cost Comparison
- Top Vehicles by Fuel Cost
- Detailed Vehicle Analytics Table

---

# ⚡ Workflow Automation

The complete pipeline is automated using **Databricks Workflows**.

Execution Order:

```
Bronze_Load
      │
      ▼
Data_Validation
      │
      ▼
Silver_Transformation
      │
      ▼
Gold_KPI_Creation
```

### Benefits

- Eliminates manual execution
- Ensures correct notebook execution order
- Improves reliability
- Reduces human errors
- Enables scheduled execution
- Keeps dashboards updated with latest processed data

---

# 📌 Business KPIs Generated

- Total Vehicles
- Total Fuel Cost
- Average Cost Per KM
- Total KM Driven
- Region-wise Cost
- Vehicle-wise Cost
- Yearly Fuel Cost Trend

---

# 🚀 Business Value

This solution helps organizations to:

- Monitor vehicle operating costs
- Identify high-cost vehicles
- Compare fuel expenses across regions
- Track yearly cost trends
- Improve operational decision-making
- Reduce manual reporting effort

---

# 📈 Key Features

- End-to-End ETL Pipeline
- Medallion Architecture
- Automated Data Validation
- SQL Transformations
- KPI Generation
- Interactive Dashboard
- Workflow Automation
- Modular Notebook Design
- Enterprise-style Project Structure

---

# 🔮 Future Enhancements

- Incremental Data Loading
- Delta Live Tables
- Predictive Cost Forecasting
- Alerting for Data Quality Issues
- CI/CD Integration
- Email Notifications on Workflow Completion
- Row-Level Security
- Real-time Data Streaming

---

# 📚 Learning Outcomes

Through this project, I gained hands-on experience in:

- Databricks
- Medallion Architecture
- ETL Pipeline Design
- SQL Transformations
- Data Validation
- Dashboard Development
- Workflow Automation
- Enterprise Data Engineering Best Practices

---
