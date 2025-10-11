# Load Balancer vs Reverse Proxy

## Definition

Both **Load Balancers** and **Reverse Proxies** act as intermediaries between clients and backend servers, but they serve different purposes in how they manage and route traffic.

---

## Load Balancer

* A **Load Balancer** distributes incoming network traffic **across multiple backend servers** to ensure that no single server is overloaded.
* Its main goal is to **improve availability, scalability, and performance**.

**Example Tools:**
→ Nginx (with load balancing), HAProxy, AWS ELB, Google Cloud Load Balancer.

---

## Reverse Proxy

* A **Reverse Proxy** sits in front of one or more servers and forwards client requests to them.
* It focuses on **security, caching, SSL termination, and request routing**, not necessarily on balancing load.

**Example Tools:**
→ Nginx, Apache HTTP Server, Traefik.

---

## Comparison: Load Balancer vs Reverse Proxy

| **Aspect**               | **Load Balancer**                                                                                         | **Reverse Proxy**                                                                         |
| ------------------------ | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Primary Purpose**      | Distributes incoming requests across multiple backend servers to balance load.                            | Forwards client requests to specific backend servers, providing abstraction and security. |
| **Focus**                | Performance, scalability, and high availability.                                                          | Security, caching, SSL termination, and centralized routing.                              |
| **Traffic Distribution** | Yes — distributes requests among multiple servers using algorithms like Round Robin or Least Connections. | No — typically routes requests to one specific backend or handles logic-based routing.    |
| **Client Awareness**     | Clients interact with the load balancer’s IP (not directly with servers).                                 | Clients interact with the reverse proxy’s IP (not directly with backend).                 |
| **Common Use Case**      | Large-scale systems handling millions of concurrent requests.                                             | Single-application deployments needing security, caching, or request filtering.           |
| **Health Checks**        | Actively monitors server health and removes unhealthy servers from the pool.                              | May include basic health checks but not required.                                         |
| **SSL Termination**      | Often supported to reduce backend load.                                                                   | Commonly supported — one of its key responsibilities.                                     |
| **Examples**             | HAProxy, AWS ALB/ELB, Google Load Balancer.                                                               | Nginx, Apache, Traefik.                                                                   |

---

## Combined Usage

* In many production architectures, **a reverse proxy and a load balancer work together**.
* Example architecture:

  * **Reverse Proxy (Nginx)** handles SSL termination, caching, and routing.
  * **Load Balancer (HAProxy or AWS ELB)** distributes traffic among multiple Nginx servers for scalability.

**Diagram:**

```
Client
   ↓
Load Balancer (HAProxy / ELB)
   ↓
Reverse Proxy (Nginx)
   ↓
Backend Servers / Application Servers
```

---

## Quick Summary

| **When to Use**                                                           | **Choose**            |
| ------------------------------------------------------------------------- | --------------------- |
| You need to **distribute traffic** and scale horizontally.                | **Load Balancer**     |
| You need to **secure, route, or cache** requests for one or more servers. | **Reverse Proxy**     |
| You need **both scalability and security**.                               | Use **both together** |

---
