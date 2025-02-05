Spring Security JWT Authentication

This project is a Spring Boot application that implements authentication and authorization using Spring Security and JSON Web Tokens (JWT).

Features

User authentication using JWT

Role-based access control

Stateless authentication with security filters

Secure API endpoints

Technologies Used

Spring Boot - Backend framework

Spring Security - Authentication and authorization

JWT (JSON Web Token) - Secure user sessions

PostgreSQL - Database

Hibernate - ORM for database interactions

Installation

Prerequisites

Java 17+

PostgreSQL (or another database)

Maven

Steps

Clone the repository

git clone https://github.com/nourrhibi/spring-security-jwt.git
cd spring-security-jwt

Configure the database

Update application.yml with your PostgreSQL credentials:

spring:
datasource:
url: jdbc:postgresql://localhost:5432/jwt_security
username: postgres
password: your_password
driver-class-name: org.postgresql.Driver

Build the project

mvn clean install

Run the application

mvn spring-boot:run

API Endpoints

Authentication

Register: POST /api/v1/auth/register

Request body:

{
"firstname" : "yourname",
"lastname" : "yourlastname",
"email" : "user@gmail.com",
"password" :"password"
}

Login: POST /api/v1/auth/authenticate

Request body:

{
"email": "user@example.com",
"password": "password"
}

Response:

{
"token": "jwt-token-here"
}

Secured Endpoints

Access secured resource: GET /api/v1/demo-controller

Requires Authorization: Bearer <jwt-token> header

License

This project is licensed under the MIT License.

Author

Nour Rhibi

