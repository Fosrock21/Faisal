
# Introduction

This project is a foundational Go library that provides a collection of common tools and utilities designed to streamline development across multiple projects. Serving as a base dependency, it encapsulates reusable components such as logging, validation, HTTP handling, messaging, and monitoring, ensuring consistency and reducing redundancy in codebases. By offering a modular and extensible design, this library simplifies the integration of essential functionalities, enabling teams to focus on building core features while maintaining high standards of reliability and efficiency across projects.

---

# Getting Started

1. **Installation Process**  
   - Ensure Go (version 1.18+ recommended) is installed.
   - If needed, configure your Go environment (`GOPRIVATE` / `GONOSUMDB`) to allow accessing private repositories.
   - Install the library:
     ```bash
     go get dev.azure.com/yourorg/yourproject/_git/myproject
     ```
   - Update your `go.mod` file accordingly and import the relevant packages from `pkg/` into your code.

2. **Software Dependencies**  
   The `go.mod` file lists only the direct dependencies required by this project. Transitive dependencies (those indirectly required) do not need to be manually included or managed—they will be automatically resolved by the Go toolchain.

---

# Build and Test

### Running Locally  
Once you have cloned the repository, navigate to the project’s root directory.

1. Install the dependencies:
   ```bash
   go mod tidy ./...
   ```

2. **Run the Producer:**  
   Use the Docker Compose file located inside the `.dev` folder to spin up required services:
   ```bash
   make docker-up
   ```

3. **Install Azure Functions Core Tools:**  
   Follow the [official instructions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local) to install the Azure Functions Core Tools on your system.

4. **Start the function locally:**  
   ```bash
   func start --custom --port 8080
   ```

5. **Test the local environment:**  
   From a separate terminal, verify that the service and its dependencies are running as expected:
   ```bash
   curl http://localhost:8080/swagger/index.html
   ```

---

# Project Structure

Below is an overview of the repository structure to help you navigate and understand where various components reside:

```
.
├── .azuredevops/                 # Azure DevOps configurations and templates
│   ├── pull_request_template/    # Templates for pull requests
├── .gitignore                    # Git ignore rules
├── CHANGELOG.md                  # Project changelog
├── LICENSE                       # Project license
├── Makefile                      # Automation commands
├── README.md                     # Project documentation (this file)
├── azure-pipelines.yml           # Azure Pipelines configuration
├── go.mod                        # Go module dependencies
├── go.sum                        # Go module checksum
├── horusec.json                  # Horusec configuration file
├── sonar-project.properties      # SonarQube project configuration
├── pkg/                          # Main package source code
│   ├── app/                      # Core application logic
│   ├── gin/                      # HTTP middleware and routing
│   ├── git/                      # Git client implementation
│   ├── io/                       # File system utilities
│   ├── kafka/                    # Kafka-related logic
│   ├── logger/                   # Logging utilities
│   ├── pagination/               # Pagination utilities
│   ├── test/                     # Testing utilities
│   ├── validation/               # Validation logic
│   └── watcher/                  # Monitoring and alerting logic
├── test/                         # Test-specific code
│   ├── app/                      # Tests for the app module
│   └── watcher/                  # Tests for the watcher module
```

This layout promotes modular design and maintainability, ensuring you can easily locate components for enhancements, debugging, and updates.

---

# Contribute

### Report Issues:  
If you encounter bugs or have feature requests, open an issue with a clear description and relevant details.

### Submit Pull Requests:  

1. Fork the repository.
2. Create a new branch for your changes.
3. Write clear commit messages.
4. Include or update tests for any new functionality.
5. Open a pull request against the `main` branch, providing a detailed description of your changes.

### Coding Standards and Testing:  
Maintain the code quality by adhering to existing standards and ensuring all tests pass before submitting a PR.

---

