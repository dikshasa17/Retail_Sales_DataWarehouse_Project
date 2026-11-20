# End-to-End CRM & ERP Data Warehouse | SQL Server

## 📌 Project Overview

This project demonstrates the development of an end-to-end **Data Warehouse using SQL Server**, integrating data from CRM (Customer Relationship Management) and ERP (Enterprise Resource Planning) source systems.

The objective is to transform raw transactional and customer data into a structured, analytics-ready data warehouse using the **Medallion Architecture (Bronze, Silver, and Gold layers)**.

The project covers the complete data engineering workflow, including data ingestion, data cleaning, transformation, data integration, dimensional modeling, and data quality validation.

A **Star Schema** was designed in the Gold layer to support business reporting, analytical queries, and downstream visualization.

## 🏗️ Data Architecture

Implemented a three-layer Medallion Architecture to progressively transform raw source data into business-ready datasets.

### 1. Bronze Layer – Raw Data Ingestion

- Loaded raw CRM and ERP CSV datasets into SQL Server.
- Created six structured Bronze tables to maintain source data.
- Implemented bulk data loading using `BULK INSERT`.
- Preserved raw data without applying business transformations.

### 2. Silver Layer – Data Cleaning & Transformation

Performed data standardization, cleansing, and integration across source systems.

Key transformations included:

- Removed duplicate customer records using `ROW_NUMBER()`.
- Standardized customer names, marital status, and gender values.
- Handled missing and invalid values.
- Converted date fields into appropriate SQL date formats.
- Derived product category identifiers from product keys.
- Applied product lifecycle logic using `LEAD()` and date calculations.
- Corrected inconsistent sales amounts and product prices.
- Standardized ERP customer IDs and country values.
- Integrated CRM and ERP datasets into cleaned Silver tables.

Implemented a stored procedure to manage Silver layer loading.

### 3. Gold Layer – Business-Ready Data Modeling

Designed a Star Schema consisting of fact and dimension views.

**Fact Table**

- `fact_sales` – Transactional sales information, including order details, sales amount, quantity, price, and dimension keys.

**Dimension Tables**

- `dim_customers` – Customer demographics, geography, gender, and marital status.
- `dim_products` – Product details, categories, subcategories, cost, and product line.

Implemented SQL views to combine cleaned Silver data into business-friendly analytical datasets.

## ⚙️ Data Engineering Workflow

### 1. Database & Schema Design
- Created a dedicated SQL Server database.
- Organized data into Bronze, Silver, and Gold schemas.
- Designed structured tables for CRM and ERP datasets.

### 2. Data Ingestion & Loading
- Imported multiple CSV source files using SQL Server `BULK INSERT`.
- Developed stored procedures for structured layer loading.
- Implemented full-refresh loading logic for the Silver layer.

### 3. Data Transformation
- Applied SQL-based cleansing and standardization.
- Used joins to integrate CRM and ERP datasets.
- Implemented window functions for deduplication and product lifecycle transformations.
- Applied conditional logic to handle inconsistent source records.

### 4. Data Modeling
- Designed a dimensional model using a Star Schema.
- Created customer and product dimensions.
- Developed a sales fact view connecting transactional data with dimension keys.

### 5. Data Quality & Validation
- Performed record count validation across layers.
- Checked NULL values and duplicate records.
- Validated dimension key relationships.
- Investigated unmatched fact records.

## 🛠️ Tech Stack

- **Database:** Microsoft SQL Server
- **SQL:** T-SQL
- **Database Client:** SQL Server Management Studio (SSMS)
- **Data Architecture:** Medallion Architecture
- **Data Modeling:** Star Schema, Fact & Dimension Tables
- **Data Ingestion:** CSV, BULK INSERT
- **Transformations:** Stored Procedures, SQL Views, Joins, CTEs
- **Analytical Functions:** ROW_NUMBER(), LEAD(), Window Functions

**Planned Analytics:** Python, Pandas, NumPy, Matplotlib, Seaborn, Google Colab.

## 🧪 SQL Concepts Implemented

- **Data Definition:** CREATE, ALTER, DROP, CREATE OR ALTER
- **Data Manipulation:** INSERT, UPDATE, DELETE, TRUNCATE
- **Data Transformation:** CASE, COALESCE, NULLIF
- **Data Integration:** INNER JOIN, LEFT JOIN
- **Advanced SQL:** CTEs, Subqueries, Window Functions
- **Data Loading:** BULK INSERT, Stored Procedures
- **Data Validation:** COUNT, SUM, NULL checks, duplicate detection
- **Analytical Modeling:** Views, Fact Tables, Dimension Tables

## 📊 Exploratory Data Analysis

*To be completed.*

Planned analysis includes:

- Customer demographic and geographic distribution.
- Product category and subcategory analysis.
- Revenue and sales performance analysis.
- Customer and product ranking.
- Monthly and yearly sales trends.
- Business KPI development and visualization.

## ✅ Project Outcome

This project demonstrates practical implementation of:

- End-to-end SQL-based data warehousing.
- Multi-source CRM and ERP data integration.
- Medallion Architecture implementation.
- Data cleansing and transformation using T-SQL.
- Stored procedure-based data loading.
- Dimensional modeling using Star Schema.
- Data quality checks and validation.
- Development of reusable analytical views.

**The final objective is to transform raw operational data into a structured data warehouse that supports reliable business analysis and reporting.**

---

*Detailed SQL scripts, data transformations, and validation queries are maintained in the project repository.*
