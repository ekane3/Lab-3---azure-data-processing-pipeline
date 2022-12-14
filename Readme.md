---
page_type: sample
languages:
  - python
products:
  - azure
  - azure-storage
  - azure-data-lake
  - azure-data-factory
  - azure-databricks
urlFragment: storage-datalake-samples
---

# Azure Storage Datalake / Data Integration / Data Pipeline

The objective of this repository is to build a data pipeline that will ingest data(stocks data) from a data lake, transform it and load it into a data warehouse. The data lake is a blob storage container that contains a set of files in CSV format. The data warehouse is a SQL database.  

Then we will couple Azure Databricks to the pipeline to perform some data analysis in a notebook taking data from Azure Data Warehouse.

**Architecture :**


**Steps :**

- Step 1 : Create a script to upload the data to the data lake. The data is in CSV format and is stored in a folder called "stocks_data". The script will upload the data to a folder called "datalake" in the storage account.
- Step 2 : Create a Batch Activity in Azure Data Factory to trasnform all csv files in the data lake to a single file called "stocks_data.csv" and store the file in the data lake.

- Step 3 : Create a copy data activity in Azure Data Factory to copy the transformed file from the SQL datalake to a table called "stocks_data_copy" in the SQL database.

- Step 4 : Create a notebook in Azure Databricks to perform some data analysis on the data in the SQL database. And at the end of these analysis, we will store the results of the output in a Data Storage.

**Data :**
> 👉🏾Link : Get it  [here](https://drive.google.com/file/d/1F63LhH7LycfQPiFpjVTqg5mWe2t_YiLy/view)
<br>  

**Tools :**
- Azure CLI
- Azure Storage Account
- Azure Data Factory
- Azure Data Lake
- Azure Databricks
- Azure SQL Database

**Demo of the pipeline :**

*"Coming soon..."*