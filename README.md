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
