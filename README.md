# NYC-TAXI Analytics | Modern DE Project

## **Introduction**
This modern data engineering project leverages the power of Azure to analyze NYC taxi trip data. We built an end-to-end pipeline, ingesting data via HTTP API, dynamically pulling data to Azure Data Factory and orchestrating transformations with Databricks, and storing insights in Azure Data Lake for analysis.

## **Architecture**
In this project **Medallion Architecture** is used

![Project Architecture](Architecture.png)

## Technologies Used
1. Progarmming language - Python
2. Scripting Language - SQL
3. Azure Cloud Platform
     - Data Factory: for orchestrating the data pipeline and moving data
     - Databricks: for scalable data processing and transformations using PySpark/SQL
     - Cloud Storage - Data Lake: for storing raw (Bronze), transformed (Silver), and aggregated (Gold) data.
     - **PowerBI** - Used for connecting to Azure Databricks (or the processed data in the Data Lake) to visualize the analyzed data and create insightful dashboards.
  
## **File Types Used**
1. **Parquet** - bronze , silver
2. **Delta Lake** - gold


## **Security Management**
1. Key Vault
2. Service Principle

   
## **Dataset Used**
   **NYC Taxi Trip Data - Green Line**
   
This repository contains the code and documentation for a data engineering project focused on analyzing the **Green Taxi Trip Records** from the New York City Taxi and Limousine Commission (TLC). This dataset provides detailed information about individual taxi trips (for green taxis), including pickup and dropoff times and locations, passenger count, trip distance, fare amounts, and payment types. The analysis in this project focuses on the Green Taxi Trip Records for January 2023. The data was accessed via **a public HTTP API (for initial ingestion)** and/or **downloaded as Parquet files from the TLC website**.

Original Dataset - https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2023-01.parquet

## **Scripts for Project**
1. **Bronze** - (bronze.zip) - Contains scripts for ingesting the raw data from the source.
2. **Silver** - (silver.dbc) - Contains Databricks notebooks/scripts for cleaning, transforming, and enriching the raw data.
3. **Gold** - (gold.dbc) - Contains Databricks notebooks/scripts for aggregating and preparing the data for analytical consumption.
