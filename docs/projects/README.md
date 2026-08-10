# Projects

A curated collection of projects focused on **Data Engineering, DevOps, and Event-Driven Architecture**.

Each project demonstrates practical experience in designing, building, and operating reliable data infrastructure and integration systems.

---

## Featured Projects

### 🔄 Event-Driven Integration with CDC

**Connecting Odoo PostgreSQL with external systems using Change Data Capture (CDC), Debezium, Kafka, Apicurio Schema Registry, and Python-based transformation services.**

This project implements a real-time data integration pipeline that captures changes directly from PostgreSQL and delivers them to external applications through an event-driven architecture.

**Architecture**

```text
┌─────────────────┐
│  Odoo           │
│  PostgreSQL     │
└────────┬────────┘
         │
         │ CDC / WAL
         ▼
┌─────────────────┐
│    Debezium     │
│   Connector     │
└────────┬────────┘
         │
         │ Events
         ▼
┌─────────────────┐
│      Kafka      │
│     Topics      │
└────────┬────────┘
         │
         │ Avro Events
         ▼
┌─────────────────────────┐
│ Apicurio Schema Registry│
│                         │
│ Schema & Versioning     │
└─────────────────────────┘
         ▲
         │ Schema
         │
┌────────┴────────┐
│ Python          │
│ Transformation  │
│ Service         │
└────────┬────────┘
         │
         │ Transformed Data
         ▼
┌─────────────────┐
│ External        │
│ Applications    │
└─────────────────┘
```

**Key Components**

| Component             | Role                                   |
| --------------------- | -------------------------------------- |
| **PostgreSQL**        | Source database for Odoo               |
| **Debezium**          | Captures database changes through CDC  |
| **Kafka**             | Distributed event streaming platform   |
| **Apicurio Registry** | Schema management and versioning       |
| **Python**            | Data transformation and business logic |
| **Docker**            | Containerized runtime environment      |

**Key Capabilities**

* Real-time Change Data Capture from PostgreSQL
* Event-driven data integration
* Avro serialization and schema management
* Schema versioning and compatibility
* Data transformation using Python
* Decoupled integration between systems
* Containerized transformation services
* Fault handling and message processing

**Data Flow**

```text
PostgreSQL
    ↓
Debezium
    ↓
Kafka
    ↓
Python Transformer
    ↓
External Application
```

**Architecture Diagram**

[View Interactive Architecture Diagram](https://mermaid.ai/app/projects/8023df45-d663-4dd3-9763-4ec72af2ea61/diagrams/adbcf13c-86f5-4516-8a74-c3a34a60bbb6/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiYWRiY2YxM2MtODZmNS00NTE2LThhNzQtYzNhMzRhNjBiYmI2IiwiYWNjZXNzIjoiVmlldyIsImlhdCI6MTc4NjMzNDc1MH0.S2l7aBLzMja5mJr9bGdJtXhtEmYnxSjuW8i1YSyJfmA?entryPoint=share-modal)

---

## Project Focus

The projects in this portfolio cover several areas of modern infrastructure and data engineering:

### Data Engineering

* Change Data Capture (CDC)
* Data integration
* Event-driven pipelines
* Data transformation
* Streaming architecture
* Schema management

### DevOps & Infrastructure

* Docker & containerization
* CI/CD
* Infrastructure automation
* Monitoring & observability
* Production deployment

### Distributed Systems

* Apache Kafka
* Event-driven architecture
* Asynchronous processing
* Service decoupling
* Fault-tolerant data pipelines

---

## Engineering Principles

These projects are built around several engineering principles:

> **Decouple systems, automate repetitive processes, make data flows observable, and design pipelines that can recover from failures.**

The goal is not only to move data from one system to another, but to build **reliable, maintainable, and scalable integration infrastructure**.

---

## Repository

Each project is maintained in its own repository with dedicated documentation covering:

* Architecture
* Data flow
* Configuration
* Deployment
* Monitoring
* Troubleshooting
* Technical decisions
* Future improvements

More projects will be added as the portfolio evolves.
