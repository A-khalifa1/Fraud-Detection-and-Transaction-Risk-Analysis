# Fraud Detection and Transaction Risk Analysis

## Overview
This project implements a **fraud detection and transaction risk analysis pipeline** for a digital wallet system. The pipeline extracts data from CSV, loads it into MongoDB, transfers it to PostgreSQL using Airbyte, transforms it with dbt, and orchestrates the workflow with Kestra.

## Data Pipeline Architecture
Below is the architecture of the ELT pipeline:

![ELT Pipeline](Fraud-Detection-and-Transaction-Risk-Analysis.jpg)

## Technologies Used
- **Python & Pandas**: Data processing and transformation.
- **MongoDB**: NoSQL database for storing raw transactions.
- **Airbyte**: Extract and load data from MongoDB to PostgreSQL.
- **PostgreSQL**: Staging area and Data Warehouse.
- **dbt**: Data modeling and transformation.
- **Kestra**: Orchestration of ELT workflows.

## Data Flow
1. **CSV to JSON & MongoDB**
   - Read transaction data from CSV.
   - Convert it to JSON format.
   - Insert it into MongoDB.
2. **MongoDB to PostgreSQL Staging**
   - Airbyte extracts data from MongoDB.
   - Loads it into a staging table in PostgreSQL.
3. **PostgreSQL to Data Warehouse**
   - dbt transforms raw data into analytical models.
   - Stores the transformed data in PostgreSQL DWH.
4. **Orchestration with Kestra**
   - Automates and schedules the entire workflow.

## Data Model
The project follows a **Star Schema** with the following tables:

### Dimension Tables
- **Dim_Time**: Contains date and time-related attributes.
- **Dim_Transaction_Type**: Stores transaction categories.
- **Dim_Customer**: Information about wallet users.
- **Dim_Merchant**: Details of merchants receiving payments.
- **Dim_Device (optional)**: Device details for mobile/web transactions.
- **Dim_Location (optional)**: Geographic location data.
- **Dim_Payment_Channel**: Specifies transaction channels.
- **Dim_Fraud_Status**: Fraud classification.

### Fact Table
- **Fact_Transactions**: Stores transaction details, linking to all dimensions.

## Running the Pipeline
### Prerequisites
Ensure you have the following installed:
- Python (with Pandas, PyMongo, etc.)
- MongoDB
- PostgreSQL
- Airbyte
- dbt
- Kestra

### Steps
1. **Run the Python script to insert data into MongoDB:**
   ```bash
   python convert_to_json_connect_mongo.ipynb
   ```
2. **Configure and run Airbyte to move data to PostgreSQL.**
3. **Execute dbt transformations:**
   ```bash
   dbt run
   ```
4. **Use Kestra to orchestrate and automate tasks.**

## Future Enhancements
- Implement **incremental loading** in Airbyte for better performance.
- Enhance **data quality checks** before inserting into MongoDB.
- Add **real-time fraud detection** with stream processing tools.

---
For any issues or improvements, feel free to contribute! 🚀

