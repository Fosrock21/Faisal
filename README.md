# TRACKER
<p>
	<img src="https://img.shields.io/badge/YAML-CB171E.svg?style=default&logo=YAML&logoColor=white" alt="YAML">
	<img src="https://img.shields.io/badge/Go-00ADD8.svg?style=default&logo=Go&logoColor=white" alt="Go">
	<img src="https://img.shields.io/badge/JSON-000000.svg?style=default&logo=JSON&logoColor=white" alt="JSON">
</p>

## Overview


## Diagrams
**End-to-End Log Ingestion & Agent Alert Pipeline**

![Diagram showing the workflow of log ingestion and agent monitoring](https://github.com/user-attachments/assets/26c8b7a6-0d48-4609-bdfd-4ba045f79886)

## Running Locally
**Once you have cloned the repository, go to the root of this project.**

**Install the dependencies:**
```bash
go mod tidy
```
**Run the Producer:**

To execute the producer, you need to run the Docker Compose file located inside the `.dev` folder. Use the following command:
```bash
make docker-up
```

**Install Azure Functions Core Tools: [here](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=windows%2Cisolated-process%2Cnode-v4%2Cpython-v2%2Chttp-trigger%2Ccontainer-apps&pivots=programming-language-csharp#install-the-azure-functions-core-tools)**


**Execute this command**

```bash
func start --custom --port 8080
```

**Test by running this command in a seperate terminal**
```bash
curl http://localhost:8080/swagger/index.html
```

## Environment Variables

| Variable                   | Description                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------|
| `WEBSITE_INSTANCE_ID`      | Unique identifier for the website instance (leave blank if not applicable).                   |
| `FUNCTIONS_WORKER_RUNTIME` | Specifies the runtime environment for functions (set to "Custom" for custom handlers).              |
| `FUNCTIONS_CUSTOMHANDLER_PORT` | The port used by the custom handler.                     |
| `IS_TESTING`               | Specifies if the app is in testing mode (`true` or `false`).                                   |
| `DB_HOST`                  | Database server hostname (e.g., `localhost` for local development).                           |
| `DB_PORT`                  | Port on which the database server is running (e.g., `5432` for PostgreSQL).                   |
| `DB_NAME`                  | Name of the database to connect to (e.g., `tracker`).                                         |
| `DB_USER`                  | Username for accessing the database (e.g., `postgres`).                                       |
| `DB_PASSWORD`              | Password for the database user.                                                               |
| `DB_SSL`                   | SSL mode for the database connection (e.g., `disable` for local development).                 |
| `ENVIRONMENT`              | Defines the environment the app is running in (e.g., `local`, `production`).                                  |
| `SITE_NAME`                | The hostname and port of the site (e.g., `localhost:8080`).                                       |
| `CATALOG_ENDPOINT`         | URL for the catalog service endpoint (e.g., `http://localhost:8080`).                         |
| `OPENSEARCH_ADDRESS`       | URL for the OpenSearch server (e.g., `http://localhost:9200`).                                |
| `KAFKA_ENDPOINT`           | The endpoint for connecting to Kafka (e.g., `localhost:9092`).                                          |
| `KAFKA_TOPIC`              | The Kafka topic that the application uses for message ingestion (e.g., `tracker-ingestor`).                            |
| `KAFKA_CONSUMER_GROUP`     | Kafka consumer group identifier (e.g., `tracker-consumer-group`).                             |
| `ISSUER_URL`               | URL for the issuer in identity management (e.g., `http://test.com`).                          |
| `DISCOVERY_BASE_URL`       | Base URL for discovery services (e.g., `http://test.com`).                                    |
| `APPLICATION_ID`           | Application ID for authentication purposes.                                                   |
| `APPLICATION_SECRET`       | Secret key associated with the application for authentication.                                |
| `B2C_TENANT_ID`            | Tenant ID for B2C (Business to Consumer) authentication.                                      |
