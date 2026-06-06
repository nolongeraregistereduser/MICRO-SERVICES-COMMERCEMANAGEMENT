# 🛒 E-Commerce Microservices Platform

> **A robust, scalable cloud-native foundation for e-commerce, built with the Spring Cloud ecosystem.**

## 📖 Overview

This repository serves as the architectural foundation for a distributed e-commerce management system. Rather than starting with a monolithic approach, this project is designed from the ground up to be cloud-ready, demonstrating a strong understanding of microservices patterns. 

It implements a centralized configuration, service discovery, an API gateway, and modular service separation, laying the groundwork for highly scalable business APIs.

## 🏗️ Architecture & Modules

The system is built using a multi-module Maven repository, cleanly separating infrastructure from business domains:

### Core Infrastructure
* **/config-server:** Centralized configuration management using Spring Cloud Config.
* **/eureka-server:** Service registry and discovery via Netflix Eureka.
* **/gateway-service:** Central entry point routing requests to downstream microservices using Spring Cloud Gateway WebMVC.

### Business Domains
* **/client-service:** Customer management domain.
* **/product-service:** Catalog and inventory domain.
* **/invoice-service:** Billing and transaction domain (Implements inter-service communication via **OpenFeign**).

### Observability
* **/monitoring:** Infrastructure placeholders for Prometheus and Grafana integration.

## 💻 Technical Stack

| Category | Technology |
| :--- | :--- |
| **Language** | Java 17 |
| **Framework** | Spring Boot 4.0.3 |
| **Cloud Native** | Spring Cloud 2025.1.0 |
| **Service Discovery** | Netflix Eureka |
| **API Gateway** | Spring Cloud Gateway Server WebMVC |
| **Inter-Service Calls**| OpenFeign |
| **Resilience** | Resilience4j Circuit Breaker |
| **Data Access** | Spring Data JPA, MySQL |
| **Observability** | Spring Boot Actuator |
| **Testing** | JUnit 5 (`@SpringBootTest`) |
| **Build Tool** | Maven (Multi-module) |

## ✨ Key Features (Current State)

* **Centralized Configuration:** Services pull their configuration from a
