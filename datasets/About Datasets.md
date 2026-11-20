## About the Datasets

This project uses six CSV files sourced from two business systems: **CRM (Customer Relationship Management)** and **ERP (Enterprise Resource Planning)**. These datasets contain customer, product, sales, location, and product category information used to build and integrate the data warehouse.

### CRM Datasets
The CRM source provides customer-related, product, and sales information.

| File Name | Description |
|---|---|
| `cust_info.csv` | Customer demographic and profile information. |
| `prd_info.csv` | Product details and attributes. |
| `sales_details.csv` | Sales transactions and order-related information. |

### ERP Datasets
The ERP source provides additional customer, location, and product category information.

| File Name | Description |
|---|---|
| `CUST_AZ12.csv` | Additional customer-related attributes. |
| `LOC_A101.csv` | Customer location and geographic information. |
| `PX_CAT_G1V2.csv` | Product category, subcategory, and maintenance-related information. |

### Data Integration

The CRM and ERP datasets are integrated during the data warehouse development process to create a consolidated view of customers, products, and sales. The data undergoes cleansing, standardization, and validation before being transformed into analytical models for reporting and business insights.

