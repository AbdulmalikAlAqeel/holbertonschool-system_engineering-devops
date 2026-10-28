# Web Infrastructure Design

This repository contains the projects for the **Web Infrastructure Design** module as part of the Holberton School System Engineering & DevOps track. The goal is to understand, design, and explain web infrastructure architectures ranging from a single server setup to highly available, distributed systems.

---

## Tasks Overview

### 0. Simple Web Stack
- **Objective:** Design and explain a simple one-server web infrastructure hosting a website reachable via `www.foobar.com`.
- **Infrastructure Components:**
  - 1 Domain name (`foobar.com`) with a `www` record pointing to server IP `8.8.8.8`.
  - 1 Server containing:
    - Web Server (Nginx)
    - Application Server
    - Application Files (Codebase)
    - Database (MySQL)
- **Diagram:** [https://imgur.com/kne56D8]


### 1. Distributed Web Infrastructure
- **Objective:** Design and explain a three-server web infrastructure to overcome single-server limitations, featuring a load balancer and distributed nodes.
- **Infrastructure Components:**
  - 1 Load Balancer (HAProxy) distributing incoming traffic.
  - 2 Servers, each containing:
    - Web Server (Nginx)
    - Application Server
    - Application Files (Codebase)
    - Database (MySQL Primary-Replica cluster)

- **Diagram:** [https://imgur.com/0CVNvbq]

### 2. Secured and Monitored Web Infrastructure
- **Objective:** Secure, encrypt, and monitor the three-server web infrastructure.
- **Infrastructure Components:**
  - 3 Firewalls protecting individual servers and the load balancer.
  - 1 SSL Certificate serving `www.foobar.com` over HTTPS.
  - 3 Monitoring Clients (e.g., Sumologic or Datadog agents) collecting metric data on each node.
- **Diagram:** [https://imgur.com/uywxwLU]

### 3. Scale up
- **Objective:** Scale up the architecture by separating components onto their own dedicated servers and adding a second load balancer to eliminate single points of failure at the entry point.
- **Infrastructure Components:**
  - 2 Load Balancers (HAProxy) configured in a cluster (Active-Passive setup).
  - Dedicated Web Servers (Nginx) handling static content and routing.
  - Dedicated Application Servers executing business logic.
  - Dedicated MySQL Primary-Replica database cluster.
- **Key Concepts:**
  - **Web Server vs Application Server:** A web server handles static files and client HTTP requests, whereas an application server executes the backend code and generates dynamic content.
- **Diagram:** [https://imgur.com/YnYciet]
