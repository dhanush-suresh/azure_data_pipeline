# azure_data_pipeline
# Azure Data Pipeline Project

This project involves the design and implementation of a robust data pipeline on Microsoft Azure, utilizing the Medallion Architecture to enhance data governance, accessibility, and efficiency. The pipeline orchestrates data flows from Azure SQL Server using Azure Data Factory to process and transform data for downstream analytics.


## Project Overview

The Azure Data Pipeline project is designed to process large datasets efficiently using the Medallion Architecture. The pipeline consists of multiple stages that work together to ensure the data is cleaned, transformed, and stored in a way that supports easy access and governance.

Key features:
- **Medallion Architecture**: Implemented to structure data processing into bronze, silver, and gold layers.
- **Data Orchestration**: Managed by Azure Data Factory, allowing automated data extraction, transformation, and loading (ETL).
- **Data Source**: The pipeline ingests data from **Azure SQL Server**, processes it using various transformations, and makes it available for analytics and reporting.

## Technologies Used

- **Azure Data Factory**: Orchestrates data pipelines, scheduling, and automates data movement.
- **Azure SQL Server**: Data storage for raw data and intermediate datasets.
- **Medallion Architecture**: Bronze (raw data), Silver (cleaned and transformed data), Gold (aggregated and reporting-ready data).
- **Azure Blob Storage**: Stores data files in the pipeline stages.
- **Python**: Used for custom transformations and scripting.
- **Azure Databricks**: Used for more complex data processing tasks (optional).

## Pipeline Overview
Pipeline Workflow
- **Bronze Layer**:

Raw data is ingested from the Azure SQL Server and stored in the bronze layer in Blob Storage.
Data at this stage is unprocessed and uncleaned.
- **Silver Layer**:

Data from the bronze layer is processed and cleaned.
Transformations include removing duplicates, filling missing values, and standardizing formats.
Cleaned data is stored in the silver layer.
- **Gold Layer**:
  
Aggregation and advanced transformations are applied to the data.
This layer contains data that is ready for reporting and analytics.
The gold layer data is stored in a format optimized for business intelligence tools.
Orchestration:

Azure Data Factory orchestrates the movement of data between each layer.
The pipeline can be scheduled to run periodically to update the data in the gold layer for use in real-time analytics.

