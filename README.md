# Project Design Overview: Software Design

**Author:** Trương Công Thiên Phú

**Co-Author:** Đặng Quang Hưng

**Status:** Draft

**Last Updated:** 2026-01-18

---

## 1. Executive Summary
**Objective:**
Build a scalable [Service Type, e.g., RESTful API / Microservice] that handles [Core Function, e.g., real-time inventory management] to replace the legacy [Old System] and reduce latency by [X]%.

**Problem Statement:**
Currently, our system struggles with [Key Pain Point, e.g., high concurrent writes during peak traffic], leading to [Consequence, e.g., data inconsistency].

**Success Metrics:**
* P99 Latency < [e.g., 200ms]
* Availability: 99.9%
* Throughput: Handles [X] requests per second (RPS)

---

## 2. System Architecture

### 2.1 High-Level Diagram
> *[Insert Link to Architecture Diagram here]*

### 2.2 Tech Stack
| Component | Technology | Rationale |
| :--- | :--- | :--- |
| **Backend** | [e.g., Go / Node.js] | High concurrency support, strictly typed. |
| **Database** | [e.g., PostgreSQL] | ACID compliance required for transactional data. |
| **Caching** | [e.g., Redis] | To offload read-heavy traffic for user sessions. |
| **Infra** | [e.g., AWS / Kubernetes] | Auto-scaling capabilities. |

---

## 3. Core Modules & Data Flow

### 3.1 Authentication Module
* **Mechanism:** JWT (JSON Web Tokens) with OAuth2.
* **Flow:** `Client` -> `Auth Service` -> `Return Access/Refresh tokens`.

### 3.2 [Core Feature A]
* **Description:** Handles the processing of [X].
* **Key Logic:**
    1.  Validate input schema.
    2.  Publish event to `topic-A`.
    3.  Worker consumes event and updates DB asynchronously.

### 3.3 [Core Feature B]
* **Description:** Reporting and Analytics.
* **Key Logic:** Aggregates data via daily Cron jobs using a read-replica DB to avoid locking the primary.

---

## 4. API Design (Draft)

**Base URL:** `/api/v1`

* `GET /resources`: List all items (Paginated).
* `POST /resources`: Create a new item.
    * *Payload:* `{ "name": "string", "value": int }`
* `GET /resources/{id}`: Detailed view.

---

## 5. Risks & Mitigation

| Risk | Impact | Mitigation Strategy |
| :--- | :--- | :--- |
| **Data Migration** | Potential data loss during switchover. | Use double-writing strategy and verify with checksums. |
| **Latency** | New network hops between microservices. | Implement gRPC for internal communication; aggressive caching. |
| **Complexity** | Steeper learning curve for new devs. | Comprehensive documentation and containerized dev environments. |

---

## 6. Project Timeline

* **Phase 1 (Week 1-2):** Proof of Concept (PoC) & Database Schema Design.
* **Phase 2 (Week 3-6):** Core API Development & Unit Testing.
* **Phase 3 (Week 7):** Integration Testing & Load Testing (k6/JMeter).
* **Phase 4 (Week 8):** Canary Deployment & Monitoring setup.

---

## 7. Open Questions
* *Do we need multi-region support immediately?*
* *Is the legacy API deprecation date finalized?*