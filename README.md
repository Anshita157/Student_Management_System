# 🎓 Student Management System

A simple full-stack **Student CRUD** web application built with **Spring Boot** and **Thymeleaf**. It allows you to add, view, update, and delete student records through a web interface.

---

### 🌐 Live Demo: studentmanagementsystem-production-5962.up.railway.app

---

## 🚀 Features

- ✅ Add new students
- ✅ View list of all students
- ✅ Edit student details
- ✅ Delete students
- ✅ In-memory database (H2) for quick setup

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Spring Boot 4.0.3 |
| Frontend | Thymeleaf |
| Database | H2 (in-memory) / MySQL |
| ORM | Spring Data JPA (Hibernate) |
| Build Tool | Maven |
| Java Version | Java 17 |
| Utilities | Lombok |

---

## 📁 Project Structure

```
src/
└── main/
    ├── java/com/student/crud/
    │   ├── CrudApplication.java        # Main entry point
    │   ├── controller/
    │   │   └── StudentController.java  # Handles HTTP routes
    │   ├── entity/
    │   │   └── Student.java            # Student data model
    │   └── repository/
    │       └── StudentRepository.java  # JPA repository
    └── resources/
        ├── templates/                  # Thymeleaf HTML views
        └── application.properties     # App configuration
```

---

## 📋 Student Fields

| Field | Type | Description |
|---|---|---|
| `id` | Long | Auto-generated unique ID |
| `name` | String | Student's full name |
| `studentGroup` | String | Group/Section of the student |
| `course` | String | Course enrolled in |
| `age` | Integer | Student's age |

---

## ⚙️ Getting Started

### Prerequisites

- Java 17+
- Maven 3.6+
- MySQL 8.0+ (create a database named `student_db`)

### Run the Application

```bash
# Clone the repository
git clone https://github.com/Anshita157/Student_Management_System.git
cd Student_Management_System

# Run with Maven
./mvnw spring-boot:run
```

The app will start at **http://localhost:8086**

### Access the App

| Page | URL |
|---|---|
| Student List | http://localhost:8086/students/list |
| Add Student | http://localhost:8086/students/signup |

---

## 🗄️ Database Setup

This app uses **MySQL**. Before running, create the database:

```sql
CREATE DATABASE student_db;
```

Then update `src/main/resources/application.properties` with your MySQL credentials:

```properties
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

## 📝 API Endpoints (Web Routes)

| Method | URL | Description |
|---|---|---|
| GET | `/students/list` | View all students |
| GET | `/students/signup` | Show add student form |
| POST | `/students/add` | Save new student |
| GET | `/students/edit/{id}` | Show edit form |
| POST | `/students/update/{id}` | Update student |
| GET | `/students/delete/{id}` | Delete student |

---

## 👩‍💻 Author

**Anshita** — [GitHub](https://github.com/Anshita157)
