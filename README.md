# 🚀 SQL Data Warehouse Project

A modern **Data Warehouse and Analytics** solution built using **SQL Server**, following the Medallion Architecture (**Bronze → Silver → Gold**) to transform raw CRM and ERP data into analytics-ready business models.

This project demonstrates industry-standard **ETL development, data modeling, data cleansing, and analytical reporting** using SQL Server.

---

## 📖 Project Overview

The objective of this project is to build a scalable and maintainable Data Warehouse capable of integrating data from multiple operational systems and transforming it into meaningful business insights.

The project covers:

- Data Ingestion
- Data Cleaning & Standardization
- Data Transformation
- Data Modeling
- ETL Automation using Stored Procedures
- Analytics-ready Star Schema

---

## 🏗️ Data Warehouse Architecture

```
                Source Systems
          ┌─────────────────────┐
          │     CRM System      │
          │     ERP System      │
          └─────────┬───────────┘
                    │
                    ▼
          ┌─────────────────────┐
          │   Bronze Layer      │
          │ Raw Data Ingestion  │
          └─────────┬───────────┘
                    │
                    ▼
          ┌─────────────────────┐
          │   Silver Layer      │
          │ Data Cleaning &     │
          │ Business Rules      │
          └─────────┬───────────┘
                    │
                    ▼
          ┌─────────────────────┐
          │    Gold Layer       │
          │ Star Schema &       │
          │ Analytics Views     │
          └─────────────────────┘
```

---

# 🥉 Bronze Layer

The Bronze Layer stores raw data exactly as received from the source systems.

### Source Systems

### CRM
- Customer Information
- Product Information
- Sales Details

### ERP
- Customer Data
- Location Data
- Product Category Data

### Tasks Performed

- Bulk Load CSV Files
- Preserve Raw Data
- No Transformations
- Maintain Source Integrity

---

# 🥈 Silver Layer

The Silver Layer performs data cleansing and standardization.

### Data Quality Operations

- Remove Duplicate Records
- Handle NULL Values
- Trim Whitespaces
- Standardize Date Formats
- Standardize Gender Values
- Convert Marital Status Codes
- Remove Invalid Records
- Apply Business Rules

This layer prepares clean and reliable data for analytical processing.

---

# 🥇 Gold Layer

The Gold Layer contains business-ready analytical tables designed using a **Star Schema**.

### Fact Table

- Fact Sales

### Dimension Tables

- Dimension Customers
- Dimension Products

The Gold Layer is optimized for:

- Reporting
- Dashboards
- Business Intelligence
- Analytics
- KPI Calculations

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

# ⚙️ ETL Workflow

```
CSV Files
     │
     ▼
Bronze Layer
(Raw Ingestion)
     │
     ▼
Silver Layer
(Cleaning &
Transformation)
     │
     ▼
Gold Layer
(Data Modeling)
     │
     ▼
Analytics &
Reporting
```

---

# 🛠️ Technologies Used

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- T-SQL
- Stored Procedures
- Bulk Insert
- Views
- Star Schema
- ETL Development
- Data Warehousing

---

# 📊 Features

✔ Automated ETL Pipeline

✔ Medallion Architecture

✔ Data Cleaning

✔ Data Validation

✔ Data Standardization

✔ Star Schema Design

✔ Fact & Dimension Modeling

✔ SQL Stored Procedures

✔ Analytics-ready Data Model

---

# 📈 Business Benefits

This Data Warehouse enables:

- Faster Reporting
- Improved Data Quality
- Single Source of Truth
- Better Business Decision Making
- Scalable ETL Process
- Easy Integration with Power BI and Tableau

---

# 📸 Sample Workflow

```
CRM + ERP Data
        │
        ▼
Bronze
        │
        ▼
Silver
        │
        ▼
Gold
        │
        ▼
Power BI
Excel
Tableau
Analytics
```

---

# 🚀 How to Run

### 1 Clone Repository

```bash
git clone https://github.com/rahulpoojith/SQL-DATA-WAREHOUSE.git
```

### 2 Open SQL Server Management Studio

Connect to your SQL Server instance.

### 3 Create Database

Run the database creation script.

### 4 Load Bronze Layer

Execute:

```
bronze.load_bronze
```

### 5 Load Silver Layer

Execute:

```
silver.load_silver
```

### 6 Build Gold Layer

Run the Gold Layer scripts to create dimensions and fact tables.

---

# 📚 Learning Outcomes

Through this project, I gained hands-on experience in:

- Data Warehouse Design
- SQL Server ETL Development
- Data Cleansing Techniques
- Star Schema Modeling
- Stored Procedure Development
- Data Validation
- SQL Performance Optimization
- Business Intelligence Foundations

---

# 👨‍💻 Author

**Rahul Poojith**

Data Analyst | SQL Developer | Aspiring Data Engineer

GitHub: https://github.com/rahulpoojith

LinkedIn: *(Add your LinkedIn profile here)*

---

# ⭐ If you found this project helpful

Give this repository a ⭐ and feel free to fork it!
