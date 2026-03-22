# Roboshop Catalogue Microservice - Continuous Integration (CI)

This repository contains the Continuous Integration (CI) pipeline and source code for the **Catalogue** service. It is designed to automate the building, testing, and delivery of the Catalogue micro service using modern DevOps practices.

## Overview

- **Source Code**: The Catalogue service source code is maintained in this repository.
- **Dockerfile**: Containerization is enabled via a `Dockerfile` for consistent deployment across environments.
- **Jenkinsfile**: CI/CD automation is implemented using Jenkins pipelines, described in the `Jenkinsfile`.

## Features

- Automated build and test workflows using Jenkins.
- Containerized application deployment using Docker.
- Easily extendable for future enhancements or additional stages in the pipeline.

## Jenkins Shared Library

This project leverages a centralized [Jenkins Shared Library](https://github.com/BharathKumarReddy2103/jenkins-shared-library) for consistent and reusable CI/CD pipeline steps across multiple services. The shared library abstracts common pipeline logic, making it easier to maintain and scale DevOps workflows.

## Repository Structure

```
.
├── Dockerfile      # Defines the container image for the application
├── Jenkinsfile     # Describes CI/CD pipeline for Jenkins
├── src/            # Source code for the Catalogue service
└── ...
```

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/)
- [Jenkins](https://www.jenkins.io/) (for running the pipeline)
- [Git](https://git-scm.com/)

### Building the Docker Image

```bash
docker build -t catalogue-service .
```

### Running the Service

```bash
docker run -p 8080:8080 catalogue-service
```

### Running CI/CD Pipeline

1. Ensure Jenkins is set up and configured with access to this repository.
2. The pipeline will automatically trigger on push events or pull requests (depending on your Jenkins configuration).
3. Review the pipeline stages in the `Jenkinsfile`.

## Contributing

Contributions are welcome. Please fork the repository and create a pull request with your proposed changes.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For questions, issues, or feature requests, please open an [issue](https://github.com/BharathKumarReddy2103/catalogue/issues).
