# CATALOG
<p>
	<img src="https://img.shields.io/badge/GNU%20Bash-4EAA25.svg?style=default&logo=GNU-Bash&logoColor=white" alt="GNU%20Bash">
	<img src="https://img.shields.io/badge/YAML-CB171E.svg?style=default&logo=YAML&logoColor=white" alt="YAML">
	<img src="https://img.shields.io/badge/PostgreSQL-4479A1.svg?style=default&logo=PostgreSQL&logoColor=white" alt="PostgreSQL">
	<img src="https://img.shields.io/badge/Files-4285F4.svg?style=default&logo=Files&logoColor=white" alt="Files">
	<img src="https://img.shields.io/badge/Go-00ADD8.svg?style=default&logo=Go&logoColor=white" alt="Go">
	<img src="https://img.shields.io/badge/NOW-001211.svg?style=default&logo=NOW&logoColor=white" alt="NOW">
	<img src="https://img.shields.io/badge/Wire-000000.svg?style=default&logo=Wire&logoColor=white" alt="Wire">
	<img src="https://img.shields.io/badge/JSON-000000.svg?style=default&logo=JSON&logoColor=white" alt="JSON">
</p>

## Overview
The Catalog software project is a robust and versatile API service that facilitates seamless interactions within an architecture. Leveraging Azure deployment resources for catalog functions, storage, and PostgreSQL server setup, the project dynamically names resources based on parameters and establishes dependencies for environment-specific Azure Function App deployment. The projects core functionalities include handling database migrations, automated application builds, deployments, linting, testing, and cleaning operations. With a well-structured codebase managing essential functions and configurations, the Catalog project ensures effective communication and operational efficiency within the system. The projects value proposition lies in its ability to streamline the development and deployment processes while enhancing overall functionality and stability through carefully managed dependencies and Azure integration.


## Diagrams
**End-to-End Log Ingestion & Agent Alert Pipeline**

![Diagram showing the workflow of log ingestion and agent monitoring](https://github.com/user-attachments/assets/26c8b7a6-0d48-4609-bdfd-4ba045f79886)

## Running Locally


## Environment Variables

| Variable Name                       | Description                                    |
|-------------------------------------|------------------------------------------------|
| `APPLICATION_ID`                    | Application ID for Azure B2C.                  |
| `APPLICATION_SECRET`                | Application secret for Azure B2C.              |
| `AZURE_SUBSCRIPTION_ID`             | Azure Subscription ID.                         |
| `B2C_TENANT_ID`                     | Azure B2C Tenant ID.                           |
| `CONTACT_CLAIM_SCREENS`             | Contact claim screens.                         |
| `EXTENSION_ID`                      | Extension ID for Azure services.               |
| `GIT_EMAIL`                         | Email associated with Git.                     |
| `GIT_USERNAME`                      | Username associated with Git.                  |
| `INFRASTRUCTURE_ACCESS_TOKEN`       | Access token for infrastructure repository.    |
| `INFRASTRUCTURE_REPOSITORY_URL`     | URL for the infrastructure repository.         |
| `INFRASTRUCTURE_START_URL`          | URL to start infrastructure services.          |
| `DEVOPS_API_VERSION`                | API version for Azure DevOps.                  |
| `SIEM_TEMPLATE_REPOSITORY_NAME`     | Repository name for SIEM template.             |
| `SIEM_TEMPLATE_PROJECT_NAME`        | Project name for SIEM template.                |
| `SIEM_TEMPLATE_ORGANIZATION_URL`    | Organization URL for SIEM template.            |
| `SITE_NAME`                         | Name of the site.                              |
| `ENVIRONMENT`                       | Environment setting (e.g., local, production). |
| `DISCOVERY_BASE_URL`                | Discovery base URL for Azure B2C.              |
| `ISSUER_URL`                        | Issuer URL for Azure B2C.                      |
| `SIEM_TEMPLATE_BUILD_DEFINITION_ID` | Build definition ID for SIEM template.         |
| `DB_PORT`                           | Port used by the database.                     |
| `DB_USER`                           | Database user.                                 |
| `DB_PASSWORD`                       | Password for the database user.                |
| `DB_NAME`                           | Name of the database.                          |
| `DB_HOST`                           | Database host.                                 |
| `DB_SSL`                            | SSL mode for the database connection.          |
| `FUNCTIONS_CUSTOMHANDLER_PORT`      | Port for the custom handler function.          |

