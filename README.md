# ESG Risk Data Pipeline Project

## 📌 Objective
Design and implement an end-to-end data engineering pipeline for analyzing ESG (Environmental, Social, and Governance) risk data for the top 500+ companies. The pipeline will:
- Process, store, and transform ESG data into analytics-ready datasets
- Include a dashboard for visualizing key insights (ESG risk distribution, trends)
- Ensure data quality, scalability, and reliability for data-driven decision making

## 🚀 Problem Statement
**Challenge:** Companies and investors struggle with ESG risk assessment due to:
- Lack of centralized, up-to-date data
- Manual, time-consuming analysis processes
- Reliance on static datasets leading to inefficiencies

## 💡 Proposed Solution
End-to-end data pipeline that processes, analyzes, and visualizes ESG risk data for top 500+ companies.

### 1. Centralized Data Ingestion
- **1.1** Collect ESG risk data from reliable sources (CSV)

### 2. Data Processing & Transformation
- **2.1** Clean/preprocess raw data (handle missing values, duplicates)
- **2.2** Derive metrics (average ESG scores by sector/industry)
- **2.3** Batch processing 

### 3. Data Warehouse & Analytics
- **3.1** Load to BigQuery (cloud data warehouse)
- **3.2** Implement dimensional modeling with dbt (fact/dimension tables)

### 4. Real-Time Monitoring (Optional)
- **4.1** Streaming pipeline (Kafka/Google Pub/Sub)
- **4.2** Stream processing (Apache Flink/Spark Streaming)

### 5. Dashboard Development
- **5.1** Data visualizations
- **5.2** Interactive filters (by sector, industry, company)

## 🛠 Technology Stack
| Category          | Tools                                                                 |
|-------------------|-----------------------------------------------------------------------|
| **Cloud Platform**| Google Cloud Platform (Compute Engine, Cloud Storage, BigQuery)       |
| **Orchestration** | Kestra (data pipeline flow)                                          |
| **Transformation**| dbt (Data Build Tool for reporting layer)                            |
| **Containerization** | Docker                                 |
| **Infrastructure**| Terraform (IaC for GCP resource deployment)                          |

## ⚙️ Implementation Highlight
### Docker Setup
   - `Dockerfile`: Environment tool installation
   - `docker-compose.yaml`: Database & pgAdmin configuration
![docker_setup](https://github.com/user-attachments/assets/a2c225b6-feca-43bb-91ce-6ec855da7cd6)
![pgadmin_esg_table](https://github.com/user-attachments/assets/778cdcf2-4daa-42b8-b968-4cb1ff3998cb)

### Data Loading
   - Jupyter Notebook: Load batch data (5 batches) to pgAdmin `sp_500_esg_risk_rating` table
![load_data_batch_2](https://github.com/user-attachments/assets/4e8cafdd-efc1-4ac1-ab51-9049d3a4de51)
   - Jupyter Notebook: data clean
![loaddata_dataclean](https://github.com/user-attachments/assets/4e793c6e-0d6f-4116-ba86-8c93f84381fa)
   - Kestra: Kestra for bucket data loading
![Kestra](https://github.com/user-attachments/assets/0490da56-9cc8-41f7-b166-7e277091cd5d)
![kestra_flow](https://github.com/user-attachments/assets/c5c9fd42-599c-43db-b1ab-2cb0a1fc02ea)
   - Google Cloud: Kestra for bucket data loading
![google_cloud_info](https://github.com/user-attachments/assets/ff3a6669-5451-42ee-adbc-8370768fddd5)
![google_cloud_bucket](https://github.com/user-attachments/assets/160e5d63-fe01-4c31-99d6-9190e144eb25)
![google_cloud_esg_risk_data](https://github.com/user-attachments/assets/d36cae1c-36f2-4526-ba38-7e34e3f5f61a)
   - dbt (Data Build Tool)
![dbt_staging](https://github.com/user-attachments/assets/0300b1cd-b6b3-4bbe-8c91-786b4cf0e03d)

## 📐 Project Architecture
![Architecture Diagram](https://github.com/user-attachments/assets/8a8859f7-f15c-4f6f-8f8d-4c8dcba6663e)

## Key Features
✔ End-to-end automated pipeline  
✔ Scalable cloud infrastructure  
✔ Analytics-ready data modeling  
✔ Interactive visualization dashboard  
