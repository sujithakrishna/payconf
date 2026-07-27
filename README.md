# PayConf Backend

## Overview

PayConf Backend is a RESTful API developed using **Java 21** and **Spring Boot 3** to support the PayConf Payment Management System.

The backend provides secure authentication, user management, payment processing, income and expense management, distribution management, reporting, payment verification, audit logging, and email-based password recovery.

This project follows a layered architecture with Spring Security, JWT authentication, Spring Data JPA, and MySQL for secure and scalable backend development.

> **Note:** The frontend application is maintained as a separate project and consumes the REST APIs exposed by this backend.

---

# Features

## Authentication & Security

- JWT Authentication
- Secure Login
- Forgot Password via Email
- BCrypt Password Encryption
- Profile Management
- Spring Security
- Input Validation
- Global Exception Handling

---

## User Management

- Create User
- Update User
- Delete User
- View Users
- Search Users

---

## Payment Management

- Create Payment
- Update Payment
- Delete Payment
- View Payment History
- Payment Status Tracking

---

## Income Management

- Add Income
- Update Income
- Delete Income
- Income History

---

## Expense Management

- Add Expense
- Update Expense
- Delete Expense
- Expense History

---

## Distribution Management

- Create Distribution
- Update Distribution
- Distribution History

---

## Dashboard

- Financial Summary APIs
- Payment Statistics
- Income Summary
- Expense Summary

---

## Reports

- Financial Reports
- Payment Reports
- Report Import
- Report Generation APIs

---

## Payment Verification

- Verify Payments
- Reject Payments
- Verification History

---

## Audit Logs

- User Activity Tracking
- System Audit Logs

---

# Technology Stack

| Category | Technology |
|-----------|------------|
| Language | Java 21 |
| Framework | Spring Boot 3.5 |
| Security | Spring Security + JWT |
| ORM | Spring Data JPA (Hibernate) |
| Database | MySQL |
| Validation | Jakarta Validation |
| Documentation | Swagger / OpenAPI |
| Build Tool | Maven |
| Logging | Spring Boot Logging |
| Monitoring | Spring Boot Actuator |
| Email | Spring Mail |
| Testing | JUnit 5, Mockito, MockMvc, JaCoCo |

---

# System Architecture

```
                Client Application
                       │
                REST API Requests
                       │
              Spring Boot Backend
                       │
        Spring Security (JWT Authentication)
                       │
                Service Layer
                       │
              Repository Layer (JPA)
                       │
                  MySQL Database
```

---

# Project Structure

```
src
├── main
│   ├── java
│   │   └── com.payconf
│   │       ├── config
│   │       ├── controller
│   │       ├── dto
│   │       ├── entity
│   │       ├── exception
│   │       ├── repository
│   │       ├── security
│   │       ├── service
│   │       ├── util
│   │       └── PayconfBackendApplication.java
│   │
│   └── resources
│       ├── application.properties
│       └── static
│
└── test
    └── java
```

---

# Prerequisites

Before running the application, ensure the following software is installed:

- Java JDK 21
- Apache Maven 3.9+
- MySQL Server 8+
- Git

---

# Environment Variables

Configure the following environment variables before running the application.

| Variable | Description |
|----------|-------------|
| DB_URL | MySQL Database URL |
| DB_USERNAME | Database Username |
| DB_PASSWORD | Database Password |
| JWT_SECRET | Secret Key for JWT Authentication |
| MAIL_USERNAME | Gmail Address |
| MAIL_PASSWORD | Gmail App Password |

---

# Database Configuration

Create a MySQL database.

```
payconf_db
```

Update the database credentials in your environment variables or `application.properties`.

---

# Running the Application

## Clone the Repository

```bash
git clone <repository-url>
```

---

## Navigate to the Project

```bash
cd payconf-backend
```

---

## Build the Project

```bash
mvn clean install
```

---

## Run the Application

```bash
mvn spring-boot:run
```

The backend will start on:

```
http://localhost:8080
```

---

# API Documentation

Swagger UI

```
http://localhost:8080/swagger-ui/index.html
```

OpenAPI Specification

```
http://localhost:8080/v3/api-docs
```

---

# Monitoring

Spring Boot Actuator endpoints are enabled.

Available endpoints include:

- Health
- Info
- Metrics

Example:

```
http://localhost:8080/actuator/health
```

---

# Security Features

- JWT Authentication
- Password Encryption using BCrypt
- Spring Security
- Input Validation
- Exception Handling
- Environment Variable Configuration
- Protected REST APIs

---

# Testing

The project includes comprehensive backend testing using:

- JUnit 5
- Mockito
- MockMvc
- JaCoCo

Current Test Coverage:

- **Overall Code Coverage: 82%**

---

# Logging

Application logging is implemented using Spring Boot Logging.

The project also supports:

- Health Monitoring
- Metrics
- Application Information via Actuator

---

# Current Project Status

| Module | Status |
|---------|--------|
| Authentication | ✅ Completed |
| User Management | ✅ Completed |
| Payments | ✅ Completed |
| Income | ✅ Completed |
| Expenses | ✅ Completed |
| Distribution | ✅ Completed |
| Dashboard APIs | ✅ Completed |
| Reports | ✅ Completed |
| Audit Logs | ✅ Completed |
| Payment Verification | ✅ Completed |
| Forgot Password (Email) | ✅ Completed |
| Swagger Documentation | ✅ Completed |
| Logging | ✅ Completed |
| Actuator | ✅ Completed |
| Backend Testing | ✅ Completed |
| Role-Based Authorization | ⏳ Pending (Business Permission Matrix Required) |

---

# Future Enhancements

- Role-Based Authorization (Permission Matrix)
- Docker Support
- CI/CD Pipeline
- Database Migration using Flyway/Liquibase
- Performance Optimization
- Production Monitoring

---

# Version

**Current Version:** 1.0.0

---

# License

This backend application has been developed as part of the PayConf Payment Management System for organizational use.

Unauthorized copying, modification, or distribution without permission is prohibited.
