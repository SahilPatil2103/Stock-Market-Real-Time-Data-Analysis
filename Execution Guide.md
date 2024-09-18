# Stock Market Real-Time Data Analysis Execution Guide

This document provides a step-by-step guide on executing the project along with screenshots and code from the Jupyter Notebook.

## Step 1: Kafka Setup

To set up **Apache Kafka** on your machine, ensure you have installed Zookeeper and Kafka correctly. [Click here](Kafka Setup.md) for the installation guide.

Once Kafka is set up, you will need to run the following services:
1. **Zookeeper**: Starts the Zookeeper instance needed by Kafka.
 
![Zookeeper Terminal](https://drive.google.com/uc?export=view&id=1riMapgm_q-a16L7vKqB4rX8cLga18-Z2)

2. **Kafka Server**: Starts the Kafka broker to handle messaging.
 
![Kafka Server Terminal](https://drive.google.com/uc?export=view&id=130LbfYCPiahwIc0ymHPH7JNAxyuouUAL)

3. **Kafka Producer**: Publishes data to a Kafka topic.
 
![Kafka Producer](https://drive.google.com/uc?export=view&id=11g98ISG75gaklvxubomHAATXl2lJ3fKN)

4. **Kafka Consumer**: Consumes the real-time data from the topic.
 
![Kafka Consumer](https://drive.google.com/uc?export=view&id=1I6kMWUGSR7PsVqsY0fNMDuErb9Zys82U)

---

## Step 2: Running Python Scripts for Producer and Consumer

Use the provided Python scripts to simulate real-time stock market data and stream it to Kafka topics. These scripts will handle producing and consuming data.

- [Producer Jupyter Notebook](KafkaProducer1.ipynb)
- [Consumer Jupyter Notebook](KafkaConsumer1.ipynb)

---

## Step 3: Store Data in AWS S3

After consuming the data, it is processed and stored in an **AWS S3** bucket for further analysis.

### S3 Screenshot:
![AWS S3 Bucket](https://drive.google.com/uc?export=view&id=11Xz2ELoX0bAuz95orhX_Fiw1Ih_hew-v)

---

## Step 4: Catalogue Data in AWS Glue & Crawler

To organize and manage the data in S3, a **Crawler** is set up in **AWS Glue**. The Crawler automatically catalogs the data in the Glue Data Catalog, making it ready for querying with Athena.

### Crawler and Glue Screenshots:
![AWS Glue Crawler](https://drive.google.com/uc?export=view&id=1oX8bkiXwJXhXGMsrmWN2hylL2a4WfkrH)
![AWS Glue](https://drive.google.com/uc?export=view&id=1FhyH4IAu_mI_q7az-fGRXeDUhNibJAN0)

---

## Step 5: Query Data in AWS Athena

Run **SQL queries** on the stored data using **AWS Athena** to generate insights and analyze the stock data.

### Athena Screenshot:
![AWS Athena](https://drive.google.com/uc?export=view&id=1gYzGZ66khtQc08jVfBzJMagSos2qRU9P)

