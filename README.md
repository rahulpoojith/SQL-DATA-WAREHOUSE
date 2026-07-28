# 🚀 SQL Data Warehouse Project

A comprehensive **SQL Server Data Warehouse** project built using the **Medallion Architecture (Bronze → Silver → Gold)**. This project demonstrates how raw CRM and ERP data can be transformed into a clean, integrated, and analytics-ready data warehouse using industry-standard ETL practices.

The Gold layer is designed using a **Snowflake Schema**, providing a normalized dimensional model that improves data consistency, reduces redundancy, and supports scalable business analytics.

---

## 📌 Project Overview

Organizations often receive data from multiple operational systems in different formats, making reporting and analytics challenging. This project addresses that problem by building a centralized Data Warehouse that integrates CRM and ERP data into a single source of truth.

The project includes:

- Raw data ingestion from multiple source systems
- Data cleansing and transformation
- Business rule implementation
- Data quality validation
- Snowflake schema dimensional modeling
- Automated ETL using SQL Server Stored Procedures
- Analytics-ready datasets for Business Intelligence tools

---

# 🏗️ Data Warehouse Architecture

```
                   Source Systems
          ┌──────────────────────────┐
          │        CRM System        │
          │        ERP System        │
          └─────────────┬────────────┘
                        │
                        ▼
                ┌─────────────────┐
                │ Bronze Layer    │
                │ Raw Data        │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Silver Layer    │
                │ Clean &         │
                │ Transform Data  │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ Gold Layer      │
                │ Snowflake       │
                │ Schema          │
                └────────┬────────┘
                         │
                         ▼
              Business Intelligence
          Power BI • Tableau • Excel
```

---

# 📂 Project Structure

```
SQL-DATA-WAREHOUSE
│
├── datasets/
│   ├── source_crm/
│   └── source_erp/
│
├── scripts/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── docs/
│
├── images/
│
└── README.md
```

---

# 🥉 Bronze Layer

The Bronze Layer serves as the raw landing zone where data is loaded exactly as received from the source systems.

### Data Sources

### CRM

- Customer Information
- Product Information
- Sales Details

### ERP

- Customer Data
- Product Categories
- Location Data

### Operations Performed

- Bulk loading CSV files
- Preserve original data
- No transformations
- Source-level storage
- Foundation for downstream processing

---

# 🥈 Silver Layer

The Silver Layer focuses on improving data quality by cleaning, validating, and standardizing the raw data.

### Data Quality Transformations

- Remove duplicate records
- Handle NULL values
- Trim leading and trailing spaces
- Standardize text values
- Convert business codes into meaningful values
- Validate dates
- Remove invalid records
- Apply business rules
- Standardize naming conventions

This layer produces reliable and consistent datasets for analytical modeling.

---

# 🥇 Gold Layer

The Gold Layer contains analytics-ready business models organized using a **Snowflake Schema**.

Unlike a traditional Star Schema, the Snowflake Schema normalizes dimension tables into multiple related tables, improving data consistency while minimizing redundancy.

The Gold Layer is designed for:

- Business Intelligence
- Reporting
- Dashboard Development
- KPI Analysis
- Decision Support
- Ad-hoc Analytics

---

# ❄️ Snowflake Schema

```
                  Dim Category
                       │
                       │
                Dim Product
                       │
                       │
             ┌─────────┴─────────┐
             │                   │
        Fact Sales         Dim Customer
                                   │
                                   │
                            Dim Geography
```

The normalized design helps maintain data integrity and supports scalable analytical workloads.

---

# 🔄 ETL Workflow

```
CSV Files
     │
     ▼
Bronze Layer
(Raw Data)
     │
     ▼
Silver Layer
(Data Cleaning &
Transformation)
     │
     ▼
Gold Layer
(Snowflake Schema)
     │
     ▼
Business Analytics
```

---

# ⚙️ Technologies Used

| Category | Technologies |
|----------|--------------|
| Database | Microsoft SQL Server |
| Language | T-SQL |
| ETL | SQL Stored Procedures |
| Data Loading | BULK INSERT |
| Data Modeling | Snowflake Schema |
| Query Objects | Views |
| Development Tool | SQL Server Management Studio (SSMS) |
| Version Control | Git & GitHub |

---

# ✨ Features

- Medallion Architecture (Bronze → Silver → Gold)
- Automated ETL Pipeline
- Bulk Data Loading
- SQL Stored Procedures
- Data Cleaning & Validation
- Data Standardization
- Snowflake Schema Modeling
- Business Rule Implementation
- Analytics-ready Data Warehouse
- Modular SQL Scripts
- Scalable Warehouse Design

---

# 📈 Business Benefits

This project enables organizations to:

- Build a centralized source of truth
- Improve data quality
- Eliminate duplicate and inconsistent records
- Accelerate reporting
- Support Business Intelligence initiatives
- Enable scalable analytics
- Improve business decision-making

---

# 🚀 Getting Started

## Prerequisites

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- Git

---

## Clone the Repository

```bash
git clone https://github.com/rahulpoojith/SQL-DATA-WAREHOUSE.git
```

---

## Create the Database

Execute the database creation scripts.

---

## Load Bronze Layer

Run the Bronze ETL procedure.

```sql
EXEC bronze.load_bronze;
```

---

## Load Silver Layer

Run the Silver ETL procedure.

```sql
EXEC silver.load_silver;
```

---

## Build the Gold Layer

Execute the Gold layer scripts to create the Snowflake Schema and analytical views.

---

# 📊 ETL Flow

```
Raw CSV Files
      │
      ▼
Bronze Layer
      │
      ▼
Data Cleaning
      │
      ▼
Silver Layer
      │
      ▼
Business Rules
      │
      ▼
Gold Layer
      │
      ▼
Snowflake Schema
      │
      ▼
Reporting & Analytics
```

---

# 🎯 Skills Demonstrated

- SQL Server Development
- T-SQL Programming
- ETL Pipeline Development
- Data Warehousing
- Data Cleaning
- Data Transformation
- Data Validation
- Snowflake Schema Design
- Stored Procedure Development
- Bulk Data Loading
- Dimensional Modeling
- Query Optimization
- Business Intelligence Fundamentals

---

# 📚 Learning Outcomes

Through this project, I gained practical experience in:

- Designing enterprise Data Warehouses
- Building Medallion Architecture
- Developing ETL pipelines
- Writing reusable Stored Procedures
- Cleaning and transforming large datasets
- Implementing Snowflake Schema models
- Applying dimensional modeling concepts
- Preparing analytics-ready datasets

---

# 🔮 Future Enhancements

- Incremental Data Loading
- Change Data Capture (CDC)
- Slowly Changing Dimensions (SCD Type 2)
- SQL Server Agent Job Automation
- Performance Tuning
- Power BI Dashboard Integration
- Data Quality Monitoring
- ETL Logging and Error Handling

---

# 👨‍💻 Author

**Rahul Poojith**

Data Analyst | SQL Developer | Aspiring Data Engineer

**GitHub:** https://github.com/rahulpoojith

> Feel free to connect, provide feedback, or contribute to the project.

---

# ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates future improvements.

---

## 📄 License

This project is intended for educational and portfolio purposes. Feel free to fork, learn from, and build upon it with appropriate attribution.
