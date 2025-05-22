🏦 TRAVEL-BANK_Docker_v.2.0
TRAVEL-BANK_Docker_v.2.0 is a continuation of the TRAVEL-BANK_Microservices_v.1.0 project, now enhanced with Docker support.
This version introduces Dockerfiles for each microservice, enabling easy containerization and deployment.

🐳 Docker Setup
You can build and run each service using Docker:

bash
Copy
Edit
# 🔧 Build Docker Image
docker build . -t vinaysteja0231/accounts:v.2.0

# ▶️ Run Container (Foreground)
docker run -p 8080:8080 vinaysteja0231/accounts:v.2.0

# ▶️ Run Container (Detached Mode)
docker run -d -p 8080:8080 vinaysteja0231/accounts:v.2.0
Once the containers are running, access the services via Postman or your web browser, just like in a local setup.

🧾 Project Overview
TRAVEL BANK is a Spring Boot-based microservices application that simulates a simplified banking platform.
It contains three independently developed and deployed services:

🧩 Microservices Overview
1️⃣ Accounts Service
Customer registration

Automatically creates a bank account

Supports full CRUD operations

Includes validations and global exception handling

2️⃣ Cards Service
Apply for credit or debit cards

Manage card details and lifecycle

Provides create, update, fetch, and delete APIs

3️⃣ Loans Service
Customers can apply for loans and view loan details

Full CRUD functionality for loan records

🛠️ Tech Stack
⚙️ Java 17+

🚀 Spring Boot 3.x

📦 Spring Data JPA

💾 H2 In-Memory Database

📘 Swagger (OpenAPI) for API Documentation

🧪 Postman for API Testing

☕ Maven for Dependency Management

🐳 Docker for Containerization

📌 Key Features
✅ Microservice architecture

✅ RESTful APIs with full CRUD

✅ Bean validations

✅ Global exception handling

✅ In-memory H2 DB for development

✅ Swagger UI for API documentation

✅ Postman collection for testing

✅ Docker support for deployment

📂 Postman Collection
You can find the Postman collection in the repository:
TRAVEL-BANK.postman_collection.json
It contains ready-made requests to test all APIs for Accounts, Cards, and Loans.

📸 API Access
Swagger UI:
http://localhost:8080/swagger-ui/index.html

H2 Console:
http://localhost:8080/h2-console

📈 Future Enhancements
🔄 Integrate Kafka for inter-service communication

🌐 Add API Gateway and Eureka Service Registry

📊 Implement ELK Stack for logging and monitoring

🐳 Expand to multi-service Docker orchestration (e.g., Docker Compose / Kubernetes)

Let me know if you'd like this formatted as a downloadable README.md file or if you'd like to add screenshots or architecture diagrams.
