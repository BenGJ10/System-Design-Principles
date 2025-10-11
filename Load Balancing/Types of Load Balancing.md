# Types of Load Balancing

Load balancing distributes incoming traffic across multiple servers to improve **availability**, **scalability**, and **performance**. Below are the main types explained in depth.

## 1. Hardware Load Balancing

- **Description**: Uses dedicated physical devices to manage traffic.

- **How It Works**: Specialized appliances sit between clients and servers, distributing requests using built-in algorithms.

- **Pros**:
  - High performance with dedicated hardware.
  - Built-in security and reliability features.

- **Cons**:
  - Expensive and less flexible.
  - Hardware upgrades required for scaling.

- **Use Cases**: Large enterprises, data centers requiring very low latency.

---

## 2. Software Load Balancing

- **Description**: Runs on commodity servers or cloud instances instead of custom hardware.

- **Examples**: **Nginx**, **HAProxy**, **Traefik**, cloud services like **AWS ELB** or **GCP Load Balancer**.

- **Pros**:
  - Cost-effective and easy to scale horizontally.
  - Highly configurable and integrates well with DevOps tools.

- **Cons**:
  - Requires OS and software maintenance.

- **Use Cases**: Web apps, microservices, cloud environments.

---

## 3. DNS Load Balancing

- **Description**: Uses **Domain Name System (DNS)** to distribute requests to different server IPs.

- **How It Works**: DNS records map a domain to multiple IPs. Clients are directed to one based on policies like round robin or geo-location.

- **Pros**:
  - Simple to set up; no single point of failure at the app level.

- **Cons**:
  - DNS caching can delay failover.
  - Limited real-time traffic control.

- **Use Cases**: Global traffic distribution, multi-region deployments.

---

## 4. Layer 4 Load Balancing (Transport Layer)

- **Description**: Operates at the **TCP/UDP** level. Routes traffic purely based on IP and port, without inspecting HTTP data.

- **Algorithms**: Round Robin, Least Connections, Source IP Hash.

- **Pros**:
  - Very fast and lightweight.
  - Works for any TCP/UDP protocol (HTTP, SMTP, FTP, etc.).

- **Cons**:
  - No application-level decisions (e.g., can’t route by URL path).

- **Use Cases**: Streaming services, gaming, low-latency network apps.

---

## 5. Layer 7 Load Balancing (Application Layer)

- **Description**: Understands **HTTP/HTTPS** and routes traffic based on content (URL, headers, cookies).

- **Features**:
  - SSL/TLS termination.
  - Caching, compression, and URL-based routing.

- **Pros**:
  - Intelligent routing and better user experience.

- **Cons**:
  - Slightly higher overhead than Layer 4.

- **Use Cases**: Modern web apps, microservices, API gateways.

---

## 6. Global Server Load Balancing (GSLB)

- **Description**: Distributes traffic across **multiple geographic regions** or data centers.

- **How It Works**: Combines DNS and health checks to direct users to the nearest or healthiest region.

- **Pros**:
  - Disaster recovery and high availability worldwide.

- **Cons**:
  - More complex to configure and monitor.

- **Use Cases**: Multi-region SaaS platforms, global e-commerce.

---