# OpenAI Custom GPT Action Template (Peotry-FastAPI-SQLModel-Postgres-Kafka-Kong-Docker)

### Overview

This project provides a template for building [OpenAI Custom GPT Actions](https://platform.openai.com/docs/actions/introduction) with [microservice pattern](https://cloud.google.com/learn/what-is-microservices-architecture) using [Event Driver Architecture](https://microservices.io/patterns/data/event-driven-architecture.html).
. The template leverages various technologies and tools to facilitate efficient development, testing, deployment, and CI/CD. The core technologies and their roles are as follows:


## Technologies Used

### Backend Technologies
- **Python**: The primary programming language used for developing GPT Actions.
- **Poetry**: Dependency management and packaging tool for Python projects.
- **FastAPI**: Modern, fast (high-performance) web framework for building APIs with Python 3.7+ based on standard Python type hints.
- **SQLModel**: SQL databases in Python, designed for simplicity, compatibility, and robustness. It’s built on top of Pydantic and SQLAlchemy.
- **Postgres**: Powerful, open-source object-relational database system.
- **Kafka**: Distributed event streaming platform capable of handling trillions of events a day.
- **Kong**: Cloud-native, fast, scalable, and distributed API gateway.

### Containerization and Development
- **Docker**: Platform for developing, shipping, and running applications in containers.
- **DevContainer**: Development environments hosted in containers to ensure consistency across different environments.

### Deployment and Testing
- **Kubernetes**: Container orchestration system for automating deployment, scaling, and management of containerized applications.
- **Terraform**: Infrastructure as Code (IaC) tool that lets you define both cloud and on-prem resources in human-readable configuration files that you can version, reuse, and share.
- **testcontainers**: Provides lightweight, disposable instances of common databases, Selenium web browsers, or anything else that can run in a Docker container, for testing.
- **GitHub Actions**: CI/CD tool that automates workflows, including testing and deployment.

### Client Tools
- **VSCode**: Free source-code editor made by Microsoft for Windows, Linux, and macOS.
- **PgAdmin**: Open-source administration and development platform for PostgreSQL.

## Architecture Overview

The template is designed with a microservice pattern and Event-Driven Architecture to ensure each GPT Action is isolated, scalable, and easy to manage. Here’s an overview of how the components interact:

1. **Microservices**: Each GPT Action is a separate microservice built using FastAPI and SQLModel, containerized with Docker.
2. **Event-Driven Architecture**: Kafka is used for event streaming, enabling real-time data processing and communication between microservices.
3. **API Gateway**: Kong serves as the API gateway, routing requests to the appropriate microservice.
4. **Database**: Postgres is used for persistent data storage.
5. **Development Environment**: DevContainer ensures a consistent development environment, and VSCode provides a powerful IDE.
6. **Deployment**: Kubernetes manages the containerized applications, and Terraform handles infrastructure provisioning.
7. **CI/CD**: GitHub Actions automate the testing and deployment processes.
8. **Testing**: testcontainers facilitate isolated and reliable testing environments.

### Key Concepts and Technologies

1. **Microservice Architecture**: 
   - Microservices break down the application into smaller, independent services that can be developed, deployed, and scaled independently.
   - **Benefits**: Scalability, flexibility, and resilience.

2. **Event-Driven Architecture**:
   - Utilizes events to trigger and communicate between decoupled services.
   - **Benefits**: Real-time data processing, improved scalability, and fault tolerance.

3. **FastAPI**:
   - High-performance, easy-to-use web framework for building APIs.
   - **Benefits**: Automatic interactive API documentation, high performance, and easy integration with asynchronous libraries.

4. **SQLModel**:
   - Simplifies working with SQL databases and provides a convenient way to define models and perform queries.
   - **Benefits**: Combines the power of SQLAlchemy and Pydantic, type annotations, and easy model definition.

5. **Postgres**:
   - Robust and reliable relational database system.
   - **Benefits**: ACID compliance, extensibility, and strong community support.

6. **Kafka**:
   - Distributed event streaming platform for high-throughput, low-latency data processing.
   - **Benefits**: Scalability, durability, and fault-tolerance.

7. **Kong**:
   - API gateway for managing, monitoring, and securing API requests.
   - **Benefits**: Load balancing, rate limiting, and request transformation.

8. **Docker**:
   - Simplifies the development and deployment process by packaging applications in containers.
   - **Benefits**: Consistency across environments, isolation, and portability.

9. **Kubernetes**:
   - Manages containerized applications across multiple hosts, providing deployment, scaling, and management capabilities.
   - **Benefits**: Automated scaling, self-healing, and efficient resource utilization.

10. **Terraform**:
    - Infrastructure as code tool for provisioning and managing cloud infrastructure.
    - **Benefits**: Version control, automation, and reproducibility.

11. **Testcontainers**:
    - Enables running Docker containers for integration tests, ensuring a consistent testing environment.
    - **Benefits**: Reliable testing, isolation, and easy setup.

12. **GitHub Actions**:
    - Automates workflows for building, testing, and deploying applications.
    - **Benefits**: Continuous integration and delivery, automation, and integration with GitHub repositories.


### Setting Up the Development Environment

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/your-repo/openai-custom-gpt-action-template.git
   cd openai-custom-gpt-action-template
   ```

2. **Install Dependencies**:
   ```sh
   poetry install
   ```

3. **Run the Application**:
   ```sh
   poetry run uvicorn src.main:app --reload
   ```

4. **Run Tests**:
   ```sh
   poetry run pytest
   ```

### Deploying with Docker and Kubernetes

1. **Build Docker Image**:
   ```sh
   docker build -t custom-gpt-action-template .
   ```

2. **Run Docker Container**:
   ```sh
   docker compose up
   ```

3. **Deploy to Kubernetes**:
   ```sh
   kubectl apply -f k8s-deployment.yml
   ```

4. **Manage Infrastructure with Terraform**:
   ```sh
   terraform init
   terraform apply
   ```

### CI/CD with GitHub Actions

1. **Configure GitHub Actions Workflow**:
   - The CI/CD pipeline is defined in `.github/workflows/ci-cd.yml`.
   - Ensure your repository has the necessary secrets configured for Docker, Kubernetes, and other integrations.


### Benefits of Using These Technologies Together

1. **Modularity**: Each component can be developed, tested, and deployed independently, allowing for greater flexibility and maintainability.
2. **Scalability**: Easily scale individual services based on demand, ensuring optimal resource utilization.
3. **Reliability**: Enhanced fault tolerance and resilience through service isolation and event-driven communication.
4. **Efficiency**: Streamlined development and deployment processes with Docker, Kubernetes, and CI/CD integration.
5. **Consistency**: Consistent development, testing, and production environments using containers and infrastructure as code.

By leveraging these technologies, this template provides a robust foundation for developing, testing, and deploying OpenAI Custom GPT Actions in a microservice pattern using event-driven architecture.



