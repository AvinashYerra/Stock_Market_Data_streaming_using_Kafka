Project Overview:
This project demonstrates a real-time data pipeline for processing and analyzing stock data using Apache Kafka, AWS S3, AWS Glue, and AWS Athena. The pipeline simulates real-time stock data streaming and provides an end-to-end workflow for ingestion, storage, cataloging, and querying.

Workflow
Dataset Preparation:
A stock dataset is customized using random sampling to simulate real-time data streams.

Kafka Producer:
Streams the sampled stock data to a Kafka topic, acting as a real-time data producer.

Kafka Consumer:
Consumes data from the Kafka topic in real time.
Saves the data to an AWS S3 bucket in a structured format (e.g., JSON or CSV).

AWS Glue:
An AWS Glue crawler scans the S3 bucket and automatically infers the schema of the stored data.
The schema is registered in the AWS Glue Data Catalog.

AWS Athena:
Athena queries the stock data directly from the S3 bucket using the Glue Data Catalog for schema definitions.

Technologies Used
Apache Kafka: For real-time data streaming.
AWS S3: To store consumed stock data.
AWS Glue: To infer the schema and create a data catalog.
AWS Athena: For querying and analyzing the stock data.
pandas: For dataset preparation and customization.
Python: To implement Kafka producer and consumer scripts.

Setup and Execution:
Prerequisites:
AWS Account with access to S3, Glue, and Athena.
Apache Kafka installed and running locally or on an EC2 instance.
Python Environment with necessary libraries installed.
Steps to Run

Dataset Customization:
Load a stock dataset and generate a random sample to simulate streaming data.

Start Kafka:
Set up and start the Kafka broker and Zookeeper service.
Create a topic (e.g., stock_topic) for streaming data.

Run Kafka Producer:
Stream the sampled stock data to the Kafka topic.

Run Kafka Consumer:
Consume data from the Kafka topic in real-time.
Store the consumed data in an AWS S3 bucket in a structured format.

Run AWS Glue Crawler:
Set up a Glue crawler to scan the S3 bucket and infer the schema.
Check the Glue Data Catalog for the created table.

Query Data with Athena:
Use Athena to run SQL queries on the stock data for analysis.
