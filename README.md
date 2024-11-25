
# Core Project

---

# Introduction

The Core Project is a Go-based tool designed to streamline various workflows including CI/CD, security analysis, and code quality assessments. The project integrates with Azure Pipelines, SonarQube, and Horusec, providing an efficient and secure development environment. 

---

# Getting Started

Follow these steps to set up the Core Project on your local system.

### Installation Process
1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/core-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd core-project
   ```
3. Install the required dependencies:
   ```bash
   go mod tidy
   ```

4. Run the setup commands:
   ```bash
   make setup
   ```

### Software Dependencies
- **Go** (version specified in `go.mod`)
- **Azure Pipelines** (for CI/CD)
- **SonarQube** (for code quality analysis)
- **Horusec** (for security scans)

### Latest Releases
Check the [CHANGELOG.md](./CHANGELOG.md) file for detailed information about new features, updates, and bug fixes.

### API References
This project currently supports:
- Integration with SonarQube for quality metrics.
- Integration with Azure Pipelines for automated builds and deployments.

---

# Build and Test

### Build
To build the project, use the `Makefile`:
```bash
make build
```

Alternatively, you can build it directly using Go:
```bash
go build ./...
```

### Run Tests
Run unit tests to verify the integrity of the project:
```bash
make test
```
or
```bash
go test ./...
```

---

# Contribute

We welcome contributions to this project! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feat/your-feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "feat: Add your feature description"
   ```
4. Push your changes to your branch:
   ```bash
   git push origin feat/your-feature-name
   ```
5. Submit a Pull Request (PR) with a detailed explanation of your changes.

---
