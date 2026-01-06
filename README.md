# 🚀 Retail Real-Time Data Pipeline

## 📌 Overview
This repository contains an **end-to-end real-time data engineering pipeline** designed for retail sales analytics.  
The project demonstrates how streaming sales data can be ingested, processed, stored, and exposed for analytical and BI use cases.

This project is built to reflect **real-world Data Engineering workflows**, not just dashboarding.

---

## 🧠 Architecture
Data Producer
↓
Apache Kafka
↓
Apache Spark (Structured Streaming)
↓
PostgreSQL (Analytical Storage)
↓
Metabase (BI & Analytics)

---

## 🧱 Tech Stack
- Python
- Apache Kafka
- Apache Spark (Structured Streaming)
- PostgreSQL
- Metabase
- Docker & Docker Compose

---

## 📂 Project Structure
retail-data-pipeline/
├── producer/
│ └── sales_producer.py
├── spark-jobs/
│ └── sales_stream_processor.py
├── sql/
│ ├── schema.sql
│ └── indexes.sql
├── docker-compose.yml
├── requirements.txt
└── README.md

---

## 🔄 Data Flow
1. **Data Ingestion**  
   Simulated retail sales events are produced and published to Kafka topics.

2. **Stream Processing**  
   Spark Structured Streaming consumes data from Kafka and applies:
   - Schema validation
   - Data cleaning (null handling, deduplication)
   - Aggregations (revenue, daily sales)

3. **Data Storage**  
   Processed data is stored in PostgreSQL using an analytical-friendly schema.

4. **Analytics Layer**  
   Metabase connects to PostgreSQL to provide dashboards and business insights.

---

## 🗄️ Data Model
### Fact Table
- `fact_sales`
  - sale_id
  - product_id
  - quantity
  - total_price
  - sale_timestamp

### Dimension Tables
- `dim_product`
- `dim_date`

The model follows **star schema principles** for efficient analytical queries.

---

## ▶️ How to Run
```bash
docker-compose up -d
Steps:

Start Kafka, Spark, PostgreSQL services

Run the Kafka producer

Execute the Spark streaming job

Access Metabase via browser

📊 Sample Analytics

Total revenue per day

Top-selling products

Real-time transaction volume

Sales trends over time

🔍 Key Concepts Demonstrated

Real-time data ingestion

Stream processing with Spark

Data cleaning & validation

Analytical data modeling

Scalable data pipeline design

BI-ready data delivery

🎯 Why This Project

This project showcases Data Engineering fundamentals commonly required in production environments and bridges the gap between raw streaming data and business intelligence systems.

👤 Author

Mohsen Moghadam
Data Engineer | BI Lead | Backend Developer
📧 mohsenmoghadam277@gmail.com

🔗 GitHub: https://github.com/mohsenmoghadam277
