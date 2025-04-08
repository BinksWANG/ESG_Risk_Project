# ESG Risk Project

Objective:
The goal of this project is to design and implement an end-to-end data engineering pipeline for analyzing ESG (Environmental, Social, and Governance) risk data for the top 500 companies. This pipeline will efficiently process, store, and transform ESG data to create analytics-ready datasets. The project will also include the development of a dashboard to visualize key insights, such as the distribution of ESG risk levels and trends over time. The pipeline will ensure data quality, scalability, and reliability, enabling stakeholders to make data-driven decisions about corporate sustainability and risk management.

Problem Statement:
Challenge: Companies and investors face significant challenges in assessing and managing ESG (Environmental, Social, and Governance) risks due to the lack of centralized, up-to-date, and actionable insights. Traditional methods of analyzing ESG data are often manual, time-consuming, and rely on static datasets, leading to inefficiencies.

Proposed Solution:
To address these challenges, we propose building an end-to-end data pipeline that processes, analyzes, and visualizes ESG risk data for the top 500 companies. The solution will include

1. Centralized Data Ingestion:

	1.1 Collect ESG risk data from reliable sources (CSV files) and store it in a Google Cloud Storage.

	1.2 Use batch processing to ingest and update data periodically (yearly).


2. Data Processing and Transformation:

	2.1 Clean and preprocess the raw data to handle missing values, duplicates, and inconsistencies.

	2.2 Transform the data to derive additional metrics, such as average ESG risk scores by sector or industry.

	2.3 Use batch processing tools like Apache Spark or AWS Glue for efficient data transformation.

3. Data Warehouse and Analytics Engineering:

	3.1 Load the processed data into a cloud-based data warehouse (BigQuery).

	3.2 Use dbt (Data Build Tool) to implement dimensional modeling and create analytics-ready datasets, including fact and dimension tables.

4. Real-Time Monitoring (Optional):

	4.1 If real-time updates are required, integrate a streaming pipeline using tools like Kafka or Google Pub/Sub to handle incoming ESG data streams.

	4.2 Use stream processing tools like Apache Flink or Spark Streaming to analyze real-time data.
    
5. Dashboard Development:
        
	5.1 Data visualizations
                
	5.2 Add filters and drill-down options to allow users to explore data by sector, industry, or company.


Technology Stack
    
    • Google Cloud Platform (GCP)
	 
        • Compute Engine: Hosting VM instance.
	    
        • Google Cloud Storage (Datalake): Where data lands.
	    
        • BigQuery (Datawarehouse): Where data is stored in dimensional modeling.
	    

    • kestra
       
        •  Used for our data pipeline flow.  

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

Project Architacture Overview

![looker_1](https://github.com/user-attachments/assets/8a8859f7-f15c-4f6f-8f8d-4c8dcba6663e)

