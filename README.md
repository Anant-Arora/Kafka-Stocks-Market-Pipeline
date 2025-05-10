# 📈 Real-Time Stock Tracking using Kafka and GCP

## 🚀 Project Overview

This project implements a real-time data pipeline that simulates a stock market feed using Apache Kafka and Google Cloud Platform. At its core, the system reads a CSV file containing stock data and streams it into a Kafka topic using a Kafka Producer written in Python. The Kafka Consumer, also built in Python, listens to this topic and pushes each record into a Google Cloud Storage (GCS) bucket in .json format.

This architecture mimics real-time stock data ingestion — as prices change, the system captures and stores every tick. The use of Kafka’s distributed messaging system makes the pipeline highly scalable and fault-tolerant. The cloud bucket acts as a persistent, cost-effective storage solution that can be used for analytics, dashboarding, or feeding downstream systems.

This structured, modular pipeline bridges data generation and storage efficiently, showcasing how Kafka can be paired with GCP to power real-time analytics pipelines for stock data.

> 📍 CSV files are initially loaded in a Jupyter Notebook, and then sent through Kafka topics using custom **producers and consumers**.

---

## 🏗️ System Architecture
(![ChatGPT Image May 10, 2025, 03_25_19 PM](https://github.com/user-attachments/assets/ebeb8768-2883-45cf-bc54-ef4d76746b77)
)

### Components:
- **Apache Kafka** on GCP VM: Handles streaming of stock data.
- **Producer Script (Python)**: Reads stock data from CSV and sends to Kafka topic.
- **Consumer Script (Python)**: Consumes stock data and pushes it to Google Cloud Storage (GCS).
- **Google Cloud Storage Bucket**: Stores the structured data in `.json` format for further analysis or dashboarding.
- **Jupyter Notebook**: Used for data preprocessing and testing pipeline logic.
![ChatGPT Image May 10, 2025, 03_25_19 PM](https://github.com/user-attachments/assets/bff1f17a-72fa-4fd5-8174-14cb9641708d)
![ChatGPT Image May 10, 2025, 03_25_19 PM](https://github.com/user-attachments/assets/d917f655-b319-4d81-a7b5-e62638f69181)

---

## 🔧 Tech Stack Used

| Component         | Tool/Service                    |
|------------------|---------------------------------|
| Data Source       | CSV (Stock Data)               |
| Stream Processor  | Apache Kafka                   |
| Infrastructure    | Google Cloud VM (Ubuntu)       |
| Storage           | GCP Storage Bucket (GCS)       |
| Notebook IDE      | Jupyter (Local/Cloud)          |
| Language          | Python                         |

---

##  How It Works

1. ✅ Load CSV in **Jupyter Notebook**.
2. ✅ Start **Producer** script to read the CSV and stream records to Kafka.
3. ✅ Kafka runs on a **GCP VM (Kafkastocks)** instance and hosts the broker and topic (`demo_test`).
4. ✅ The **Consumer** reads from the Kafka topic and writes each record into a **Google Cloud Storage bucket** (`kafka_stocks_bucket`) as a `.json` file.

---

## Why GCP Buckets Matter in Stock Analytics

- **Durable Storage**: Buckets serve as a reliable, scalable, and cost-effective place to store historical and real-time stock data.
- **Integration with BigQuery & AI**: Easy to plug in analytics or ML models.
- **Data Lake Foundation**: Ideal for setting up a stock analytics platform with dashboards and queries.
- **Safe Decoupling**: GCS decouples storage from processing, ensuring that consumers don’t need to be always live.
  
---
##  Challenges Faced
- Kafka not recognizing brokers (NoBrokersAvailable).
- GCP IAM permission configurations.
- Bucket access and role management.
- Authentication with gcloud auth login & CLI.
- Kafka setup and port management on VM.

---
##  Output:

##  Next Steps

- [ ] Connect to **BigQuery** for real-time analysis.
- [ ] Implement **Alerting System** for sudden stock movement.
- [ ] Integrate with **Power BI** or **Tableau** dashboards.

---

##  Contributions & License

Pull requests welcome! For major changes, please open an issue first to discuss what you would like to change.

---

##  Final Thoughts

This project demonstrates how modern data engineering tools can be applied to build fast, scalable, and cloud-native stock monitoring systems.

---

