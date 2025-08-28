# System Design Roadmap (HLD Preparation)

This roadmap covers everything you need to study for **System Design Interviews (High-Level Design)**, organized in a structured order.

---

## 1. Foundations of System Design
- **What is System Design?**
- Functional vs. Non-Functional Requirements
- Latency vs. Throughput
- Horizontal vs. Vertical Scaling
- **Availability, Reliability, Fault Tolerance**
- **Consistency**
- **Maintainability**
- **CAP Theorem**
- **Concurrency vs. Parallelism**

---

## 2. Networking & Communication
- Basics of HTTP/HTTPS
- TCP/IP and UDP
- DNS (Domain Name System)
- CDN (Content Delivery Networks)
- API Communication
  - REST APIs
  - gRPC
  - WebSockets
- Reverse Proxy (Nginx, HAProxy)

---

## 3. Databases & Storage
- Relational Databases (SQL)
- Non-Relational Databases (NoSQL)
  - Key-Value Stores
  - Document Stores
  - Wide Column Stores
  - Graph Databases
- Indexing & Query Optimization
- **Database Scaling**
  - Replication (Master-Slave, Master-Master)
  - Sharding & Partitioning
- **Consistency Models**
  - Strong Consistency
  - Eventual Consistency
  - Causal Consistency
- Database Caching (Redis, Memcached)

---

## 4. Core Distributed Systems Concepts
- Distributed Systems Basics
- Leader Election (Zookeeper, etcd)
- Consensus Algorithms (Raft, Paxos)
- Quorum & Voting Mechanisms
- Eventual Consistency (Amazon Dynamo Model)
- Vector Clocks & Versioning

---

## 5. High Availability & Scalability
- **Load Balancing**
  - Layer 4 vs. Layer 7 Load Balancing
  - Load Balancing Algorithms (Round Robin, Least Connections, IP Hash)
- Auto Scaling & Elasticity
- Health Checks & Failover
- Multi-Region Deployment
- Redundancy & Removing Single Point of Failure (SPOF)

---

## 6. Performance Optimization
- **Caching**
  - CDN Caching
  - Application Caching (Redis, Memcached)
  - Cache Eviction Policies (LRU, LFU, FIFO)
- Rate Limiting & Throttling
- Connection Pooling
- Asynchronous Processing
  - Message Queues (RabbitMQ, SQS)
  - Publish-Subscribe (Kafka, Pub/Sub)
- Data Compression
- Query Optimization

---

## 7. Architecture Patterns
- **Monolith vs. Microservices**
- Service-Oriented Architecture (SOA)
- Event-Driven Architecture
- CQRS (Command Query Responsibility Segregation)
- Saga Pattern (Distributed Transactions)
- API Gateway Pattern
- Service Discovery (Consul, Eureka, Zookeeper)

---

## 8. Reliability & Fault Handling
- **Fault Tolerance**
- Circuit Breaker Pattern
- Retry Mechanisms
- Backpressure Handling
- Graceful Degradation
- Bulkheads & Isolation
- Disaster Recovery Strategies (RPO, RTO)

---

## 9. Monitoring, Logging & Maintainability
- Observability (Logs, Metrics, Traces)
- Monitoring Tools (Prometheus, Grafana, Datadog, CloudWatch)
- Logging Systems (ELK Stack, Splunk)
- Distributed Tracing (Jaeger, Zipkin)
- CI/CD Pipelines
- Deployment Strategies
  - Blue-Green Deployments
  - Canary Releases
  - Rolling Updates
- Rollback Mechanisms

---

## 10. Security & Compliance
- Authentication & Authorization
  - OAuth 2.0
  - JWT (JSON Web Tokens)
  - SSO (Single Sign-On)
- Data Encryption
  - SSL/TLS
  - Encryption at Rest vs. In Transit
- DDoS Mitigation
- Web Application Firewall (WAF)
- Secure API Design
- Compliance Standards (GDPR, HIPAA, PCI-DSS)

---

## 11. Advanced Topics
- Distributed File Systems (HDFS, Ceph)
- Object Storage (Amazon S3, Google Cloud Storage)
- Event Streaming (Kafka, Kinesis, Pulsar)
- Serverless Architectures (AWS Lambda, GCP Cloud Functions)
- Containerization & Orchestration
  - Docker
  - Kubernetes
- Edge Computing
- Hybrid & Multi-Cloud Architectures

---

## 12. Case Studies & System Design Problems
- **Beginner-Friendly**
  - URL Shortener (TinyURL)
  - Pastebin
  - Rate Limiter
- **Intermediate**
  - Chat Application (WhatsApp, Messenger)
  - News Feed System (Facebook, Twitter)
  - Distributed Caching System
- **Advanced**
  - YouTube / Netflix (Video Streaming)
  - Uber / Lyft (Ride-Sharing)
  - Amazon / Flipkart (E-commerce)
  - Google Drive / Dropbox (File Storage)
  - Payment Gateway (Stripe, PayPal)

---

## Key Resources
- **Books**
  - Designing Data-Intensive Applications – Martin Kleppmann
  - System Design Interview Vol 1 & 2 – Alex Xu
- **Websites**
  - System Design Primer (GitHub)
  - High Scalability Blog
- **Practice**
  - LeetCode System Design
  - Grokking the System Design Interview (Educative)

---
