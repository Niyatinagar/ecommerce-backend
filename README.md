# 🛒 E-Commerce Backend REST API

![Java](https://img.shields.io/badge/Java-17-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-brightgreen)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Hibernate](https://img.shields.io/badge/Hibernate-JPA-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 👩‍💻 Author

**Niyati Nagar**  
Backend Developer | Java | SQL | REST APIs  

---

## 📖 Project Overview

The **E-Commerce Backend REST API** is a full-featured backend application built using **Java, Spring Boot, Spring Data JPA, Hibernate, and MySQL**.

This project simulates a real-world e-commerce platform that manages:

- Customer and Seller authentication  
- Product inventory management  
- Cart operations  
- Order placement and tracking  
- Session-based security  

The application follows a layered architecture and RESTful design principles, ensuring scalability, maintainability, and secure data handling.

---

## 🏗️ Architecture

The project follows a clean layered architecture:

Controller → Service → Repository → Database

- **Controller Layer**: Handles HTTP requests and responses
- **Service Layer**: Contains business logic
- **Repository Layer**: Communicates with MySQL database using JPA
- **Database Layer**: Enforces constraints and relationships

---

## 🚀 Key Features

### 🔐 Authentication & Security
- Separate login & registration for Customers and Sellers
- Session-based authentication
- Secure session token with 1-hour validity
- Token required for protected operations

---

### 👤 Customer Features
- Register & login
- View products
- Add/remove items from cart
- Place orders
- View order history
- Update profile, password, address, and card details
- Delete account

---

### 🏪 Seller Features
- Register & login
- Add, update, delete products
- View customers & orders
- Update profile and credentials

---

### 📦 Product Management
- Add new products
- Update product details
- Update product quantity
- View products by category
- View seller-specific products
- Delete products

---

### 🛒 Cart Management
- Add items to cart
- Remove items
- Clear cart
- View cart contents

---

### 📑 Order Management
- Place order from cart
- View all orders
- View orders by date
- Update pending order
- Cancel order

---

## 🛠️ Tech Stack

- **Backend**: Java 17, Spring Boot
- **Database**: MySQL
- **ORM**: Hibernate, Spring Data JPA
- **Build Tool**: Maven
- **API Testing**: Swagger UI / Postman

---

## 📊 Database Design

The application is based on a structured relational model including:

- Customer
- Seller
- Product
- Cart
- Order
- Session

Foreign keys and constraints ensure data integrity across modules.

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```
git clone https://github.com/YOUR_USERNAME/ecommerce-backend.git
cd ecommerce-backend
```

---

### 2️⃣ Configure Database

Create MySQL database:

```sql
CREATE DATABASE ecommercedb;
```

Update `application.properties`:

```
server.port=8009

spring.datasource.url=jdbc:mysql://localhost:3306/ecommercedb
spring.datasource.username=root
spring.datasource.password=your-password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

### 3️⃣ Run the Application

```
mvn clean install
mvn spring-boot:run
```

API runs at:

```
http://localhost:8009/
```

Swagger UI:

```
http://localhost:8009/swagger-ui/index.html
```

---

## 📌 Example API – Customer Login

**POST** `/login/customer`

Request:

```json
{
  "mobileId": "9999999999",
  "password": "password123"
}
```

Response:

```json
{
  "sessionId": 23,
  "token": "customer_0ad57094",
  "userId": 19,
  "userType": "customer",
  "sessionStartTime": "2024-07-06T10:48:20",
  "sessionEndTime": "2024-07-06T11:48:20"
}
```

---

## 🌟 What This Project Demonstrates

- REST API development using Spring Boot
- CRUD operations with MySQL
- Session-based authentication
- Data validation & integrity
- Clean layered backend architecture
- Enterprise-level module separation

---

## 🎯 Why This Project?

This project reflects my ability to design and implement scalable backend systems suitable for enterprise-grade applications such as e-commerce platforms.

It demonstrates strong understanding of:

- SQL relationships
- Authentication flow
- Business logic handling
- REST API best practices

---

## 📬 Contact

**Niyati Nagar**  
GitHub: https://github.com/Niyatinagar  

---

⭐ If you found this project useful, feel free to star it!