# Stock Market Real-Time Data Analysis

## 1. Introduction
This project demonstrates a real-time stock market data analysis system that captures live stock data, processes it using a data pipeline, and provides insights. The system utilizes **Apache Kafka** to fetch and stream real-time stock data, while **Python** is used to simulate stock market trends and analyze the data. The processed data is then stored in **AWS S3**. Using **AWS Glue Crawler** and **Glue Catalog**, the data is cataloged and prepared for querying. Finally, **AWS Athena** is used to run SQL queries on the stored data, allowing for insightful analysis and trend identification.

## 2. Architecture Diagram
![Architecture Diagram](C:\Users\sahil\OneDrive\Documents\Stock Market Project)

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
For detailed steps executed for the project, including screenshots and codes, please refer to the [Execution Guide](docs/execution_guide.md). This guide will walk you through the process from setting up Kafka to python code.

## 5. Dataset Used
The dataset contains stock market data. You can download it [here](C:\Users\sahil\OneDrive\Documents).

---

This version now includes a brief introduction, a list of technologies used in a more organized format, and a concise execution section pointing to a separate document. Let me know if you’d like any further tweaks!
