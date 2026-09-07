# ETL-Pipeline
An end-to-end Data Engineering pipeline built using Python, Google Cloud Platform, BigQuery, Apache Airflow/Cloud Composer, and Cloud Data Fusion.

The project demonstrates how raw data can be extracted, transformed, masked, and loaded into a cloud data warehouse, with workflow orchestration for automated and repeatable data processing.
# Overview
Modern data systems require reliable pipelines to move data from source systems into analytical platforms.

This project implements an ETL workflow that:

Extracts raw employee data
↓
Transforms and prepares the data
↓
Masks/encodes sensitive information
↓
Loads the processed data into Google BigQuery
↓
Orchestrates the workflow using Apache Airflow / Cloud Composer

The primary objective is to understand and implement the core concepts involved in building a cloud-based ETL pipeline.

#Tech Stack
Python - Data extraction and transformation
Google - BigQuery	Cloud data warehouse / data storage
Apache - Airflow	Workflow orchestration
Cloud - Composer	Managed Airflow environment
Cloud - Data Fusion	Data integration
Google - Cloud Platform	Cloud infrastructure
## ETL Workflow
1. Extract
The pipeline extracts the source employee data and prepares it for downstream processing.
The extraction layer is implemented using Python and the relevant Google Cloud data-integration components.

2. Transform
The extracted data is processed before being loaded into the data warehouse.
The transformation stage includes:
- Data preparation
- Data transformation
- Sensitive-data masking
- Data encoding
- Formatting data for downstream consumption
Masking sensitive information helps reduce exposure of personally identifiable information (PII) during data processing.

3. Load
After transformation, the processed data is loaded into Google BigQuery.
BigQuery acts as the analytical storage layer where the transformed dataset can be queried and used for downstream analysis.

4. Orchestration
The pipeline workflow is orchestrated using Apache Airflow / Google Cloud Composer.
Airflow allows individual pipeline tasks to be represented as a Directed Acyclic Graph (DAG), making the workflow easier to manage and automate.
Example workflow:
Extract
   ↓
Transform
   ↓
Mask / Encode
   ↓
Load to BigQuery
