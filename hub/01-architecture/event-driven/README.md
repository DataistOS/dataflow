# Event-Driven Architecture Standards

This directory defines the standards, naming conventions, and schema designs for asynchronous communication across our microservices using message brokers (e.g., Apache Kafka or RabbitMQ).

---

## 📨 Core Principles

1. **Decoupling:** Services must not depend on each other synchronously for background tasks. Changes in one service should emit events rather than direct API calls.
2. **At-Least-Once Delivery:** Consumers must be designed to be idempotent to handle potential duplicate event deliveries.
3. **Event Schema Versioning:** Every event payload must include a version field to support backward compatibility.

---

## 🏷️ Topic Naming Conventions
Topics must follow this strict naming structure:
```text
<domain>.<entity>.<action>
```
Examples:

        user.account.created

        order.payment.completed

        inventory.stock.updated

## 🏷📄 Standard Event Payload Structure

Every message published to the broker must adhere to this JSON structure:

```json
{
  "event_id": "550e8400-e29b-41d4-a716-446655440000",
  "specversion": "1.0",
  "type": "user.account.created",
  "source": "auth-service",
  "time": "2026-08-04T12:00:00Z",
  "datacontenttype": "application/json",
  "data": {
    "user_id": 12345,
    "email": "developer@example.com",
    "role": "engineer"
  }
}
```