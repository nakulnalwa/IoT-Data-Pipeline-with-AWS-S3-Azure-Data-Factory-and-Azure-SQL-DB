# IoT-Data-Pipeline-with-AWS-S3-Azure-Data-Factory-and-Azure-SQL-DB
# Overview
This project demonstrates the creation of an end-to-end data pipeline for processing IoT device data. The pipeline ingests raw data from an IoT device, validates it, and stores it in an Azure SQL Database. The key components include AWS S3, Azure Data Factory (ADF), and an Azure Function.
#Architecture
![image](https://github.com/nakulnalwa/IoT-Data-Pipeline-with-AWS-S3-Azure-Data-Factory-and-Azure-SQL-DB/assets/47208563/5da2a5ba-539d-4f2e-8acd-fa8d9ec12d8f)
1. IoT Device: The IoT device sends data to AWS S3 storage.
2. Data Extraction: An ADF pipeline extracts data from Amazon S3 and loads it into Azure Data Lake Storage (ADLS).
3. Data Validation: An Azure Function evaluates the JSON data for validity. Invalid data is routed to a rejected folder, while valid data is sent to a staging folder.
4. Data Loading: Another ADF pipeline moves data from the staging folder to an Azure SQL Database.

# Repository Contents
1. ADF JSON Code: The JSON code for the ADF pipeline is responsible for extracting data from AWS S3 to the ADLS landing folder.
2. ADF SQL Code: The ADF pipeline code for pushing data from the staging folder to the Azure SQL DB.
3. Azure Function App Code: The code for the Azure Function that validates the IoT data.

# Usage
- Set up your AWS S3 bucket and configure the IoT device to send data there.
- Create an Azure Data Factory instance.
- Upload the ADF JSON code to create the extraction pipeline.
- Deploy the Azure Function app code to validate the data.
- Configure the ADF SQL pipeline to load data into the Azure SQL DB.

# Contributions
Feel free to contribute by improving the code, adding features, or suggesting enhancements. Let’s build a robust and efficient IoT data pipeline together! 🚀




   
