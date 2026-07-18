# IssueFlow - Bug Tracking System Backend

IssueFlow is a backend application built with **Spring Boot** and **Spring Data JPA** to manage software projects, issues, sprints, comments, labels, and users in a Jira-like workflow. This project is currently under development and is being built as a practical learning project to master real-world backend development concepts such as REST APIs, layered architecture, entity relationships, validation, exception handling, pagination, and business logic.

## Project Status

🚧 Under Development

Current focus:
- Layered architecture
- REST API development
- Spring Data JPA entity mapping
- Repository and service layer implementation
- Validation and exception handling

Planned next phases:
- Project and sprint management
- Issue tracking workflow
- Comments and labels
- File attachments
- Authentication and authorization
- Reports and dashboard APIs

## Objective

The main goal of this project is to learn how enterprise backend applications are designed and developed using Spring Boot. Instead of building a basic CRUD project, this application models a real bug and project tracking workflow used by software teams. [web:2][web:10]

## Features

### User Management
- Create user
- Update user
- Delete user
- View user details
- Search users
- Activate or deactivate user

### Project Management
- Create project
- Update project
- Assign manager
- Assign team members
- View active and completed projects

### Sprint Management
- Create sprint
- Update sprint
- Close sprint
- View sprint details
- Move issues to sprint

### Issue Management
- Create issue
- Update issue
- Delete issue
- Assign issue to developer
- Change priority and status
- Filter issues by project, sprint, assignee, and status
- View overdue issues

### Comment Management
- Add comment
- Update comment
- Delete comment
- View all comments for an issue

### Label Management
- Add labels to issues
- Remove labels from issues
- Manage issue categorization

### Attachment Management
- Upload attachment
- Download attachment
- Delete attachment

### Reports and Dashboard
- Total projects
- Total issues
- Open bugs
- Critical bugs
- Sprint progress
- Developer performance
- Project statistics

## Tech Stack

- Java 17
- Spring Boot 3.x
- Spring MVC
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- Bean Validation
- Postman
- Git and GitHub

## Concepts Covered

This project is being used to learn and practice:

- Spring Boot project setup
- Maven dependency management
- REST API design
- Layered architecture
- DTO pattern
- Entity relationships
- One-to-One mapping
- One-to-Many mapping
- Many-to-One mapping
- Many-to-Many mapping
- Derived query methods
- JPQL
- Native queries
- Pagination and sorting
- Global exception handling
- Transactions
- Auditing
- Soft delete
- File upload handling
- Spring Security and JWT (planned)

## Business Modules

The application is designed around the following modules:

- Authentication
- Users
- Roles
- Projects
- Sprints
- Issues
- Comments
- Labels
- Attachments
- Notifications
- Reports
- Dashboard

## Core Entities

- User
- Role
- Project
- Sprint
- Issue
- Comment
- Label
- Attachment
- Notification

## Entity Relationships

- One Role can have many Users
- One Project can have many Sprints
- One Project can have many Issues
- One Sprint can have many Issues
- One User can report many Issues
- One User can be assigned many Issues
- One Issue can have many Comments
- One Issue can have many Attachments
- One Issue can have many Labels
- One Label can belong to many Issues

## Project Structure

```text
issueflow-backend
├── src/main/java/com/example/issueflow
│   ├── controller
│   ├── service
│   │   ├── impl
│   ├── repository
│   ├── entity
│   ├── dto
│   │   ├── request
│   │   ├── response
│   ├── mapper
│   ├── exception
│   ├── config
│   ├── enums
│   ├── specification
│   ├── util
│   └── IssueFlowApplication.java
│
├── src/main/resources
│   ├── application.properties
│   └── data.sql
│
├── pom.xml
└── README.md
```

Spring Boot recommends a clear code structure so that application components are organized and easy to maintain as the project grows. [web:9]

## API Development Plan

### Phase 1
- Project setup
- Spring Boot configuration
- Database configuration
- First test API

### Phase 2
- Role and user module
- Validation
- Exception handling
- DTO implementation

### Phase 3
- Project module
- Sprint module
- Entity relationships

### Phase 4
- Issue module
- Filtering
- Pagination
- Sorting
- JPQL queries

### Phase 5
- Comments, labels, and attachments
- Reports and dashboard

### Phase 6
- Security with Spring Security and JWT
- Role-based authorization
- Testing and Swagger documentation

## Sample APIs

### User APIs
- `POST /api/users`
- `PUT /api/users/{id}`
- `DELETE /api/users/{id}`
- `GET /api/users/{id}`
- `GET /api/users`
- `GET /api/users/search`

### Project APIs
- `POST /api/projects`
- `PUT /api/projects/{id}`
- `GET /api/projects`
- `GET /api/projects/{id}`

### Sprint APIs
- `POST /api/sprints`
- `PUT /api/sprints/{id}`
- `GET /api/sprints`
- `GET /api/sprints/{id}`

### Issue APIs
- `POST /api/issues`
- `PUT /api/issues/{id}`
- `DELETE /api/issues/{id}`
- `GET /api/issues`
- `GET /api/issues/{id}`
- `PATCH /api/issues/{id}/status`
- `PATCH /api/issues/{id}/priority`
- `PATCH /api/issues/{id}/assign`

### Comment APIs
- `POST /api/comments`
- `PUT /api/comments/{id}`
- `DELETE /api/comments/{id}`
- `GET /api/comments/issue/{issueId}`

## Getting Started

### Prerequisites

Make sure you have installed:

- Java 17
- Maven
- MySQL Server
- IntelliJ IDEA or any Java IDE
- Postman
- Git

### Clone the Repository

```bash
git clone https://github.com/your-username/issueflow-backend.git
cd issueflow-backend
```

### Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/issueflow_db
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

### Run the Application

```bash
mvn spring-boot:run
```

By default, the application will start on:

```bash
http://localhost:8080
```

Spring Boot applications are commonly run as stand-alone apps with embedded server support, which makes local development simple. [web:1]

## Learning Outcome

After completing this project, I will be able to:

- Build REST APIs using Spring Boot
- Design layered backend architecture
- Work with JPA entity relationships
- Write repository queries using Spring Data JPA
- Implement validation and exception handling
- Build production-style backend modules
- Understand how enterprise Java applications are structured

## Future Enhancements

- JWT authentication
- Role-based access control
- Email notifications
- Activity history
- Audit logs
- Swagger/OpenAPI documentation
- Docker support
- Unit and integration testing
- Deployment to cloud

## Author

Developed as a hands-on learning project for mastering Spring Boot and Spring Data JPA through a real-world backend application.
