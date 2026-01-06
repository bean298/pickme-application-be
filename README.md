# 🍽 PickMe – Backend 

Backend API for **PickMe – Pre-order, Pick Up, Go!**

A food pre-ordering system that allows users to order in advance and pick up directly at the restaurant.

Built with **Spring Boot**, **PostgreSQL** + **PostGIS**, and **RESTful APIs**, supporting authentication, ordering, location-based features, and system management.

This system supports:
- User authentication and role-based access control (Admin, Customer, Restaurant Owner)
- Restaurant and menu management
- Food pre-ordering with pickup time selection
- Order management and processing
- Location-based services (PostGIS integration)
- Route-based restaurant recommendations
- Customer address management
- Feedback and rating system
- System administration and user management

---

## 🚀 Tech Stack

- Java 17
- Spring Boot 3
- Spring Security + JWT
- PostgreSQL 12+
- PostGIS (Geolocation)
- JPA (Hibernate)
- REST API
- Swagger UI
- Java Mail Sender
- Maven

---

## 🧩 Main Features

### 👤 Customer
- Register & login
- View restaurants and menus
- Pre-order food and select pickup time
- View directions to restaurants
- Get restaurant recommendations along the route
- Place and pay for orders
- Manage delivery/pickup addresses (PostGIS)
- Submit feedback after purchase

### 🧑‍🍳 Restaurant Owner
- Manage restaurant profile
- Manage restaurant location and menu
- Receive and process pre-orders
- Track customer orders

### 🧑‍💼 Admin
- Manage all users
- Manage restaurants, campaigns, and promotions
- Monitor system activities
- Activate / deactivate users and manage roles

---

## 🗄 Database

- PostgreSQL + PostGIS  
- Database name: `pickmeapplication`

Supports:
- Geolocation storage (latitude / longitude)
- Nearby search
- Route-based restaurant recommendations

---

## ⚙️ Installation & Run

### 1. Clone the repository

```bash
git clone <backend-repo-url>
```

### 2. Database Setup

2.1: Neon PostgreSQL (Cloud)
- Register at ``` https://neon.tech ```
- Create a new project
- Copy the connection string from the dashboard

Update Neon configuration:
```bash
NEON_DATABASE_URL=jdbc:postgresql://ep-your-endpoint.neon.tech/neondb?sslmode=require
NEON_DB_USERNAME=your-username
NEON_DB_PASSWORD=your-password
```
### 3.Environment Variables

Create a `.env` file at the root of the project:

```bash
copy .env.example .env
```

Update the environment variables:

```bash
# Database (Neon / Local PostgreSQL)
DB_PASSWORD=your_database_password

# JWT Configuration
JWT_SECRET=your_strong_secret_key_at_least_32_characters
JWT_EXPIRATION=86400000

# Email Configuration (Gmail SMTP)
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-16-digit-app-password
MAIL_FROM=your-email@gmail.com

# Application
APP_BASE_URL=http://localhost:8080
APP_ENV=development

# Server
SERVER_ADDRESS=0.0.0.0
SERVER_PORT=8080
```

### 4. Run backend

```bash
mvn spring-boot:run 
```

Server will start at:

```bash
http://localhost:8080
```

---

## 🧪 API Documentation

Swagger UI:

```bash
http://localhost:8080/swagger-ui/index.html
```

<img width="1919" height="870" alt="Screenshot 2026-01-06 160756" src="https://github.com/user-attachments/assets/23a5950e-8c6b-4150-9777-eaf44d7f0fd3" />







