# Change Data Capture (CDC) Realtime Streaming with Postgres, Debezium, Kafka

This project demonstrates an end-to-end implementation of Change Data Capture (CDC) for real-time data synchronization and streaming. The stack includes PostgreSQL, Debezium, Apache Kafka, Apache Spark, and Slack.

## Overview

In the dynamic world of data processing and analytics, CDC stands out as a critical technology for real-time data synchronization and streaming. This project integrates CDC with a stack comprising PostgreSQL, Debezium, Kafka to create a comprehensive ecosystem for handling, processing, and monitoring data changes.

## Technologies Used

- **PostgreSQL:** Open-source relational database known for reliability and SQL standards compliance.
- **Debezium:** CDC platform efficiently captures row-level changes in databases like PostgreSQL.
- **Apache Kafka:** High-throughput distributed messaging system serving as the backbone for streaming data changes.


## Setup

### Docker Containers

Use the provided `docker-compose.yml` file to set up Docker containers for Zookeeper, Kafka, Control Center, Debezium, Debezium UI, and PostgreSQL.

docker-compose up -d

Debezium Connector
Create a new connector using the provided script or the Debezium UI to capture changes in PostgreSQL.

bash
Copy code
curl -H 'Content-Type: application/json' localhost:8083/connectors --data ' 
{
  "name": "postgres-connector",  
  "config": {
    "connector.class": "io.debezium.connector.postgresql.PostgresConnector", 
    "plugin.name": "pgoutput",
    // ... other configuration parameters
  }
}'
Data Ingestion
Generate simulated transactions and insert them into the PostgreSQL database.

bash
Copy code
python data_ingestion_script.py
Usage
View changes in PostgreSQL.
Visualize changes on Kafka through the Control Center UI (http://localhost:9021).
Explore advanced features like capturing users and modification time using triggers.
Use streaming technologies like Apache Spark for further data processing.
Considerations and Best Practices
Be mindful of performance impact with triggers on high-write tables.
Ensure audit logs comply with privacy laws and company policies.
Define a clear data retention policy for audit logs.
