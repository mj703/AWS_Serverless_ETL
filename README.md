# AWS_Serverless_ETL 

## Overview

This project involves building a data engineering pipeline on AWS cloud using various services such as AWS Lambda, AWS Glue, AWS Athena, AWS S3, AWS CloudWatch, and AWS SNS. The goal is to create an end-to-end solution for processing data from DynamoDB triggers, storing it in a staging layer on S3, performing ETL using Glue, and querying the transformed data using Athena.

## Project Architecture 

![Project Architecture Diagram](architecture_diagram_updated.gif)

## Project Steps

### Step 1: Setting up Lambda Function

- Create a Lambda function to handle DynamoDB triggers.
- Integrate Lambda function with CloudWatch for monitoring.
- Set up DynamoDB trigger to automatically invoke Lambda function.
- Implement CloudWatch alarms and metrics for monitoring Lambda function performance.

### Step 2: Storing Data in Staging Layer

- Create a Lambda function to process data from DynamoDB triggers.
- Format the data and store it in a staging layer on S3.
- Utilize AWS SNS to notify on successful data processing.
- Use Pandas and Boto3 libraries for data processing and S3 interaction.

### Step 3: Building ETL Pipeline with AWS Glue

- Write a Glue job script to process data from the staging layer.
- Use Spark engine for data processing.
- Join and merge data from different sources.
- Save the transformed data into a data warehouse.
- Implement CloudWatch logs for Glue job monitoring.

### Step 4: Querying Data with AWS Athena

- Run a Glue crawler to populate tables in a database.
- Use Athena to query the data in the database.
- Write SQL-like queries to analyze and retrieve insights from the data.

## Tools and Techniques Used

- AWS Lambda: For serverless execution of code in response to events.
- AWS Glue: For ETL (Extract, Transform, Load) processing of data.
- AWS Athena: For querying data stored in S3 using SQL-like syntax.
- AWS S3: For storing raw and transformed data.
- AWS CloudWatch: For monitoring Lambda function and Glue job performance.
- AWS SNS: For notification on successful data processing.
- Pandas: For data manipulation and processing.
- Boto3: For interacting with AWS services programmatically.

## Conclusion

This project demonstrates the implementation of a data engineering solution on AWS cloud, covering data ingestion, transformation, and querying. By leveraging serverless and managed services, the project ensures scalability, reliability, and cost-effectiveness.



