# 🚀 End-to-End Azure Data Engineering Project

This project demonstrates a complete Azure-based data engineering solution, built using free-tier Azure resources. It connects and integrates major Azure services to build a dynamic, scalable, and efficient pipeline.

---

## 🧱 Architecture Overview

Please look at the Data Architecture.png

---

## 🧰 Tools & Services Used

- **Azure Data Factory (ADF)** – for data ingestion  
- **Azure Data Lake Storage Gen2** – for layered storage (Raw & Silver & Gold)  
- **Azure Databricks** – for scalable transformation  
- **Azure Synapse Analytics** – for querying with external tables  
- **Power BI** – for visualization  
- **GitHub** – for source control and data source  

---

## 📥 Data Ingestion (ADF → Data Lake RAW Layer)

- Parameterized ADF pipeline ingests data dynamically from GitHub.  
- Stored in the **RAW** layer of Azure Data Lake.

> ✅ Uses parameterized dataset, linked services, and dynamic content in pipeline expressions.

---

## 🔄 Data Transformation (Databricks)

- Databricks used for scalable and complex transformations.  
- Transformed data is written to the **Silver** layer in Data Lake.

> ✅ Databricks connected securely using **Entra ID** and **service principal authentication**.

---

## 🧮 Synapse Analytics

- External tables created on top of Silver Layer using **serverless SQL pools**.  
- Enabled querying structured data stored in parquet format.

---

## 📊 Power BI Integration

- Connected to Synapse SQL pool.  
- Built interactive dashboards to visualize insights.

---

## 📁 Folder Structure

```text
📂datasets           → Sample datasets  
📂notebooks          → Databricks notebooks  
📂adf_json           → Exported ADF pipeline JSONs  
📂synapse            → SQL scripts for Synapse external tables  
📂powerbi            → Screenshots or Power BI files  
📄architecture-diagram.png → System architecture  
📄README.md          → Project documentation  
