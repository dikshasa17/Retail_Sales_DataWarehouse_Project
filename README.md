# Retail Sales Data Warehouse and Analytics Project

This repository contains the complete materials for a SQL Server Data Warehouse project, including source datasets, SQL scripts, documentation, and data quality tests.

## Repository Structure

```text
sql-data-warehouse-project/
├── datasets/              # Six source CSV files
│   ├── source_crm/        # CRM source data - Customer Relationship Management
│   └── source_erp/        # ERP source data - Enterprise Resource Planning
├── 02_docs/                # Requirements, architecture, diagrams, and documentation
├── 03_scripts/             # SQL scripts organized by project phase
│   ├── init_database.sql   # Database initialization script
│   ├── bronze/             # Raw data ingestion
│   ├── silver/             # Data cleansing and transformation
│   └── gold/               # Analytical data modeling
└── 04_tests/                # Data quality and validation scripts
```

## Project Overview

This project demonstrates the development of a modern SQL Server Data Warehouse by integrating data from two source systems: CRM (Customer Relationship Management) and ERP (Enterprise Resource Planning).

The data is processed through a structured Medallion Architecture consisting of Bronze, Silver, and Gold layers, transforming raw source files into clean, integrated, and analytics-ready datasets.

### Data Architecture

- **Bronze Layer:** Ingests raw data from CRM and ERP CSV files into SQL Server while preserving the original source data.
- **Silver Layer:** Cleans, standardizes, validates, and integrates the data to improve quality and consistency.
- **Gold Layer:** Organizes business-ready data into a dimensional model, including fact and dimension tables, to support analytical reporting.

## Project Objectives

- Design and implement a modern Data Warehouse using SQL Server.
- Integrate data from multiple source systems (CRM and ERP).
- Develop ETL pipelines for data ingestion, transformation, and loading.
- Implement data quality checks and validation.
- Build a business-oriented data model using fact and dimension tables.
- Develop SQL-based analytics to extract meaningful business insights.
- Document the architecture, data model, and implementation process.

## Data Engineering Scope

### Data Sources
- CRM: Customer, product, and sales-related datasets.
- ERP: Customer, location, and product category datasets.

### Data Processing
- Raw data ingestion into the Bronze layer.
- Data cleansing and standardization in the Silver layer.
- Data integration and dimensional modeling in the Gold layer.
- Data quality testing and validation across the warehouse.

### Data Modeling
- Fact and dimension table design.
- Star schema implementation.
- Relationships and key management.
- Business-oriented analytical data structures.

### Data Analytics

SQL-based analysis focused on:

- Customer behavior and segmentation.
- Product performance.
- Sales trends.
- Revenue analysis.

## Tools & Technologies

- **SQL Server**
- **SQL Server Management Studio (SSMS)**
- **SQL**
- **Git & GitHub**

## Project Requirements

### Data Warehouse Development

Build a centralized Data Warehouse to consolidate sales-related data from CRM and ERP source systems, improve data quality, and provide a unified data model for analytical workloads.

The warehouse focuses on the latest available dataset without implementing historical data tracking.

### Analytics & Reporting

Develop SQL queries to analyze customer behavior, product performance, and sales trends, providing insights that support business decision-making.

## Data Flow

```text
CRM & ERP Source Files
        |
        v
   Bronze Layer
   (Raw Ingestion)
        |
        v
   Silver Layer
 (Clean & Standardized)
        |
        v
    Gold Layer
 (Dimensional Modeling)
        |
        v
  SQL Analytics & Insights
```

## Repository Contents

- Source datasets
- Database initialization scripts
- Bronze, Silver, and Gold SQL scripts
- Project requirements and documentation
- Architecture and data model diagrams
- Data quality and validation scripts

## Acknowledgments

This project is based on the Data Warehouse learning project by [Data With Baraa](https://github.com/DataWithBaraa/sql-data-warehouse-project), used as a learning reference for Data Warehouse architecture, SQL development, ETL, and dimensional modeling.

If you find this repository helpful, consider giving the original project a star.
