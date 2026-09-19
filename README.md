# Fitness Microservices Application

A simple fitness application built using **Spring Boot microservices** and a frontend application.

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

- Java 24
- Maven
- MongoDB
- Kafka
- Node.js (for frontend)

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

## Configuration

Update the application configuration files with your local:

- MongoDB connection
- Kafka configuration
- Service ports
- Config Server URL
- Eureka Server URL
- AI/API credentials, if required

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
