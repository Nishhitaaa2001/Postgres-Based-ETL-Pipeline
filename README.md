Postgres-Based-ETL-Pipeline
A robust ETL pipeline for processing and analyzing music streaming data using PostgreSQL as the backend database. This project is designed to extract, transform, and load song and user activity data from JSON files into a structured database for analytics and reporting.

Table of Contents
Project Overview

Architecture

Data Sources

Pipeline Workflow

How to Run

File Structure

Dependencies

License

Project Overview
This project enables the creation of a scalable data pipeline for Sparkify, a music streaming app. The pipeline processes raw JSON data (song metadata and user activity logs), transforms it, and loads it into a PostgreSQL database for efficient querying and analysis.

Architecture
Database: PostgreSQL for storing structured data.

ETL Pipeline: Python scripts for data extraction, transformation, and loading.

Schema: Star schema with fact and dimension tables for analytics.

Data Sources
Song Data: JSON files containing song metadata (title, artist, duration, year, etc.).

User Activity Logs: JSON files recording user song plays, timestamps, and session details.

Pipeline Workflow
Extract: Read JSON files for songs and user activity.

Transform: Clean, filter, and enrich data (e.g., timestamp parsing, song/artist matching).

Load: Insert processed data into PostgreSQL tables.

How to Run
Clone the repository.

Install dependencies (see below).

Run the following scripts in order:

bash
python create_tables.py
python etl.py
The database will be populated with processed data.

File Structure
text
Postgres-Based-ETL-Pipeline/
├── create_tables.py      # Creates and manages database tables
├── etl.py              # ETL pipeline script
├── sql_queries.py      # SQL queries for table creation and data insertion
├── test.ipynb          # Jupyter notebook for testing and validation
└── README.md           # This file
Dependencies
Python 3.x

psycopg2

pandas

numpy

Install dependencies using:

bash
pip install psycopg2 pandas numpy
License
This project is licensed under the MIT License. See the LICENSE file for details.
