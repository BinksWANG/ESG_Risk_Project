# ESG Risk Project

Objective:
The goal of this project is to design and implement an end-to-end data engineering pipeline for analyzing ESG (Environmental, Social, and Governance) risk data for the top 500 companies. This pipeline will efficiently process, store, and transform ESG data to create analytics-ready datasets. The project will also include the development of a dashboard to visualize key insights, such as the distribution of ESG risk levels and trends over time. The pipeline will ensure data quality, scalability, and reliability, enabling stakeholders to make data-driven decisions about corporate sustainability and risk management.

Problem Statement:
Challenge: Companies and investors face significant challenges in assessing and managing ESG (Environmental, Social, and Governance) risks due to the lack of centralized, up-to-date, and actionable insights. Traditional methods of analyzing ESG data are often manual, time-consuming, and rely on static datasets, leading to inefficiencies.

Proposed Solution:
To address these challenges, we propose building an end-to-end data pipeline that processes, analyzes, and visualizes ESG risk data for the top 500 companies. The solution will include:

    • Centralized Data Ingestion:
        • Collect ESG risk data from reliable sources (CSV files) and store it in a centralized data lake (Google Cloud Storage).
        • Use batch processing to ingest and update data periodically (yearly).
    • Data Processing and Transformation:
        • Clean and preprocess the raw data to handle missing values, duplicates, and inconsistencies.
        • Transform the data to derive additional metrics, such as average ESG risk scores by sector or industry.
        • Use batch processing tools like Apache Spark or AWS Glue for efficient data transformation.
    • Data Warehouse and Analytics Engineering:
        • Load the processed data into a cloud-based data warehouse (BigQuery).
        • Use dbt (Data Build Tool) to implement dimensional modeling and create analytics-ready datasets, including fact and dimension tables.
    • Real-Time Monitoring (Optional):
        • If real-time updates are required, integrate a streaming pipeline using tools like Kafka or Google Pub/Sub to handle incoming ESG data streams.
        • Use stream processing tools like Apache Flink or Spark Streaming to analyze real-time data.
    • Dashboard Development:
        • Include visualizations such as:
            • A bar chart or pie chart showing the distribution of ESG Risk Levels (categorical data).
            • A line chart showing trends in Total ESG Risk Scores over time (temporal data).
        • Add filters and drill-down options to allow users to explore data by sector, industry, or company.

Key Aspects
✅ Which sectors have the highest ESG risks?
✅ How environmental and governance risks influence overall ESG scores?
✅ Can we predict ESG scores for companies without existing data?

Technology Stack
    • Google Cloud Platform (GCP)
	    • Compute Engine: Hosting VM instance.
	    • Google Cloud Storage (Datalake): Where data lands.
	    • BigQuery (Datawarehouse): Where data is stored in dimensional modeling.
	    • Spark (Data Processing Layer): Local cluster on VM instance.
    • Mage
        • Orchestration Tool: Used for our data pipeline flow.  (kestra)
    • DBT (Data Build Tool)
        • Reporting Layer: Built in models.
    • Docker
        • Containerization: Wrapping Mage and Spark in containers.
    • Terraform (Infrastructure as Code)
        • Deployment: Used to deploy all the needed resources on GCP.

data pipeline: batch  
setup docker: 
    Dockerfile: install tool for the enviroment
    docker-compose.yaml: setup the database, pgadmin  
load data:
    jupyter notebook: load data batches (5 batches) to pgadmin sp_500_esg_risk_rating table\
    google cloud service: using kestra load data to bucket

Project Architacture Overview (image)

Data Flow

EJ15PMUELYPLQ4TP4Z14K744  dbtcode