# 🏋️ AI-Powered Fitness Recommendation Platform

A cloud-native **AI-Powered Fitness Recommendation Platform** built using a **Microservices Architecture**. The application provides personalized fitness recommendations, user management, and activity tracking by leveraging **Spring Boot, Spring Cloud, React, MongoDB, RabbitMQ, and AI services**.

---

## 🚀 Features

- 👤 User Registration & Authentication
- 🏃 Activity Tracking
- 🤖 AI-Based Fitness Recommendations
- 🌐 RESTful APIs
- 🚪 API Gateway
- 🔍 Service Discovery (Eureka)
- ⚙️ Centralized Configuration Server
- 📨 RabbitMQ Messaging
- 📊 MongoDB Database
- 🎨 React Frontend
- ☁️ Cloud-Native Microservices Architecture

---

# 🏗️ System Architecture

```text
                        +----------------------+
                        |    React Frontend    |
                        +----------+-----------+
                                   |
                                   |
                          API Gateway (8080)
                                   |
        -----------------------------------------------------
        |                     |                    |
        |                     |                    |
+---------------+     +---------------+    +---------------+
| User Service  |     |ActivityService|    |  AI Service   |
+---------------+     +---------------+    +---------------+
        |                     |                    |
        -------------------------------
                     |
                RabbitMQ Events
                     |
                 MongoDB Database

         Config Server (8888)
                 |
         Eureka Server (8761)
```

---

# 🛠️ Tech Stack

## Backend

- Java 17
- Spring Boot
- Spring Cloud
- Spring Security
- Spring Cloud Gateway
- Spring Cloud Config
- Eureka Discovery Server
- RabbitMQ
- MongoDB
- Maven

## Frontend

- React 19
- Redux Toolkit
- React Router
- Material UI (MUI)
- Axios
- Vite

## Tools

- Git
- GitHub
- IntelliJ IDEA
- Postman

---

# 📁 Project Structure

```text
ai-powered-fitness-recommendation-platform
│
├── configserver/
├── eureka/
├── gateway/
├── userservice/
├── activityservice/
├── aiservice/
├── fitness-app-frontend/
└── README.md
```

---

# 📦 Microservices

| Service | Description |
|----------|-------------|
| Config Server | Centralized configuration management |
| Eureka Server | Service discovery |
| API Gateway | Single entry point for all APIs |
| User Service | User registration and management |
| Activity Service | Tracks user workouts and activities |
| AI Service | Generates personalized fitness recommendations |
| React Frontend | User interface |

---

# ⚙️ Application Workflow

1. User opens the React application.
2. Requests are sent to the API Gateway.
3. Gateway routes requests to the appropriate microservice.
4. All services register with Eureka Server.
5. Configuration is fetched from Config Server.
6. Activity events are exchanged using RabbitMQ.
7. AI Service analyzes activity data and generates recommendations.
8. MongoDB stores user and activity data.

---

# 🚀 Getting Started

## Clone Repository

```bash
git clone https://github.com/<your-github-username>/ai-powered-fitness-recommendation-platform.git

cd ai-powered-fitness-recommendation-platform
```

---

## Start Microservices

Run the services in the following order:

1. Config Server
2. Eureka Server
3. API Gateway
4. User Service
5. Activity Service
6. AI Service
7. React Frontend

---

## Backend

Run each Spring Boot application.

```bash
mvn spring-boot:run
```

or

```bash
./mvnw spring-boot:run
```

---

## Frontend

```bash
cd fitness-app-frontend

npm install

npm run dev
```

---

# 📡 Default Ports

| Service | Port |
|----------|-----:|
| Config Server | 8888 |
| Eureka Server | 8761 |
| API Gateway | 8080 |
| User Service | Config Managed |
| Activity Service | Config Managed |
| AI Service | Config Managed |
| React Frontend | 5173 |

---

# 📚 REST APIs

## User Service

- Create User
- Get User
- Update User
- Delete User

## Activity Service

- Add Activity
- Get Activity History
- Activity Summary

## AI Service

- Personalized Fitness Recommendation
- AI Health Analysis
- Workout Suggestions

---

# ✨ Key Highlights

- Microservices Architecture
- AI Recommendation Engine
- Event-Driven Communication
- RESTful APIs
- API Gateway Pattern
- Service Discovery
- Centralized Configuration
- Scalable & Modular Design
- Clean Code Structure

---

# 🔮 Future Enhancements

- JWT Authentication
- Docker Support
- Docker Compose
- Kubernetes Deployment
- CI/CD Pipeline
- Swagger/OpenAPI Documentation
- Prometheus & Grafana Monitoring
- Notification Service
- Diet Recommendation Engine
- Workout Planner

---

# 👨‍💻 Author

**Vishal Mate**

Java Backend Developer | Spring Boot | Microservices | React | Cloud | AI Applications

---

# ⭐ Support

If you like this project, consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and supports future development.
