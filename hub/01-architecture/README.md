# Architecture Blueprints & Dataflow

This directory defines how data moves across our 100+ repositories and how different microservices communicate with each other. 

---

## 🏛️ Architecture Patterns

We follow two primary patterns for service communication, depending on the use case:

1. **Synchronous Communication (API Gateway):**
   * Used for direct client-to-service requests or real-time operations.
   * Standardized via REST APIs and GraphQL.
   * Managed centrally through the API Gateway.

2. **Asynchronous Communication (Event-Driven):**
   * Used for background processing, decoupling services, and data pipelines.
   * Powered by Message Brokers (e.g., Kafka / RabbitMQ).
   * Events must follow strict JSON schemas and naming conventions (e.g., `domain.entity.action`).

---

## 📂 Subdirectories
* **`api-gateway/`**: Contains specifications, routing rules, and authentication standards for API endpoints.
* **`event-driven/`**: Contains topic naming conventions, event schemas, and publisher/subscriber patterns.
