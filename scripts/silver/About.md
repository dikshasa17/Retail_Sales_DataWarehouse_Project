# Silver Layer – Data Cleaning & Transformation (Short)
In the Silver layer, we performed the following transformations on Bronze data:
- Deduplication: Removed duplicate customer records using ROW_NUMBER().
- Data cleaning: Removed extra spaces using TRIM().
- Standardization: Converted marital status, gender, product line, and country codes into consistent readable values.
- NULL handling: Replaced missing values with defaults like n/a or 0.
- Data validation: Handled invalid dates and future birthdates.
- Data correction: Corrected inconsistent sales and price values.
- Derived columns: Extracted product/category IDs and calculated product end dates.
- Load timestamp: Added dwh_create_date to track when data was loaded.
In simple words: Bronze stores raw data, Silver cleans, validates, standardizes and corrects it, and Gold organizes it for business analysis.
