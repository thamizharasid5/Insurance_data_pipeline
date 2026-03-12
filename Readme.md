##### 🏦 Automated ETL Pipeline for Insurance Data



##### 📖 Overview



##### This project is an Automated ETL Pipeline designed to process insurance claims data from multiple sources.

##### It demonstrates Azure Databricks orchestration, parameterization, and performance tuning to deliver curated 

##### datasets for analytics and reporting.

##### 

##### ✨ Features





##### Automated Data Ingestion → Reads raw insurance claims from CSV/Parquet stored in Azure Data Lake Gen2.

##### 

##### Data Transformation → Cleans, deduplicates, and applies business rules using PySpark.

##### 

##### Efficient Data Loading → Stores curated outputs into Delta Lake (Bronze → Silver → Gold zones).

##### 

##### Job Orchestration → Managed via Databricks Jobs with parameters, dependencies, and scheduling.

##### 

##### Monitoring \& Debugging → Spark UI analysis, cluster logs, and job notifications.

##### 

##### Scalability → Optimized with partitioning, caching, and pushdown filters.





##### 

##### 🛠️ Technologies Used





##### Azure Databricks → ETL orchestration and PySpark transformations

##### 

##### Azure Data Lake Gen2 → Storage (Bronze, Silver, Gold zones)

##### 

##### Azure Data Factory (ADF) → Pipeline scheduling and triggers

##### 

##### PySpark / SQL → Data processing and aggregation

##### 

##### GitHub → Version control and CI/CD integration





##### 

##### 📊 Dataset



##### Synthetic Insurance Claims Data with fields:

##### 

##### Claim ID, Claim Type, Claim Date, Amount, Customer ID, Fraud Flag

##### 

##### Used to demonstrate fraud detection thresholds and claims aggregation





##### 

##### 🏗️ Architecture



##### mermaid

##### graph TD

##### &nbsp;   A\[Raw Insurance Data - Bronze] --> B\[Cleaning \& Deduplication - Silver]

##### &nbsp;   B --> C\[Aggregation \& Business Rules - Gold]

##### &nbsp;   C --> D\[Curated Delta Tables for Analytics]







##### 📐 Data Model



##### <img src="Pipeline Architecture.png">

##### 

##### Claims Table → Raw claim records

##### 

##### Aggregated Claims Table → Claims grouped by type and date

##### 

##### Fraud Detection Table → Claims flagged above threshold





##### 

##### ⚙️ Parameters



##### Key	Example Value	Purpose

##### run\_date	2026-03-11	Controls which day’s data to process

##### env	dev / prod	Switches between environments

##### threshold	0.8	Fraud detection cutoff







##### 🛠️ Project Structure



##### Code

##### Insurance-ETL-Pipeline/

##### │-- notebooks/

##### │   │-- 01\_insurance\_clean\_transform.ipynb

##### │   │-- 02\_insurance\_agg\_pipeline.ipynb

##### │-- configs/

##### │   │-- parameters.json

##### │-- README.md







##### 🚀 Usage



##### Configure parameters (run\_date, env, threshold) in Databricks Job UI.

##### 

##### Trigger the job manually or via ADF scheduler.

##### 

##### Monitor execution in Jobs → Runs → Spark UI.

##### 

##### Query curated tables in the Gold Zone for analytics.





##### 

##### 📊 Monitoring





##### Databricks Job Runs → Track task durations and statuses

##### 

##### Spark UI → Identify shuffle bottlenecks, skew, and disk spills

##### 

##### Cluster Logs → Review executor performance and memory usage





##### 

##### 🎯 Business Impact





##### Reduced ETL job runtime by 40% through shuffle optimization

##### 

##### Delivered curated Delta tables enabling risk analysis and claim trend reporting

##### 

##### Automated daily runs with retry policies and notifications for reliability





##### 

##### 📜 License



##### This project is licensed under the MIT License.

