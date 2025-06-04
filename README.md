infrastructure
Shared infrastructure setup for Eldorado, a marketplace platform.
This repository contains the core infrastructure components and orchestration needed to run the distributed microservices architecture locally and in development environments.

🔧 Stack

Apache Kafka — distributed event streaming platform for microservice communication
Apache Zookeeper — coordination service for Kafka cluster management
Kafka UI — web-based interface for monitoring and managing Kafka topics
Docker Compose — container orchestration for local development
Just — command runner for development tasks


🚀 Infrastructure Components
Message Streaming

Kafka Broker — handles event streaming between microservices (auth-service, notification-service, etc.)
Zookeeper — manages Kafka cluster coordination and configuration
Kafka UI — provides visual interface for topic management and message monitoring

Networking

External Network — microservices-net for service-to-service communication
Health Checks — automated service health monitoring with retry policies
Persistent Volumes — data persistence for Kafka and Zookeeper


🛠️ Local Development
Prerequisites

Docker and Docker Compose
Just command runner (cargo install just or brew install just)

1. Create network
bashdocker network create microservices-net
2. Start infrastructure
bashjust up
3. Access services

Kafka UI: http://localhost:8080
Kafka Broker: localhost:9092
Zookeeper: localhost:2181

4. Stop infrastructure
bashjust down

📋 Service Integration
This infrastructure supports the following Eldorado microservices:

auth-service — user authentication and JWT management
notification-service — email notifications and messaging
Additional services can connect via the microservices-net network

Each service can publish and consume events through Kafka topics for decoupled communication.