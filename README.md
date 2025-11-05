# Postgres-Based ETL Pipeline

This project demonstrates a robust ETL pipeline designed to process and analyze music streaming data using PostgreSQL as the data warehouse. The pipeline extracts raw JSON data related to songs and user events, transforms it into clean relational tables, and loads it into a star-schema optimized database for analytics and reporting.

## Project Overview
This project simulates a real-world scenario for Sparkify, a fictional music streaming application. The goal is to convert semi-structured JSON data into a well-structured data model so that analysts can efficiently query user listening behavior and streaming trends.

## Architecture
- Data Source: JSON files (song metadata and user activity logs)
- ETL Processing: Python scripts to extract, transform, and load data
- Data Storage: PostgreSQL relational database
- Output: Star schema supporting analytical workloads

## Data Schema
The database follows a star schema composed of:

**Fact Table**
- `songplays`: Records of user song playback interactions

**Dimension Tables**
- `users`: User profile and subscription information  
- `songs`: Song metadata including title, duration, and year  
- `artists`: Artist details and geographical information  
- `time`: Timestamp information broken into analytical fields (hour, day, week, month, year)  

This schema improves performance for BI queries and reporting dashboards.

## ETL Workflow
1. Extract raw JSON data from song and log files
2. Transform data by cleaning, parsing timestamps, and linking songs with artists
3. Load processed data into PostgreSQL using defined SQL insert statements

## How to Run the Project
1. Clone this repository  
2. Install dependencies (psycopg2, pandas, and numpy)
3. Run `create_tables.py` to create/reset database tables
4. Execute `etl.py` to load transformed data into PostgreSQL

After successful execution, structured and analytics-ready tables will be available inside the PostgreSQL database.

## Project Structure
Postgres-Based-ETL-Pipeline/
├── create_tables.py      # Creates and manages database tables
├── etl.py              # ETL pipeline script
├── sql_queries.py      # SQL queries for table creation and data insertion
├── test.ipynb          # Jupyter notebook for testing and validation
└── README.md           # This file

## Dependencies
- Python 3.x
- PostgreSQL
- psycopg2
- pandas
- numpy
