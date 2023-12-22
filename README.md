# Change Data Capture (CDC) Realtime Streaming with Postgres, Debezium, Kafka, Apache Spark, and Slack

This project demonstrates an end-to-end implementation of Change Data Capture (CDC) for real-time data synchronization and streaming. The stack includes PostgreSQL, Debezium, Apache Kafka, Apache Spark, and Slack.

## Overview

In the dynamic world of data processing and analytics, CDC stands out as a critical technology for real-time data synchronization and streaming. This project integrates CDC with a stack comprising PostgreSQL, Debezium, Kafka, Spark, and Slack to create a comprehensive ecosystem for handling, processing, and monitoring data changes.

## Technologies Used

- **PostgreSQL:** Open-source relational database known for reliability and SQL standards compliance.
- **Debezium:** CDC platform efficiently captures row-level changes in databases like PostgreSQL.
- **Apache Kafka:** High-throughput distributed messaging system serving as the backbone for streaming data changes.
- **Apache Spark:** Enables advanced data processing, analytics, machine learning, and real-time data transformations.
- **Slack:** Integrated for real-time notifications and alerts.

## Setup

### Docker Containers

Use the provided `docker-compose.yml` file to set up Docker containers for Zookeeper, Kafka, Control Center, Debezium, Debezium UI, and PostgreSQL.

```bash
docker-compose up -d
