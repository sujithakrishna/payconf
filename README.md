# PayConf 2.0 Backend

A secure and scalable RESTful backend for the **PayConf 2.0 Payment Management System**, developed using **Java 21**, **Spring Boot**, and **MySQL**.

The backend provides REST APIs for authentication, payment management, UTR verification, financial tracking, report generation, audit logging, and role-based access control. It is designed to integrate seamlessly with the React.js frontend.

---

# Project Overview

PayConf 2.0 is a centralized Payment Management System developed to streamline the management of student payments and organizational financial operations.

The backend exposes REST APIs that enable secure authentication, payment verification, income and expense management, report generation, share distribution, and audit logging while maintaining data integrity through role-based authorization.

---

# Key Features

## Authentication & Security

- Secure Login
- JWT Authentication
- Role-Based Authorization
- Password Encryption (BCrypt)
- Forgot Password (Email Recovery)
- Spring Security
- Global Exception Handling
- Input Validation

---

## User Management

- Create User
- Update User
- Delete User
- View Users
- Search Users

---

## Payment Management

- Import Payment Records
- View Payment Logs
- Search Payments
- Track Payment Status
- Update Payment Information

---

## UTR Verification

- Verify Payments
- Reject Payments
- Update Verification Status
- Verification Workflow Support

---

## Income Management

- Add Income
- Edit Income
- Delete Income
- Monthly Income Tracking

---

## Expense Management

- Add Expenses
- Edit Expenses
- Delete Expenses
- Expense Tracking

---

## Share & Profit Distribution

- Monthly Operational Profit Calculation
- Employee Salary Adjustment
- Investment Share Deduction
- Backup Fund Allocation
- Founder Share Distribution

---

## Reports

- Generate Financial Reports
- Generate Payment Reports
- Export Reports
- Archive Reports

---

## Audit Logs

- User Activity Tracking
- Financial Activity Logs
- Verification Logs
- Report Generation Logs

---

# Technology Stack

| Component | Technology |
|------------|------------|
| Language | Java 21 |
| Framework | Spring Boot 3.x |
| Security | Spring Security + JWT |
| ORM | Spring Data JPA (Hibernate) |
| Database | MySQL |
| Validation | Jakarta Validation |
| Build Tool | Maven |
| Email | Spring Mail |

---

# System Architecture

```
                    React Frontend
                           │
                    REST API Requests
                           │
                 Spring Boot Backend
                           │
                 Spring Security (JWT)
                           │
                    Service Layer
                           │
                  Repository Layer
                           │
                       MySQL Database
```

---

# Backend Modules

```
Authentication
│
├── Login
├── Forgot Password
└── User Management

Payments
│
├── Payment Records
├── UTR Verification
└── Payment Tracking

Finance
│
├── Income
├── Expenses
└── Share Distribution

Reports
│
├── Generate Reports
├── Existing Reports
└── Audit Logs
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
│   │       └── util
│   │
│   └── resources
│       ├── application.properties
│       └── static
│
└── test
```

---

# Prerequisites

Install the following before running the project:

- Java JDK 21
- Apache Maven
- MySQL Server 8+
- Git

---

# Database Setup

Create a MySQL database.

```
payconf_db
```

Update your database configuration in:

```
application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/payconf_db
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

# Running the Application

Clone the repository

```bash
git clone <repository-url>
```

Navigate to the backend

```bash
cd payconf-backend
```

Build

```bash
mvn clean install
```

Run

```bash
mvn spring-boot:run
```

Backend URL

```
http://localhost:8080
```

---

# Frontend Integration

The backend is integrated with an existing React.js frontend.

Communication between frontend and backend is handled using REST APIs for:

- Authentication
- Payment Management
- Income Management
- Expense Management
- UTR Verification
- Share Distribution
- Report Generation
- Audit Logs

---

# Security

The application includes:

- JWT Authentication
- Role-Based Authorization
- BCrypt Password Encryption
- Spring Security
- Request Validation
- Exception Handling

---

# Current Project Status

| Module | Status |
|---------|--------|
| Authentication | ✅ Completed |
| User Management | ✅ Completed |
| Payment Management | ✅ Completed |
| UTR Verification | ✅ Completed |
| Income Management | ✅ Completed |
| Expense Management | ✅ Completed |
| Share Distribution | ✅ Completed |
| Report Generation | ✅ Completed |
| Existing Reports | ✅ Completed |
| Audit Logs | ✅ Completed |
| Backend Integration | ✅ Completed |
| Testing | ✅ Completed |
| Email Notifications | ⏳ Pending SMTP Configuration |

---

# Known Limitations

- SMTP sender email credentials are pending from the organization.
- Confirmation is pending regarding ADMIN_VIEW permission for payment import.
- Payment verification history workflow requires business confirmation.
- Imported payment timestamp behavior requires business confirmation.

---

# Contribution

This backend was developed using Spring Boot and MySQL.

The work included:

- Backend Architecture Design
- REST API Development
- Database Integration
- Spring Security Configuration
- JWT Authentication
- Role-Based Authorization
- Business Logic Implementation
- Backend Integration with the Existing React Frontend
- Functional Testing
- End-to-End Testing
- Deployment Preparation

---

# Future Enhancements

- Docker Support
- CI/CD Pipeline
- Cloud Deployment
- Advanced Dashboard Analytics
- Automated Database Backup
- Performance Optimization
- Enhanced Notification System

---

# Version

**PayConf 2.0 Backend**

**Version:** 1.0 RC1

---

# License

Developed for the PayConf 2.0 Payment Management System.

This repository is intended for organizational use. Unauthorized copying, modification, or distribution without permission is prohibited.
