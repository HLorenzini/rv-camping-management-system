# 🏕️ RV Camping Management System

A Java-based desktop application designed to manage RV camping operations, including user applications, RV inspections, document management, maintenance requests, and administrative approval workflows.

This project simulates a real-world system and was built to demonstrate backend architecture, business rules, security, and desktop application development using Java.

---

## 📌 Project Overview

The RV Camping Management System allows users to apply for short-term or long-term stays at an RV campground.  
Applications may require document submission and, for older RVs, a photo-based inspection process reviewed by campground managers.

The system also supports maintenance requests and provides a management area for staff to review, approve, or reject applications and inspections.

---

## 👥 User Roles

### User
- Register and log in
- Submit camping applications
- Upload documents and RV photos
- Track application and inspection status
- Create maintenance requests

### Manager / Admin
- Review and manage user applications
- Approve or reject RV inspections
- Access user documents
- Manage maintenance requests
- View system dashboards

---

## ⚙️ Main Features

- User authentication with role-based access control
- Secure login using JWT
- Camping application workflow with status tracking
- RV inspection required for older vehicles
- Document and file upload management
- Maintenance request system
- Manager and admin dashboard
- Desktop application interface built with JavaFX

---

## 🧠 Business Rules

- Each user can only access their own data
- Applications cannot be edited after submission
- RVs older than a defined year require inspection
- Applications can only be approved if all required documents and inspections are completed
- Only managers/admins can approve or reject applications and inspections

---

## 🛠️ Technologies Used

### Backend
- Java
- Spring Boot
- Spring Security
- Spring Data JPA (Hibernate)
- JWT Authentication
- H2 Database (development)
- PostgreSQL or MySQL (production-ready)

### Desktop Application
- JavaFX
- REST API consumption
- Token-based authentication

### Tools & Practices
- Maven
- RESTful API design
- DTO pattern
- Layered architecture
- Unit testing with JUnit
- Git & GitHub

---

## 🧱 Project Architecture

The project follows a layered architecture:

- Controller: REST endpoints
- Service: Business logic
- Repository: Data access
- Entity: Database models
- DTO: Data transfer objects

The desktop application communicates with the backend via REST APIs using HTTP and JWT tokens.

---

## 🗂️ Database Model (High Level)

Main entities:
- User
- Role
- Application
- RV
- Inspection
- Document
- MaintenanceRequest

Relationships:
- User → Applications (1:N)
- Application → RV (1:1)
- RV → Inspection (1:1)
- Application → Documents (1:N)
- User → MaintenanceRequests (1:N)

---

## 🚀 Getting Started

### Prerequisites
- Java 17+
- Maven
- Git

---

## Backend Setup

```bash
git clone https://github.com/your-username/rv-camping-management-system.git
cd backend
mvn spring-boot:run
```
---


## Desktop Application Setup
```bash
cd desktop
mvn clean javafx:run
```
---

## 🔐 Security
- Passwords are encrypted using BCrypt
- Authentication via JWT
- Role-based authorization for all endpoints
- File upload validation (type and size)
- Access control enforced on backend and frontend

---

## 🧪 Testing
- Unit tests for service layer
- Repository tests
- Authentication and authorization tests
- Business rule validation tests

---

## 📈 Project Roadmap
This project was developed using:
- GitHub Issues
- Milestones
- Epics

Each feature was broken down into small, trackable tasks to simulate a real development workflow.

---

## 📄 Documentation
- System requirements
- Business rules
- Diagrams (Use Case, Class, ER)
- API documentation

All documentation can be found in the /docs folder.

---

## 🎯 Purpose of This Project
This project was built for learning and portfolio purposes, with a focus on:
- Backend development with Java
- Clean architecture and business rules
- Desktop application development
- Security and authentication
- Real-world problem solving

---

## 👩‍💻 Author - Heloísa Lorenzini
- Software Engineering Student
- Aspiring Java Developer

## 📬 Contact
- GitHub: https://github.com/your-username
- LinkedIn: https://linkedin.com/in/your-profile
