# 🚀 End-to-End Data Lakehouse Project on Databricks

Welcome to my Data Engineering Bootcamp project! This repository contains the code for building a scalable **Data Lakehouse** using the **Medallion Architecture** (Bronze, Silver, Gold layers) on **Databricks**.

The project processes E-commerce/Retail data (Sales, CRM, Products) to enable analytics and reporting.

---

## 🏗️ Architecture Overview

I have implemented the **Multi-Hop (Medallion) Architecture** to ensure data quality and reliability:

1.  **Bronze Layer (Raw):** Ingests raw data from external sources (CSV/JSON) into Delta tables with minimal transformation.
2.  **Silver Layer (Cleaned & Conformed):** Performs data cleaning, deduplication, schema enforcement, and joins (e.g., combining Sales and CRM data).
3.  **Gold Layer (Curated):** Business-level aggregates ready for dashboards and reporting (BI).

---

## 🛠️ Tech Stack & Tools

* **Cloud Platform:** Databricks (Community/Standard Edition)
* **Language:** Python (PySpark), SQL
* **Data Format:** Delta Lake (Open source storage layer)
* **Orchestration:** Databricks Workflows (Jobs)
* **Version Control:** GitHub Integration

---

## 📂 Repository Structure

Here is an overview of the key files and folders in this repository:

| File / Folder Name | Description |
| :--- | :--- |
| **`init_lakehouse.ipynb`** | Setup script to initialize the Lakehouse environment (Creating Catalogs, Schemas, and Volumes). |
| **`bike_lakehouse_2026/Bronze.ipynb`** | Ingestion logic to read raw files and write to the **Bronze** Delta layer. |
| **`silver_crm_prd_info.ipynb`** | Transformations for Product & CRM data (Silver Layer). |
| **`silver_crm_sales_details.ipynb`** | Cleaning and processing Sales transaction data (Silver Layer). |
| **`Silver_Orchestration.ipynb`** | A master notebook/script to orchestrate the execution of multiple Silver layer notebooks sequentially or in parallel. |

---

## 🔑 Key Features Implemented

* **Delta Lake & ACID Transactions:** Used Delta format to ensure data integrity during write operations.
* **Schema Enforcement:** Handling schema evolution and data type validation.
* **Orchestration:** Automated the data pipeline using Databricks Jobs to run notebooks in a specific dependency order.
* **Data Partitioning:** Optimized storage by partitioning large tables for faster query performance.

---

## 🚀 How to Run

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/amir0322/data_engineer_bootcamp_project.git](https://github.com/amir0322/data_engineer_bootcamp_project.git)
    ```
2.  **Import to Databricks:**
    * Go to your Databricks Workspace.
    * Select **Repos** > **Add Repo** and paste the GitHub URL.
3.  **Run Initialization:**
    * Execute `init_lakehouse.ipynb` first to set up the database and paths.
4.  **Execute Pipeline:**
    * Run the notebooks in order (Bronze -> Silver) or simply trigger the `Silver_Orchestration.ipynb` notebook.

---

## 👨‍💻 Author

**[Amir Zaheer]**
*Data Science Student at Superior University*
*Aspiring Data Engineer*

[LinkedIn Profile Link:https://www.linkedin.com/in/amir-zaheer-b1b40a258/]
