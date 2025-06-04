# infrastructure
Shared infrastructure setup for **Eldorado**, a marketplace platform.
This repository contains the core infrastructure components and orchestration needed to run the distributed microservices architecture locally and in development environments.
---
## 🔧 Stack
- **Apache Kafka** — distributed event streaming platform for microservice communication
- **Apache Zookeeper** — coordination service for Kafka cluster management
- **Kafka UI** — web-based interface for monitoring and managing Kafka topics
- **Docker Compose** — container orchestration for local development
- **Just** — command runner for development tasks
---
## 🚀 Features
- Kafka event streaming for microservice communication
- Zookeeper cluster coordination and management
- Web-based Kafka UI for topic monitoring
- Health checks and automatic service recovery
- Persistent data volumes for reliability
- External network for service integration
---
## 🛠️ Local Development
### 1. Create network
```bash
docker network create microservices-net
```
### 2. Start infrastructure
```bash
just up
```
