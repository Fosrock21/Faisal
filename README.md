# TRACKER PRODUCER
<p>
	<img src="https://img.shields.io/badge/YAML-CB171E.svg?style=default&logo=YAML&logoColor=white" alt="YAML">
	<img src="https://img.shields.io/badge/Go-00ADD8.svg?style=default&logo=Go&logoColor=white" alt="Go">
	<img src="https://img.shields.io/badge/JSON-000000.svg?style=default&logo=JSON&logoColor=white" alt="JSON">
</p>

## Overview
This project is responsible for processing and ingesting logs from various sources into OpenSearch. The "Tracker Producer" receives logs from an external application, batches them, and publishes messages to a queue for asynchronous processing. These messages are then consumed by the "Tracker Consumer," which reads, processes, and stores them in a database. Additionally, the "Tracker Webhook" monitors for offline agents, triggering alerts and updating OpenSearch with this information. The system is designed to ensure all logs and agent statuses are efficiently ingested and monitored within the platform.

## Diagrams
**End-to-End Log Ingestion & Agent Alert Pipeline**

![Diagram showing the workflow of log ingestion and agent monitoring](https://github.com/user-attachments/assets/26c8b7a6-0d48-4609-bdfd-4ba045f79886)

## Running Locally
**Clone the tracker-producer repository:**
```bash
git clone git@ssh.dev.azure.com:v3/ZestSecurity/backend/tracker-producer
```

**Change to the project directory:**
```bash
cd tracker-producer/cmd
```

**Install the dependencies:**
```bash
go mod download
```

**Run the Producer:**

To execute the producer, you need to run the Docker Compose file located inside the `.dev` folder. Use the following command:
```bash
make docker-up
```

## Environment Variables

| Variable                        | Description                                                                                       |
|---------------------------------|---------------------------------------------------------------------------------------------------|
| `WEBSITE_INSTANCE_ID`           | Unique identifier for the website instance (leave blank if not applicable).                       |
| `FUNCTIONS_WORKER_RUNTIME`      | Specifies the runtime environment for functions (set to "Custom" for custom handlers).            |
| `FUNCTIONS_CUSTOMHANDLER_PORT`  | The port used by the custom handler.                                 |
| `IS_TESTING`                    | Specifies if the app is in testing mode (`true` or `false`).                                      |
| `ENVIRONMENT`                   | Defines the environment the app is running in (e.g., `local`, `production`).                     |
| `SITE_NAME`                     | The hostname and port of the site (e.g., `localhost:8080`).                                      |
| `KAFKA_ENDPOINT`                | The endpoint for connecting to Kafka (e.g., `localhost:9092`).                                   |
| `KAFKA_TOPIC`                   | The Kafka topic that the application uses for message ingestion (e.g., `tracker-ingestor`).       |
