<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a472a,100:2d6a4f&height=150&section=header&text=Task%20Manager%20API&fontSize=36&fontColor=ffffff&fontAlignY=40"/>

# ✅ Task Manager — Spring Boot REST API
### Full-Stack Task Management with JWT Authentication

[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://java.com)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)](https://mysql.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> **A production-ready RESTful task management API built with Spring Boot, Spring Data JPA, and MySQL. Features full CRUD operations, user authentication, and clean REST architecture.**

</div>

---

## 📌 Project Overview

A full-stack **Task Management REST API** demonstrating enterprise-grade Java backend development with Spring Boot. Implements clean REST endpoints, database persistence with JPA/Hibernate, and follows SOLID principles throughout.

**Target roles**: Java Developer | Backend Engineer | Full Stack Developer | Spring Boot Developer

---

## ✨ Features

| Feature | Description |
|---------|------------|
| 📋 Full CRUD | Create, Read, Update, Delete tasks via REST endpoints |
| 🔐 Authentication | JWT-based user authentication and authorization |
| 🗃️ Persistence | MySQL database with JPA/Hibernate ORM |
| ✅ Validation | Bean validation with descriptive error responses |
| 📄 API Docs | Swagger/OpenAPI documentation |
| 🏷️ Categories | Task categorization and priority levels |
| 🔍 Filtering | Filter tasks by status, priority, and due date |

---

## 🌐 REST API Endpoints

```
Auth:
POST   /api/auth/register     → Register new user
POST   /api/auth/login        → Login & get JWT token

Tasks:
GET    /api/tasks             → Get all tasks (paginated)
GET    /api/tasks/{id}        → Get task by ID
POST   /api/tasks             → Create new task
PUT    /api/tasks/{id}        → Update task
DELETE /api/tasks/{id}        → Delete task
PATCH  /api/tasks/{id}/done   → Mark task complete
```

---

## 🏗️ Architecture

```
┌─────────────────────────────────────┐
│         REST Client / Frontend       │
└─────────────────┬───────────────────┘
                  │ HTTP/JSON
                  ▼
┌─────────────────────────────────────┐
│     Spring Boot Application          │
│  ┌──────────┐  ┌─────────────────┐  │
│  │Controller│→ │  Service Layer  │  │
│  │ @RestCon │  │  Business Logic │  │
│  └──────────┘  └────────┬────────┘  │
│                          │           │
│                ┌─────────▼────────┐  │
│                │ Repository (JPA) │  │
│                │ Spring Data      │  │
│                └─────────┬────────┘  │
└──────────────────────────┼──────────┘
                           │
                  ┌────────▼────────┐
                  │   MySQL DB      │
                  │   tasks table   │
                  │   users table   │
                  └─────────────────┘
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| Java 17 | Core language |
| Spring Boot 3.x | Application framework |
| Spring Data JPA | Database ORM |
| Spring Security + JWT | Authentication |
| MySQL 8.0 | Relational database |
| Hibernate | ORM implementation |
| Maven | Build tool |
| Swagger/OpenAPI | API documentation |

---

## 🚀 Quick Start

```bash
# 1. Clone repository
git clone https://github.com/ITMohanraj/task-manager-springboot.git
cd task-manager-springboot

# 2. Configure database (src/main/resources/application.properties)
spring.datasource.url=jdbc:mysql://localhost:3306/taskmanager
spring.datasource.username=root
spring.datasource.password=yourpassword

# 3. Create MySQL database
mysql -u root -p -e "CREATE DATABASE taskmanager;"

# 4. Build and run
mvn clean install
mvn spring-boot:run

# 5. Access API docs
open http://localhost:8080/swagger-ui.html
```

---

## 📁 Project Structure

```
task-manager-springboot/
├── src/main/java/com/mohanraj/taskmanager/
│   ├── controller/        # REST Controllers
│   │   ├── TaskController.java
│   │   └── AuthController.java
│   ├── service/           # Business Logic
│   │   └── TaskService.java
│   ├── repository/        # JPA Repositories
│   │   └── TaskRepository.java
│   ├── model/             # Entity Classes
│   │   ├── Task.java
│   │   └── User.java
│   ├── dto/               # Data Transfer Objects
│   └── security/          # JWT Security Config
├── src/main/resources/
│   └── application.properties
├── pom.xml
└── README.md
```

---

## 🔮 Future Enhancements

- [ ] 📧 Email notifications for due tasks
- [ ] 📊 Analytics dashboard (React frontend)
- [ ] 🐳 Docker + Docker Compose setup
- [ ] ☁️ AWS deployment (Elastic Beanstalk)
- [ ] 🧪 Full unit & integration test coverage

---

## 👨‍💻 Author

**Mohanraj Kulanthaivel**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/mohanraj-kulanthaivel)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/ITMohanraj)

---

<div align="center">
⭐ <b>Star this repository if it helped you!</b>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2d6a4f,100:1a472a&height=100&section=footer"/>
</div>