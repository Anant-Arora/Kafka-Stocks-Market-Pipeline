# 📈 Real-Time Stock Tracking using Kafka and GCP

## 🚀 Project Overview

This project demonstrates a **real-time stock analytics pipeline** using **Apache Kafka**, **Google Cloud Platform (GCP)**, and **Python**. It ingests, processes, and stores live stock data using a producer-consumer model — designed for high-performance and scalability.

> 📍 CSV files are initially loaded in a Jupyter Notebook, and then sent through Kafka topics using custom **producers and consumers**.

---

## 🏗️ System Architecture

![Architecture Diagram](path_to_your_architecture_image.png)
<!-- Replace with your architecture image file or GDrive link -->

### Components:
- **Apache Kafka** on GCP VM: Handles streaming of stock data.
- **Producer Script (Python)**: Reads stock data from CSV and sends to Kafka topic.
- **Consumer Script (Python)**: Consumes stock data and pushes it to Google Cloud Storage (GCS).
- **Google Cloud Storage Bucket**: Stores the structured data in `.json` format for further analysis or dashboarding.
- **Jupyter Notebook**: Used for data preprocessing and testing pipeline logic.

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

##  Screenshots / Output Samples

###  Kafka Streaming Output:
![Streaming Logs](path_to_streaming_screenshot.png)

###  Files in GCP Bucket:
![GCP Bucket Structure](path_to_gcp_bucket_screenshot.png)

---

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

