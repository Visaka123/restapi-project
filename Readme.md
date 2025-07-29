Online News Portal (Backend)

## Overview

The **Online News Portal** is a backend application developed using **Spring Boot**. It provides RESTful APIs to manage news articles, users, roles, categories, comments, and advertisements. This project offers a robust, scalable backend to support real-time news posting and user interactions in a digital news platform.

---

## Key Features

- CRUD operations for articles, categories, and advertisements
- Role-based access control for Admins and Users
- User registration and login functionality
- Commenting on articles
- Categorization and filtering of news content
- Swagger integration for API testing and documentation

---

##  Tech Stack

| Component          | Technology                          |
|-------------------|-------------------------------------|
| Backend Framework | Spring Boot (Spring Tool Suite)     |
| Database          | MySQL                               |
| API Documentation | Swagger                             |
| Hosting           | (Optional) AWS / Google Cloud / Azure |

---

##  Modules & Entities

### 1. **Authentication & User Management**
- **Login**: Handles authentication.
- **User**: Stores user details like name, mobile number, email, and address.
- **Roles**: Defines Admin and User roles.
- **Permission**: Assigns access levels to roles.

### 2. **News & Content Management**
- **News**: Stores articles with type, description, and metadata.
- **Latest Post**: Highlights recently added articles.
- **Contents**: Stores various media contents linked to articles.

### 3. **User Interaction**
- **Comment**: Allows users to comment and edit on articles.

### 4. **Admin Functionalities**
- **Admin**: Can manage users, articles, and advertisements.
- **Advertisement**: Stores ads with title, description, type, and date.

### 5. **Structure & Categorization**
- **NewsPortal**: Manages system structure and news categories.
- **Category**: Organizes articles under specific categories.

---

## How to Run the Project

### Prerequisites
- Java 17
- Spring Boot
- MySQL
- Maven
  ##  Configure MySQL

1. **Create a database** named: `news_portal`.

2. **Update `application.properties`:**

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/news_portal
spring.datasource.username=root
spring.datasource.password=yourpassword

###Run the application:

./mvnw spring-boot:run

Access Swagger API Docs:
http://localhost:8080/swagger-ui/

 ##User Roles:
Role	Permissions

Admin-	Create, update, delete articles, manage users & ads
User-	View articles, post comments, edit profile

Sample API Endpoints:
Method	Endpoint	Description
GET	/api/news	List all news articles
POST	/api/news	Create a new article
GET	/api/users	List all users (Admin only)
POST	/api/comments	Add a comment to an article
GET	/api/categories	View all categories

