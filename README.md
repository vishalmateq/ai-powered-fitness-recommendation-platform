# Fitness Microservices Application

A fitness Activity & AI Recommendation application built using **Spring Boot microservices** and **React.js**.

## Tech Stack

- Java
- Spring Boot
- Spring Cloud
- MySQL
- MongoDB
- Apache Kafka
- Eureka Service Discovery
- API Gateway
- Spring WebFlux
- React / Frontend
- Maven

## Microservices

- **User Service** – Manages user information.
- **Activity Service** – Manages fitness activities.
- **AI Service** – Generates fitness recommendations using AI.
- **Eureka Server** – Service discovery.
- **Config Server** – Centralized configuration.
- **API Gateway** – Entry point for microservices.
- **Fitness Frontend** – User interface for the application.

## Architecture

```text
Frontend
   |
   v
API Gateway
   |
   +------------------+
   |        |         |
   v        v         v
User     Activity    AI Service
Service   Service
              |        |
              +--------+-------> Kafka
                       |
                    MongoDB

Eureka Server
      |
Service Discovery

Config Server
      |
Centralized Configuration
```

## Prerequisites

Make sure the following are installed:

- Java 17
- Maven
- MySQL
- MongoDB
- Kafka
- Node.js (for frontend)

# Activity & AI Recommendation Flow

1. **User Creation**

   * The user is first created and stored in the **User Database**.
   * A unique **User ID** is generated and used for subsequent operations.

2. **Activity Creation**

   * When an activity is created, the **Activity Service** receives the request along with the User ID.
   * The service validates whether the **User ID exists and belongs to a valid user**.

3. **Store Activity**

   * After successful validation, the Activity Service stores the activity details in the **Activity Database**.

4. **Publish Event to Kafka**

   * Once the activity is successfully stored, the Activity Service publishes an **Activity Created event** to a **Kafka topic**.
   * The event contains the required activity details and User ID.

5. **AI Microservice Consumes Event**

   * The **AI Microservice** listens to the Kafka topic.
   * When an Activity Created event is received, it processes the activity details.

6. **Gemini API Integration**

   * The AI Microservice prepares a **prompt using the activity details** and sends it to the **Gemini API**.
   * Gemini analyzes the activity information and generates a **recommendation**.

7. **Process & Store Recommendation**

   * The AI Microservice receives the recommendation from Gemini.
   * It processes/validates the response according to the application's requirements.
   * Finally, the recommendation is stored in the **Recommendation Database**.


## How to Run

Clone the repository:

```bash
git clone <repository-url>
cd fitness-micro-hindi-main
```

Start the infrastructure services first:

1. Config Server
2. Eureka Server
3. User Service
4. Activity Service
5. AI Service
6. API Gateway
7. Frontend

For each Spring Boot service:

```bash
mvn spring-boot:run
```

For the frontend:

```bash
npm install
npm start
```


## Features

- User management
- Fitness activity tracking
- AI-based fitness recommendations
- Microservice-to-microservice communication
- Kafka-based messaging
- Service discovery using Eureka
- Centralized configuration
- API Gateway

## Project Structure

```text
fitness-micro-hindi-main/
├── activityservice/
├── aiservice/
├── configserver/
├── eureka/
├── gateway/
├── userservice/
└── fitness-frontend/
