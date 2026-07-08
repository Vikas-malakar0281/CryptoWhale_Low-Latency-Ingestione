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
