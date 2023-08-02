# Data Engineering YouTube Analysis Project

## Overview
This project aims to securely manage, streamline, and perform analysis on the structured and semi-structured YouTube videos data based on the video categories and the trending metrics.

## Project Goals
1. Data Ingestion — Build a mechanism to ingest data from different sources
2. ETL System — We are getting data in raw format, transforming this data into the proper format
3. Data lake — We will be getting data from multiple sources so we need centralized repo to store them
4. Scalability — As the size of our data increases, we need to make sure our system scales with it
5. Cloud — We can’t process vast amounts of data on our local computer so we need to use the cloud, in this case, we will use AWS
6. Reporting — Build a dashboard to get answers to the question we asked earlier

## Services Used
1. AWS IAM: Identity and access management which enables us to manage access to AWS services and resources securely.
2. Amazon S3: Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance.
3. AWS Glue: A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
4. AWS Lambda: Lambda is a computing service that allows programmers to run code without creating or managing servers.
5. AWS Athena: Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.
6. QuickSight: Amazon QuickSight is a scalable, serverless, embeddable, machine learning-powered business intelligence (BI) service built for the cloud.

## Dataset Used
This Kaggle dataset contains statistics (CSV files) on daily popular YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.

https://www.kaggle.com/datasets/datasnaek/youtube-new

## Architecture Diagram
<img src="architecture.jpeg">

## Note
I have attached the work done in the AWS Console in aws_console_videos directory where I recorded the S3 buckets, lambda functions, glue crawlers and jobs etc created.

**aws_cli_s3_shell_commands.sh** contains AWS CLI commands to upload data into AWS S3 bucket.
**lambda_function.py** is used to create trigger function in AWS Lambda.
**pyspark.py** is used to create ETL job in AWS Glue Job.