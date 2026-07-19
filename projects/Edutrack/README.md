# 🚀  Full Stack REST API

A **Spring Boot RESTful Web Service** built using **Java**, **Spring Boot**, and **MongoDB** that provides CRUD operations for managing training batches. The application follows a layered architecture consisting of **Controller**, **Service**, **Repository**, and **Entity** layers, demonstrating modern backend development practices.

This project serves as a beginner-friendly backend application showcasing REST API development, dependency injection, MongoDB integration, and Spring Data JPA-style repositories. :contentReference[oaicite:0]{index=0}

---

# ✨ Features

- RESTful API architecture
- CRUD operations
- MongoDB integration
- Spring Boot framework
- Layered architecture
- Dependency Injection
- Spring Data MongoDB Repository
- JSON request/response handling
- HTTP status code handling

---

# 🏗️ System Architecture

```
                 Client
(Postman / Browser / Frontend)
                     │
                     ▼
            REST Controller Layer
                     │
                     ▼
              Service Layer
                     │
                     ▼
          Mongo Repository Layer
                     │
                     ▼
                MongoDB Database
```

---

# 📂 Project Structure

```
FullStack
│
├── Controller
│   ├── BatchEntryController
│   └── HealthCheck
│
├── Entity
│   └── BatchEntry
│
├── Repository
│   └── BatchEntryRepository
│
├── Service
│   └── BatchEntryService
│
└── MarvellousFullStackApplication
```

---

# 🗃 Entity Model

The application manages **Batch Details**.

```java
BatchEntry
-----------
ObjectId id
String   name
int      fees
```

MongoDB Collection

```
BatchDetails
```

---

# 🔥 REST API Endpoints

## Get All Batches

```
GET /batches
```

Response

```json
[
  {
    "id": "...",
    "name": "Java Full Stack",
    "fees": 25000
  }
]
```

---

## Create Batch

```
POST /batches
```

Request

```json
{
  "name": "Java Full Stack",
  "fees": 25000
}
```

Response

```
201 Created
```

---

## Update Batch

```
PUT /batches/id/{id}
```

Request

```json
{
  "name": "Python",
  "fees": 18000
}
```

---

## Delete Batch

```
DELETE /batches/id/{id}
```

Response

```
204 No Content
```

---

# ⚙️ Application Flow

```
Client Request
      │
      ▼
REST Controller
      │
      ▼
Service Layer
      │
      ▼
Mongo Repository
      │
      ▼
MongoDB
      │
      ▼
Response
```

---

# 🛠 Technologies Used

- Java
- Spring Boot
- Spring MVC
- Spring Data MongoDB
- MongoDB
- Maven
- Lombok
- REST API
- JSON

---

# 📚 Spring Boot Concepts Covered

- REST Controllers
- Dependency Injection
- Service Layer
- Repository Layer
- Entity Mapping
- MongoDB Integration
- CRUD Operations
- HTTP Methods
- ResponseEntity
- HTTP Status Codes
- Spring Boot Auto Configuration

---

# 🚀 Getting Started

## Clone Repository

```bash
git clone https://github.com/yourusername/MarvellousFullStack.git
```

---

## Configure MongoDB

Start your local MongoDB server and configure the database connection in:

```
application.properties
```

Example

```properties
spring.data.mongodb.uri=mongodb://localhost:27017/MarvellousDB
```

---

## Run the Project

Using Maven

```bash
mvn spring-boot:run
```

Or run the main class

```
MarvellousFullStackApplication
```

---

# 🧪 API Testing

The REST endpoints can be tested using:

- Postman
- Thunder Client
- cURL
- Any frontend application

Example

```bash
curl -X GET http://localhost:8080/batches
```

---

# 📊 Project Workflow

```
Start Application
       │
       ▼
Spring Boot Starts
       │
       ▼
Connect MongoDB
       │
       ▼
Receive HTTP Request
       │
       ▼
Controller
       │
       ▼
Service
       │
       ▼
Repository
       │
       ▼
MongoDB
       │
       ▼
Return JSON Response
```

---

# 🎯 Learning Outcomes

This project demonstrates:

- Spring Boot Development
- REST API Design
- MongoDB CRUD Operations
- Layered Architecture
- Dependency Injection
- Repository Pattern
- JSON Serialization
- Backend Application Development

---

# 🚀 Future Enhancements

- Input Validation using Bean Validation
- Global Exception Handling
- Swagger/OpenAPI Documentation
- Authentication & Authorization (Spring Security + JWT)
- Pagination and Sorting
- Search APIs
- Logging with SLF4J
- Docker Containerization
- Unit Testing with JUnit & Mockito
- Deployment on AWS or Render
- Frontend Integration using React or Angular

---

# 📈 Advantages

- Clean layered architecture
- Easy to extend and maintain
- RESTful API design
- MongoDB integration
- Beginner-friendly Spring Boot project
- Lightweight backend service

---

# ⚠️ Current Limitations

- No authentication or authorization
- No request validation
- No global exception handling
- HealthCheck controller is currently empty
- No pagination or filtering
- Limited entity fields
- No automated tests
- No API documentation (Swagger)

---

# 👨‍💻 Author

**Sumit Dorle**

Artificial Intelligence & Data Science Engineer

GitHub: https://github.com/sumitdorle95

---

# 📜 License

This project is licensed under the MIT License.

---

⭐ If you found this project useful, consider giving it a star!
