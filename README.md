# DLH Sales Performance Lakehouse Pipeline (PySpark)
##  Project Overview

This project implements an end-to-end Sales Performance Data Lakehouse pipeline using PySpark and Delta Lake, following the **Medallion Architecture (Bronze → Silver → Gold).**

The pipeline is designed to ingest raw source data, clean and standardize it, and produce analytics-ready dimension and fact tables for reporting and downstream consumption.

The entire workflow is orchestrated using Databricks Jobs & Pipelines, ensuring modular, scalable, and maintainable data processing.

### Technology Stack

	•	Language: PySpark
	•	Storage Format: Delta Lake
	•	Processing Engine: Apache Spark (Databricks Runtime)
	•	Orchestration: Databricks Jobs & Pipelines
	•	Architecture Pattern: Medallion (Bronze → Silver → Gold)

## Architecture & Data Flow

The pipeline follows a layered approach:

### Bronze Layer – Raw Ingestion
	•	Ingests raw data from multiple source systems:
	•	Customer master
	•	Customer attributes
	•	Location data
	•	Product master
	•	Product category hierarchy
	•	Sales transaction details
	•	Stores data in Delta format with minimal transformation
	•	Preserves source structure and ingestion metadata for traceability

### Silver Layer – Cleansed & Conformed Data
	•	Applies data cleansing, standardization, and normalization
	•	Handles:
	•	Data type corrections
	•	Null handling and deduplication
	•	Business rule validations
	•	Creates query-optimized Delta tables
	•	Uses partitioning (e.g., event/date fields) to enable source-level filtering and partition pruning
  
### Gold Layer – Analytics-Ready Models
	•	Builds business-friendly tables:
	•	dim_customers
	•	dim_products
	•	fact_sales_details
	•	Implements dimensional modeling concepts
	•	Optimized for reporting, dashboards, and ad-hoc analytics


### Key Features
	•	End-to-end Lakehouse architecture
	•	Modular notebooks for each pipeline stage
	•	Scalable transformations using Spark SQL & DataFrame APIs
	•	Partitioned Silver tables for efficient filter pushdown
	•	Clear separation of ingestion, transformation, and analytics layers
	•	Production-style pipeline orchestration and dependency management

### Learning Outcomes

##### Through this project, I demonstrated:

	•	Practical implementation of Lakehouse design principles
	•	Hands-on experience with PySpark transformations
	•	Data modeling using dimension and fact tables
	•	Designing pipelines optimized for performance and scalability
	•	Real-world orchestration using Databricks workflows
