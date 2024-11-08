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
## Catalog - Infrastructure Overview

![Diagram showing the infrastructure of the catalog system](https://github.com/user-attachments/assets/0593dd7f-6e90-460c-8f9c-580e7177e925)


## Catalog - CI/CD Pipeline

![Diagram illustrating the CI/CD pipeline for the catalog deployment](https://github.com/user-attachments/assets/48582e74-ce86-465a-ba48-3d81ad59c7d9)


## Catalog - Database and HTTP Request Flow

![Diagram displaying database interactions and HTTP request flow within the catalog system](https://github.com/user-attachments/assets/84fe3ca4-a009-4789-a16d-6da40ad2f42f)


## Running Locally
**Once you have cloned the repository, go to the root of this project.**

**Install the dependencies:**
```bash
go build -o catalog
```
**Run Catalog using the command below:**

```bash
$ ./catalog
```

**Create a `.env` file in the root directory and add the environment variables for the keys present in the `.env.example`.**
Run the test suite using the command below in the root directory:

```bash
$ make test
```



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

