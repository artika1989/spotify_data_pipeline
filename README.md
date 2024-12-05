# spotify End-to-End Data Engineering project

## Description
In this project we build ETL pipeline using Spotify api on AWS. The main objective is to fetch data from spotify API , transform it and load in AWS data store.

## Technology Used
Programming Language - Python
Amazon S3 bucket
Amazon IAM role
Amazon Lambda
Amazon Glue
Amazon Athena

## Architecture
![Architecture](<Screenshot 2024-12-04 at 5.13.45 PM.png>)

## Python Packages
Pip3 install Pandas
Pip3 install Numpy
Pip3 instal Apache Airflow

# Overview 
## Step 1
First to create connection between spotify to fetch data. It is required to create app on developer mode. from where client Id and Client secret created which is utilized to make an api call.

## Step 2
To work on Apache airflow following https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html. Where you need to download docker-compose.yaml to host Airflow webserver.

## Step 3
Once Apache airflow is launched it is the time that is needed to write script for creating dag. First we create Dag to fetch spotify data. Later it is tranformed to create artists, albums, tracks list which further store into S3 bucket.

## Step 4
Utilizing AWS glue ETl job which crawl over processed data store into S3 bucket. Crawler store the metadata and schema of processed data in glue database.

## Step 5
Later creating AThena database where it is connected to glue database to query agaist table to fetch relevant data based on the requirement.



