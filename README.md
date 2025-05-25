
# 🏦 Travel Bank – Config Management (v3)

This repository is dedicated to **configuration management** for the `Travel Bank` microservices application. It is designed to support scalable, cloud-native architecture using **Spring Boot configuration best practices**.

---

## 📌 Project Continuity

This repository continues from:
- `TRAVEL-BANK_Microservices_v.1.0`
- `TRAVEL-BANK_Docker_v.2.0`

The current version, **`v3.0`**, focuses on **centralized configuration management**, making the services more maintainable and scalable.

---

## 🧰 Configuration Management in Spring Boot

Spring Boot supports multiple ways to read application properties. Here’s a breakdown of the most commonly used approaches:

### 1️⃣ Using `@Value`
Inject individual property values directly into Spring Beans.
```java
@Value("${property.name}")
private String propertyValue;
```

### 2️⃣ Using `Environment`
Use the Environment interface to programmatically fetch property values.
```java
@Autowired
private Environment environment;

public void getProperty() {
    String propertyValue = environment.getProperty("property.name");
}
```

### 3️⃣ Using `@ConfigurationProperties` ✅ *Recommended*
Bind groups of related properties to a POJO class.
```java
@ConfigurationProperties(prefix = "prefix")
public class MyConfig {
    private String property;
    // getters and setters
}
```

This avoids hardcoding keys and improves maintainability.

---

## 🐳 Docker Support (From v2.0)

Each microservice in the Travel Bank ecosystem is fully containerized using Docker.

### 🔧 Docker Compose
```bash
# Start all services
docker compose up -d

# Stop all services
docker compose down
```

### 🔧 Build Docker Images

| Method         | Command                                         |
|----------------|--------------------------------------------------|
| Google Jib     | mvn compile jib:dockerBuild                    |
| Buildpacks     | mvn spring-boot:build-image                    |
| Dockerfile     | docker build . -t <image-name>:<tag>           |

### ▶️ Run Docker Containers
```bash
# Foreground
docker run -p 8080:8080 vinaysteja0231/accounts:v2.0

# Detached
docker run -d -p 8080:8080 vinaysteja0231/accounts:v2.0
```

---

## 🧩 Travel Bank - Microservices Overview

A microservices-based banking platform built with Spring Boot.

### ✅ Core Services

| Service   | Features |
|-----------|----------|
| **Accounts** | Customer registration, account creation, validations, exception handling |
| **Cards** | Card issuance, CRUD for cards |
| **Loans** | Loan application, tracking, CRUD operations |

---

## 🛠️ Tech Stack

- Java 17+
- Spring Boot 3.x
- Spring Data JPA
- H2 Database
- Swagger (OpenAPI)
- Docker + Buildpacks + Jib
- Maven
- Postman

---

## 🔍 API Testing & Docs

- 📘 **Swagger UI**: http://localhost:8080/swagger-ui/index.html  
- 💾 **H2 Console**: http://localhost:8080/h2-console

---

## 🧪 Postman Collection

A ready-to-use Postman collection is available here:

📂 **File**: `TRAVEL-BANK.postman_collection.json`  
🔹 Test all microservices from one place

---

## 📈 Future Enhancements

- 📡 Integrate Kafka for event-driven architecture
- 🧭 API Gateway + Eureka Discovery
- 📊 Logging & Monitoring with ELK Stack
- 🐳 Docker Compose for full service orchestration

---

## 📚 Related Repositories

- `travelbank-microservices`
- `travelbank-docker`

---

## 🙌 Contribution

Feel free to fork, raise issues, or submit pull requests. Feedback and improvements are always welcome!

---

## 📜 License

This project is licensed under the MIT License.
