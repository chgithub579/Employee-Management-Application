📌 Employee Management System (Full-Stack)

A Full-Stack Employee Management Application with Spring Boot (backend) and React (frontend).
This project provides CRUD operations to manage employees including Name, Username, Email, and Mobile Number.

🚀 Features

Add, update, delete, and view employees

Store details like:

Name

Username

Email

Mobile Number

REST API powered by Spring Boot

Responsive frontend with React

Integrated backend + frontend for smooth workflow

🛠 Tech Stack
Backend

Java 17+

Spring Boot

Spring Data JPA (Hibernate)

MySQL / PostgreSQL

Maven

Frontend

React

JavaScript (ES6+)

Bootstrap / Tailwind (optional)

Axios for API calls

⚙️ Setup & Installation
Backend Setup

Clone the repo and go to backend folder:

cd backend


Configure database in src/main/resources/application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/employeesdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update


Run the backend:

mvn spring-boot:run


Backend runs at:

http://localhost:8080

Frontend Setup

Go to frontend folder:

cd frontend


Install dependencies:

npm install


Start the frontend:

npm start


Access the app in browser:

http://localhost:3000

📡 API Endpoints (Backend)
Method	Endpoint	Description
GET	/employees	Get all employees
GET	/employees/{id}	Get employee by ID
POST	/employees	Create a new employee
PUT	/employees/{id}	Update employee by ID
DELETE	/employees/{id}	Delete employee by ID
📷 Example Request (Create Employee)
{
  "username": "john123",
  "email": "john@example.com",
  "mobileNumber": "9876543210"
}

📌 Future Enhancements

Add role & department management

Employee search & filter options

Authentication & authorization (JWT, Spring Security)

Pagination & sorting in API

Dockerize for easy deployment
