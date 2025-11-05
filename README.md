 🎧 Postgres-Based ETL Pipeline

A robust ETL pipeline for processing and analyzing **music streaming data** using **PostgreSQL** as the backend data warehouse.  
This project extracts, transforms, and loads song metadata and user activity logs from JSON files into a structured **star schema** for analytics and reporting.

---

## 📌 Table of Contents
- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Data Sources](#data-sources)
- [Schema Design](#schema-design)
- [Pipeline Workflow](#pipeline-workflow)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [License](#license)

---

## 📖 Project Overview
This project builds a scalable ETL pipeline for a sample music streaming platform (**Sparkify**).  
It processes song metadata and user activity logs stored as JSON files and loads them into PostgreSQL for faster querying, reporting, and insights into user listening behavior.

---

## 🏗️ Architecture

| Component       | Technology |
|----------------|------------|
| Database       | PostgreSQL |
| ETL Processing | Python     |
| Data Format    | JSON       |

ETL Pipeline:
Extract → Transform → Load → Query → Analytics

yaml
Copy code

---

## 📂 Data Sources
| Dataset | Description |
|--------|-------------|
| **Song Data** | Contains song metadata (title, artist, duration, year) |
| **User Logs** | App events recording song plays, user activity & timestamps |

---

## ⭐ Schema Design (Star Schema)

**Fact Table**
- `songplays` — records for each user song stream event

**Dimension Tables**
- `users` — user attributes (level, gender, name, etc.)
- `songs` — song details (title, duration, year)
- `artists` — artist metadata (name, location)
- `time` — timestamp breakdown (hour, day, month, year, weekday)

This structure supports **analytical queries and BI dashboards**.

---

## 🔄 Pipeline Workflow
| Phase | Details |
|------|---------|
| **Extract** | Load raw JSON logs & metadata |
| **Transform** | Clean + parse timestamps + link songs & artists |
| **Load** | Insert processed data into normalized tables in PostgreSQL |

Executed using Python scripts + SQL insert queries.

---

## ▶️ How to Run

### 1️⃣ Clone the repository
```sh
git clone <your-repo-url>
cd Postgres-Based-ETL-Pipeline
2️⃣ Install required libraries
sh
Copy code
pip install -r requirements.txt
—or manually:

sh
Copy code
pip install psycopg2 pandas numpy
3️⃣ Setup database tables
sh
Copy code
python create_tables.py
4️⃣ Run ETL Pipeline
sh
Copy code
python etl.py
✅ PostgreSQL database gets populated with analytics-ready tables

📁 Project Structure
graphql
Copy code
Postgres-Based-ETL-Pipeline/
├── create_tables.py       # Creates & resets database schema
├── etl.py                 # ETL workflow execution script
├── sql_queries.py         # SQL for create/insert operations
├── test.ipynb             # Notebook for validation/queries
└── README.md              # Documentation
🧩 Dependencies
Python 3.x

PostgreSQL

psycopg2

pandas

numpy

📜 License
Licensed under the MIT License.
See the LICENSE file for more details.

✨ Author
Nishita Rajak
Data Engineering & Analytics
🔗 Feel free to ⭐ this repository if you find it useful!
