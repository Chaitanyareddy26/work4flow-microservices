# Work4Flow Microservices Migration

Work4Flow is a cloud-native workflow automation and customer relationship management platform that is being migrated from a monolithic codebase to a scalable microservices architecture. This repository contains a sample code skeleton representing the microservices migration using Java and Spring Boot back-end, a React front-end, and cloud-native infrastructure.

## Tech Stack

- **Java & Spring Boot** for developing microservices  
- **Apache Kafka** for event-driven communication  
- **AWS** (EC2, RDS, S3, CloudWatch) for cloud hosting  
- **React** for building the admin portal  
- **Docker & Kubernetes** for containerization and orchestration  
- **CI/CD** pipelines using GitHub Actions and Helm  

## Features

- Decompose the monolithic Work4Flow platform into domain‑driven microservices  
- Implement asynchronous communication using Kafka producers and consumers  
- Provide REST and gRPC APIs with Resilience4j for fault tolerance  
- Develop a responsive React portal for workflow management  
- Set up containerized builds and Helm charts for deployment to Kubernetes  
- Monitor and log microservices using CloudWatch  

## Architecture

The migration follows a microservices architecture. Each bounded context (orders, users, notifications, etc.) is implemented as an independent Spring Boot service communicating via Kafka.

![Architecture Diagram](docs/architecture.png)

## Getting Started

### Prerequisites

- Java 17
- Node.js 18
- Docker & Kubernetes (Kind or Minikube)
- Maven

### Building and running locally

```bash
# Build Java services
mvn clean package -DskipTests

# Start Kafka broker (docker-compose or local)
docker compose up -d kafka

# Run a service
java -jar order-service/target/order-service-*.jar
```

### Front-end

Navigate to the `portal` folder and run:

```bash
npm install
npm start
```

## My Role & Impact

In the actual project at Work4Flow, I led the migration effort by designing the microservices architecture, implementing Kafka-based event streams, and creating CI/CD pipelines with Docker, Kubernetes and Helm. This modernization reduced deployment times by over 60% and improved system scalability.
