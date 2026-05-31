# Task Management API Project

## Overview

This project is a Spring Boot REST API developed as part of a coding challenge. It provides CRUD operations for managing tasks, including task creation, retrieval, update, deletion, filtering, and pagination.

API documentation is available through Swagger UI, which can be used to explore and test all available endpoints.

Swagger Documentation
http://localhost:8080/swagger-ui.html
## Technologies Used

* Java 17
* Spring Boot
* Spring Data JPA
* H2 In-Memory Database
* Swagger OpenAPI
* Maven
* JUnit 5
* Mockito

## Prerequisites

Before running the application, ensure the following are installed:

* Java 17 or later
* Maven 3.8+
* Git (optional)

## Build the Project

```bash
mvn clean install
```

## Run the Application

```bash
mvn spring-boot:run
```

The application will start on:

```text
http://localhost:8080
```

## Swagger Documentation

```text
http://localhost:8080/swagger-ui.html
```

## H2 Database Configuration

```text
JDBC URL : jdbc:h2:mem:taskdb
Username : sa
Password :
```

## API Endpoints

### Create Task

```http
POST /tasks
```

### Get Task By Id

```http
GET /tasks/{id}
```

### Update Task

```http
PUT /tasks/{id}
```

### Delete Task

```http
DELETE /tasks/{id}
```

### List Tasks

```http
GET /tasks?page=0&size=10
```

Optional filter:

```http
GET /tasks?status=PENDING
```

## Running Tests

```bash
mvn test
```

## Assumptions

* Task ID is generated using UUID.
* Due date is mandatory.
* Title is mandatory.
* Default task status is PENDING.
* Tasks are sorted by due date.

## Author

Nagesh
