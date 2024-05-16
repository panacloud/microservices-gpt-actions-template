# OpenAI Custom GPT Action Template (Peotry-FastAPI-SQLModel-Postgres-Kafka-Kong-Docker)

### Overview

This project provides a template for building [OpenAI Custom GPT Actions](https://platform.openai.com/docs/actions/introduction) with [microservice pattern](https://cloud.google.com/learn/what-is-microservices-architecture) using [Event Driver Architecture](https://microservices.io/patterns/data/event-driven-architecture.html).
. The template leverages various technologies and tools to facilitate efficient development, testing, deployment, and CI/CD. The core components and their roles are as follows:

- **Python**: The primary programming language for developing GPT actions.
- **Poetry**: Dependency management and packaging tool for Python.
- **FastAPI**: Web framework for building APIs with Python 3.12+.
- **SQLModel**: SQL databases interaction using Python, combining the best features of SQLAlchemy and Pydantic.
- **Postgres**: Relational database management system.
- **Kafka**: Distributed event streaming platform used for building real-time data pipelines and streaming applications.
- **Kong**: API gateway for managing API requests.
- **Docker**: Platform for developing, shipping, and running applications in containers.
- **Kubernetes**: Container orchestration system for automating application deployment, scaling, and management.
- **Terraform**: Infrastructure as code tool for building, changing, and versioning infrastructure.
- **Testcontainers**: Tool for running Docker containers for integration tests.
- **GitHub Actions**: CI/CD tool for automating workflows.

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



