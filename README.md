
# 🏦 TRAVEL-BANK_Docker_v.2.0

This project, TRAVEL-BANK_Docker_v.2.0, is a continuation of TRAVEL-BANK_Microservices_v.1.0, with Docker support added.  
In this version, Dockerfiles have been included for each microservice, enabling containerization and smoother deployment.

![Alt text](https://github.com/vinaysteja2/TRAVEL-BANK_Docker_v.2.0/blob/master/screenshots-v.2.0/Screenshot%20(117).png?raw=true)


You can now build and run each service using Docker:

### 🔧 Build Docker Image
```bash
docker build . -t vinaysteja0231/accounts:v.2.0
```

### ▶️ Run Container (Foreground)
```bash
docker run -p 8080:8080 vinaysteja0231/accounts:v.2.0
```

### ▶️ Run Container (Detached Mode)
```bash
docker run -d -p 8080:8080 vinaysteja0231/accounts:v.2.0
```

Once the containers are up and running, you can access the services via Postman and browser as you would in a local setup.

---

# 🏦 TRAVEL BANK - Microservices Platform

TRAVEL BANK is a Spring Boot-based microservices application designed to simulate a simplified banking platform.  
It consists of three core microservices that handle Accounts, Cards, and Loans functionalities. Each service is built with Spring Boot, Spring Data JPA, H2 database, and includes validations and exception handling for robust and secure development.

## 🧩 Microservices Overview

### 1️⃣ Accounts Service
- Allows customer registration  
- Creates a new bank account during registration  
- Supports full CRUD operations  
- Includes validations and global exception handling  

### 2️⃣ Cards Service
- Enables customers to apply for credit or debit cards  
- Manages card issuance and details  
- Provides create, update, fetch, and delete APIs  

### 3️⃣ Loans Service
- Customers can apply for loans and track loan details  
- Full CRUD functionality for loan records  

## 🛠️ Tech Stack
- ⚙️ Java 17+  
- 🚀 Spring Boot 3.x  
- 📦 Spring Data JPA  
- 💾 H2 In-Memory Database  
- 📘 Swagger (OpenAPI) for API Documentation  
- 🧪 Postman for API Testing  
- ☕ Maven for Dependency Management  

## 📌 Features
- ✅ Microservice architecture  
- ✅ RESTful APIs with full CRUD operations  
- ✅ Bean validations on input data  
- ✅ Global exception handling  
- ✅ In-memory H2 DB for quick testing  
- ✅ Swagger UI for interactive API docs  
- ✅ Postman collection included for easy testing  
- ✅ Docker containerization for deployment  

## 📂 Postman Collection

🧪 You can find the Postman collection in the repository named:  
**TRAVEL-BANK.postman_collection.json**

It contains ready-to-use requests to test all available APIs for Accounts, Cards, and Loans.

## 📸 Swagger UI and H2 Console

- 📘 Swagger UI: [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)  
- 💾 H2 Database Console: [http://localhost:8080/h2-console](http://localhost:8080/h2-console)  

## 📈 Future Enhancements

- 🔄 Add Kafka for inter-service communication  
- 🌐 Integrate with API Gateway and Eureka  
- 📊 Use ELK (Elasticsearch, Logstash, Kibana) for logging and monitoring  
- 🐳 Extend Docker setup for multi-service orchestration  
