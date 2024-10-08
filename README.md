# Stock Market Real-Time Data Analysis

## 1. Introduction
This project demonstrates a real-time stock market data analysis system that captures live stock data, processes it using a data pipeline, and provides insights. The system utilizes **Apache Kafka** to fetch and stream real-time stock data, while **Python** is used to simulate stock market trends and analyze the data. The processed data is then stored in **AWS S3**. Using **AWS Glue Crawler** and **Glue Catalog**, the data is cataloged and prepared for querying. Finally, **AWS Athena** is used to run SQL queries on the stored data, allowing for insightful analysis and trend identification.

## 2. Architecture Diagram
![Architecture Diagram](https://drive.google.com/uc?export=view&id=1REgCj-1dOSLVk85PCmsHEn_2u5vsveJc)

## 3. Technologies Used
- **Programming Language**: Python
- **Apache Kafka**
- **Amazon Web Services (AWS)**  
  - **EC2**
  - **S3 (Simple Storage Service)**
  - **Athena**
  - **Glue Crawler**
  - **Glue Catalog**

## 4. Execution
For detailed steps executed for the project, including screenshots and codes, please refer to the [Execution Guide](./Execution%20Guide.md). This guide will walk you through the process from setting up Kafka to python code.

## 5. Dataset Used
The dataset contains stock market data. You can download it [Here](https://drive.google.com/uc?export=download&id=1aKdndcA-8rgXHk4t2n2yBUkeaMb1tDZb).
