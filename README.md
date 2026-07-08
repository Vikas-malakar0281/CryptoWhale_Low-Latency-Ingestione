# Crypto-pipline-project_1
This repository is Part 1 of a three-part end-to-end data engineering project designed to demonstrate my ability to build, deploy, and operate modern streaming data pipelines.  
  
This part focuses on building the same streaming data pipeline in two environments.   
- **The first implementation is a self-managed:**  
Docker containerized streaming cluster built from scratch using Apache Kafka, Apache Spark, and Python.  
- **The second implementation recreates the pipeline using AWS managed services:**  
 Amazon Kinesis, AWS Glue, Amazon S3, Apache Iceberg, Amazon Athena, and Terraform for infrastructure provisioning.
  
Together, these implementations demonstrate my ability to design and build both self-managed and cloud-native streaming data pipelines, covering real-time data ingestion, distributed stream processing, data lake storage, and analytics while following production-inspired data engineering practices.
  
The overall three-part project is designed to showcase a complete data engineering journey, progressing from local infrastructure to cloud-native architectures and production-ready data lake solutions.

## Why Two Different Environments?

Modern data engineering solutions are built in a variety of environments depending on an organization's size, budget, operational requirements, and cloud strategy. To reflect this reality, this project implements the same streaming pipeline in two different environments.

### Self-Managed (Local) Environment

The Docker-based implementation demonstrates my understanding of the underlying technologies that power streaming systems. Rather than relying on managed cloud services, I configured and orchestrated the infrastructure myself, including Kafka, Zookeeper, Spark Master, Spark Worker, and the streaming application.

This environment showcases my ability to:

* Build and manage distributed services using Docker Compose.
* Configure and troubleshoot Apache Kafka and Apache Spark.
* Develop real-time streaming applications with PySpark.
* Understand how individual components interact within a streaming architecture.

### Cloud-Native (AWS) Environment

The AWS implementation demonstrates how the same business problem can be solved using managed cloud services. Instead of managing infrastructure, the focus shifts to scalability, reliability, automation, and operational efficiency.

This environment showcases my ability to:

* Design cloud-native data pipelines.
* Use managed AWS analytics services such as Amazon Kinesis, AWS Glue, Amazon S3, Apache Iceberg, and Amazon Athena.
* Provision infrastructure using Terraform.
* Apply modern data lake and Lakehouse concepts following production-inspired practices.

### Why Build Both?

Building both implementations demonstrates that I understand the concepts behind distributed data engineering rather than simply knowing how to use a specific cloud service. It also highlights my ability to adapt the same architecture to different deployment models, from self-managed infrastructure for development and learning to managed cloud services commonly used in production environments.
## Frequently Asked Questions

### Why did I build this project?

The objective of this project was to gain hands-on experience with modern data engineering technologies while demonstrating how the same streaming data pipeline can be implemented in both a self-managed environment and a cloud-native environment.

Rather than focusing on a single technology, this project showcases the complete lifecycle of a real-time streaming pipeline—from data ingestion and processing to storage and querying.

---

### What problem does this project solve?

Modern organizations continuously generate streaming data that must be processed efficiently for analytics and decision-making.

This project demonstrates how to:

- Ingest real-time cryptocurrency market data.
- Process streaming events with distributed computing.
- Store optimized analytical datasets.
- Build a scalable data lake architecture.
- Query processed data efficiently for analysis.

The architecture can be adapted to many real-world streaming use cases beyond cryptocurrency.

---

### Why choose cryptocurrency streaming data?

Cryptocurrency exchanges generate high-volume, real-time public market data, making them an excellent dataset for learning streaming architectures.

It provides:

- Continuous event streams
- High-frequency updates
- Semi-structured JSON data
- Real-world streaming workloads
- No authentication required for public market data

This allows the project to focus on engineering challenges rather than data collection.

---

### Why implement the pipeline in two different environments?

The project demonstrates two approaches commonly found in industry.

**Local (Self-Managed)**

- Learn how distributed systems work internally.
- Configure and manage Kafka and Spark.
- Understand infrastructure and networking.

**Cloud (AWS)**

- Learn how organizations build scalable managed pipelines.
- Reduce operational overhead.
- Demonstrate cloud-native data engineering practices.

---

### What technologies does this project demonstrate?

This project demonstrates practical experience with:

- Docker & Docker Compose
- Apache Kafka
- Apache Spark Structured Streaming
- PySpark
- Python
- Amazon Kinesis
- AWS Glue
- Amazon S3
- Apache Iceberg
- Amazon Athena
- Terraform

---

### What skills does this project showcase?

The project demonstrates experience with:

- Real-time data ingestion
- Distributed stream processing
- Infrastructure as Code (Terraform)
- Data lake architecture
- Lakehouse concepts
- Cloud-native analytics
- Containerization
- Data modeling
- Schema evolution
- Production-inspired pipeline design

---

### Is this intended to be a production-ready system?

No.

The primary objective is educational and portfolio-driven while following production-inspired design principles.

Where appropriate, the project incorporates concepts commonly used in production systems, such as:

- Infrastructure as Code
- ACID table formats
- Schema evolution
- Distributed processing
- Cloud-native services
- Modular architecture

The goal is to demonstrate an understanding of modern data engineering practices rather than replicate a complete enterprise production platform.

---

### Who is this project intended for?

This project is intended for:

- Recruiters
- Hiring managers
- Data Engineers
- Cloud Engineers
- Students learning data engineering
- Anyone interested in modern streaming data architectures

## Project Structure

```text
crypto-pipeline-project-1/
│
├── src/                               # Application source code
│   ├── producer.py                    # Binance WebSocket producer
│   ├── spark_streaming.py             # Spark Structured Streaming application
│   └── test.py                        # Testing and experimentation scripts
│
├── terraform/                         # Infrastructure as Code (AWS)
│   ├── main.tf                        # Main infrastructure resources
│   ├── variables.tf                   # Terraform variables
│   ├── outputs.tf                     # Output values
│   ├── iam.tf                         # IAM roles and policies
│   └── glue_catalog.tf                # AWS Glue Data Catalog resources
│
├── docker-compose.yml                 # Local streaming cluster
├── Dockerfile                         # Producer container image
├── Dockerfile.spark                   # Spark container image
├── compaction_parquet.py              # Parquet compaction utility
├── setup_local.bat                    # Windows setup script
├── requirement.txt                    # Python dependencies
├── .env                               # Environment variables (local)
├── .gitignore
├── README.md
└── LICENSE
```

### Folder Overview

| Component                 | Description                                                                                                                         |
| ------------------------- | -----------------------------------------------------------------------------------------------------------------------------------|
| **src/**                  | Contains the Python applications responsible for data ingestion, stream processing, and testing.                                   |
| **terraform/**            | Infrastructure as Code used to provision the complete AWS environment using Terraform.                                             |
| **docker-compose.yml**    | Defines the self-managed Docker streaming cluster, including Kafka, Zookeeper, Spark Master, Spark Worker, Producer, and Spark Job.|
| **Dockerfile**            | Builds the producer container image.                                                                                               |
| **Dockerfile.spark**      | Builds the Spark runtime used by the master, worker, and streaming job.                                                            |
| **compaction_parquet.py** | Utility script for compacting small Parquet files generated by streaming workloads.                                                |
| **setup_local.bat**       | Automates local environment setup on Windows.                                                                                      |
| **requirement.txt**       | Python package dependencies required by the project.                                                                               |



