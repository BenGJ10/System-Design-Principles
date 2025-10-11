# High Level System Design (HLD) Roadmap

This roadmap takes you **from foundations → distributed systems → real-world architectures**, in a progressive, interview-focused way.

---

## 1. Foundations of System Design

Build conceptual clarity before diving into systems.

* What is System Design?
* Functional vs Non-Functional Requirements
* Horizontal vs Vertical Scaling
* **Latency vs Throughput**
* **Availability, Reliability, Fault Tolerance**
* **Consistency & CAP Theorem**
* **Concurrency vs Parallelism**
* **Idempotency & Statelessness** (often asked in interviews)
* **Data Partitioning Basics**

*Goal:* Understand how system design is about **trade-offs** between these principles.

---

## 2. Networking & Communication

Everything begins with how systems talk to each other.

* **Networking Basics**
* **TCP/IP vs UDP**
* **HTTP/HTTPS**
* **DNS (Domain Name System)**
* **CDN (Content Delivery Networks)**
* **API Communication**

  * REST
  * gRPC
  * GraphQL
  * WebSockets
  * SOAP (legacy systems)
* **Proxy & Reverse Proxy (Nginx, HAProxy)**
* **Load Balancing (Layer 4 vs Layer 7 + Algorithms)**

*Goal:* You should know **how requests travel from browser → backend → database** and how systems optimize that flow.

---

## 3. Databases & Storage Systems

The backbone of every design.

### **Database Types**

* Relational (SQL) – ACID
* Non-Relational (NoSQL)

  * Key-Value (Redis, DynamoDB)
  * Document (MongoDB, CouchDB)
  * Wide Column (Cassandra)
  * Graph (Neo4j)

### **Database Scaling**

* Replication (Master-Slave, Master-Master)
* Sharding & Partitioning
* Indexing & Query Optimization
* Denormalization for Performance
* Read/Write Splitting

### **Consistency Models**

* Strong Consistency
* Eventual Consistency
* Causal Consistency

*Goal:* Be able to **choose and justify** which database fits each use case (OLTP vs OLAP, consistency vs latency trade-offs).

---

## 4. Caching & Performance Optimization

Caching is one of the most common interview deep-dives.

* **Types of Caching**

  * CDN Caching
  * Application Caching (Redis, Memcached)
  * Database Query Caching
* **Eviction Policies**: LRU, LFU, FIFO
* **Write Policies**: Write-through, Write-back, Write-around
* **Cache Invalidation**: The hardest problem in system design
* **Content Hashing & TTLs**

*Goal:* Understand where to cache (client, CDN, app, DB) and when to **bypass or invalidate** it.

---

## 5. Messaging & Asynchronous Processing

Crucial for scalable, decoupled architectures.

* **Message Queues**

  * RabbitMQ, SQS, Kafka
* **Pub/Sub Pattern**
* **Event-Driven Architecture**
* **Producer-Consumer Model**
* **Idempotency in Messaging**
* **Backpressure Handling**
* **Retry and Dead Letter Queues (DLQ)**

*Goal:* Be able to handle **spikes in workload** and design resilient background systems.

---

## 6. High Availability & Scalability

Keeping systems alive under pressure.

* **Load Balancing (L4 vs L7)**
* **Health Checks & Failover**
* **Auto Scaling**
* **Replication and Redundancy**
* **Multi-Region Deployment**
* **Disaster Recovery**

  * RTO (Recovery Time Objective)
  * RPO (Recovery Point Objective)

*Goal:* Build systems that gracefully handle traffic spikes and failures without downtime.

---

## 7. Core Distributed Systems Concepts

Deep concepts that power scalable systems.

* Distributed Consensus (Paxos, Raft)
* Leader Election (Zookeeper, etcd)
* Quorum Reads/Writes
* Vector Clocks
* Gossip Protocol
* CAP & BASE Theorems (advanced view)
* Distributed Transactions (2PC, 3PC)
* Clock Synchronization & Logical Clocks

*Goal:* Understand **how distributed systems coordinate and agree** on data/state under failure.

---

## 8. Architecture & Design Patterns

Learn reusable structures for real-world systems.

* **Monolithic vs Microservices**
* **Service-Oriented Architecture (SOA)**
* **Event-Driven Architecture**
* **CQRS (Command Query Responsibility Segregation)**
* **Saga Pattern (Distributed Transactions)**
* **API Gateway Pattern**
* **Service Discovery (Consul, Eureka, Zookeeper)**
* **Sidecar Pattern (used in Kubernetes)**

*Goal:* Know when to use each architecture and trade-offs (simplicity vs flexibility).

---

## 9. Reliability & Fault Handling

Keeping things running even when parts fail.

* **Circuit Breaker Pattern**
* **Bulkhead Isolation**
* **Graceful Degradation**
* **Retry & Timeout Strategies**
* **Backoff Mechanisms**
* **Chaos Engineering (Netflix’s Simian Army)**

*Goal:* Design fault-tolerant systems that degrade gracefully rather than crash.

---

## 10. Observability & Maintainability

Building systems you can monitor, debug, and evolve.

* **Monitoring**

  * Prometheus, Grafana, CloudWatch
* **Logging**

  * ELK Stack (Elasticsearch, Logstash, Kibana)
* **Tracing**

  * Jaeger, Zipkin, OpenTelemetry
* **Metrics**

  * RED & USE Principles
* **CI/CD Pipelines**

  * Blue-Green, Canary, and Rolling Deployments

*Goal:* Know how to ensure **visibility** and **continuous improvement** in production.

---

## 11. Security & Compliance

Essential for production systems.

* **Authentication vs Authorization**

  * OAuth 2.0, JWT, SSO
* **Encryption**

  * SSL/TLS, Data at Rest vs In Transit
* **DDoS Protection**
* **Web Application Firewall (WAF)**
* **API Security & Rate Limiting**
* **Compliance Standards**

  * GDPR, HIPAA, PCI-DSS

*Goal:* Be able to secure your design at every layer.

---

## 12. Advanced & Cloud Topics

What top-tier systems rely on.

* **Distributed File Systems (HDFS, Ceph)**
* **Object Storage (S3, GCS)**
* **Event Streaming (Kafka, Kinesis, Pulsar)**
* **Serverless Architectures (Lambda, Cloud Functions)**
* **Containerization (Docker)**
* **Orchestration (Kubernetes)**
* **Edge Computing**
* **Hybrid & Multi-Cloud Designs**
* **Global System Design** (GeoDNS, Anycast, CDN, Multi-Region DBs)

*Goal:* Design globally available, cloud-ready systems.

---

## 13. System Design Case Studies

Now that you know the parts — build the whole.

### Beginner-Level

* URL Shortener (TinyURL)
* Rate Limiter
* Pastebin

### Intermediate

* Chat Application (WhatsApp)
* News Feed System (Twitter)
* Notification System
* Distributed Cache

### Advanced

* YouTube / Netflix (Streaming)
* Uber / Lyft (Ride Sharing)
* Google Drive / Dropbox (Cloud Storage)
* Amazon / Flipkart (E-commerce)
* Stripe / PayPal (Payment System)

*Goal:* Practice **end-to-end thinking** — from requirements → scaling → trade-offs.

---

## 14. Learning Resources

The best materials to master every layer.

| Category               | Recommended                                                                                                |
| ---------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Books**              | *Designing Data-Intensive Applications* (Martin Kleppmann), *System Design Interview Vol. 1 & 2* (Alex Xu) |
| **Courses**            | Grokking the System Design Interview (Educative), ByteByteGo videos, Gaurav Sen YouTube                    |
| **Practice**           | System Design Primer (GitHub), LeetCode Design Questions                                                   |
| **Tools for Diagrams** | Excalidraw, Draw.io, Whimsical                                                                             |

---
