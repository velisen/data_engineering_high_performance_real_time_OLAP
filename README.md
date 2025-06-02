
# High-Performance Real-Time OLAP Data Engineering

This project demonstrates a high-performance, real-time Online Analytical Processing (OLAP) data pipeline. It integrates Apache Kafka, Apache Druid, and Apache Superset for streaming data ingestion, storage, and visualization with low latency.

---

## 🚀 Features

- **Real-Time Streaming with Kafka** – Efficient and scalable ingestion of real-time data.
- **Fast OLAP Analytics with Apache Druid** – Low-latency analytical queries on large-scale datasets.
- **Interactive Dashboards via Superset** – Visualize insights instantly with a modern BI interface.
- **Containerized Microservices** – Easily deployable with Docker Compose.
- **Modular & Scalable Architecture** – Easy to adapt and expand for different use cases.

---

## 🧱 Architecture Overview

```
                ┌──────────┐
                │ Data Gen │
                └────┬─────┘
                     ▼
                ┌──────────┐
                │  Kafka   │  ← Real-time ingestion
                └────┬─────┘
                     ▼
                ┌──────────┐
                │  Druid   │  ← Fast OLAP engine
                └────┬─────┘
                     ▼
                ┌────────────┐
                │ Superset   │  ← Dashboards and SQL queries
                └────────────┘
```

---

## 🛠️ Getting Started

### Prerequisites

- [Docker]
- [Docker Compose]

---

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/velisen/data_engineering_high_performance_real_time_OLAP.git
   cd data_engineering_high_performance_real_time_OLAP
   ```

2. **Configure Environment Variables** (Optional):

   Modify `.env` files in the `environment/` directory for custom settings.

3. **Run the Entire Stack**:

   ```bash
   docker-compose up --build
   ```

   This command will build the Docker images and start all the services defined in the `docker-compose.yml` file.

---

## 📦 Components

### ✅ Apache Kafka

- **Purpose**: Acts as a real-time message broker.
- **Usage**: Stream events (e.g., JSON) from producers like data generators or external APIs.

### ✅ Apache Druid

- **Purpose**: High-performance OLAP datastore designed for real-time and batch ingestion.
- **Features**: Time-based partitioning, columnar storage, roll-ups, and fast aggregation.

### ✅ Apache Superset

- **Purpose**: Open-source BI platform for exploring and visualizing Druid data.
- **Usage**: Connect Superset to Druid to create dashboards and ad-hoc queries.

---

## 📂 Project Structure

```
├── Dockerfile               # Defines the Docker image for the application
├── docker-compose.yml       # Orchestrates multi-container deployment
├── environment/             # Contains environment-specific configurations
│   └── .env                 # Environment variables
├── main.py                  # Entry point for the application
├── .gitignore               # Specifies files to ignore in version control
```

---

## 📈 Usage

- **Data Ingestion**: Feed your real-time data into the ingestion endpoint or service.
- **Querying Data**: Use the provided API endpoints to perform analytical queries on the processed data.
- **Monitoring**: Monitor the performance and health of the pipeline through logs and metrics (if implemented).

---

## 🧪 Testing

to send data to kafka:
run main.py

<img src="superset.jpg">
