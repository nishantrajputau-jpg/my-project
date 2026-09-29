# Student Management System

A console-based **Student Management System** developed using **Java, MySQL, JDBC, and Maven**.

The project provides basic CRUD operations for managing student records.

## Features

- Add student
- View all students
- Search student by ID
- Update student details
- Delete student
- MySQL database integration using JDBC
- PreparedStatement for database operations
- Maven dependency management

## Technologies Used

- Java 17+
- MySQL 8+
- JDBC
- Maven
- Git & GitHub

## Project Structure

```text
StudentManagementSystem/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/studentmanagement/
│   │   │       ├── DBConnection.java
│   │   │       ├── Student.java
│   │   │       ├── StudentDAO.java
│   │   │       └── StudentManagementSystem.java
│   │   └── resources/
│   │       └── database.sql
├── screenshots/
│   └── README.md
├── .gitignore
├── pom.xml
└── README.md
```

## Requirements

Install these before running the project:

1. JDK 17 or later
2. MySQL Server
3. Maven
4. IntelliJ IDEA, Eclipse, VS Code, or another Java IDE

## Database Setup

Open MySQL and run:

```sql
CREATE DATABASE IF NOT EXISTS student_db;
USE student_db;

CREATE TABLE IF NOT EXISTS students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    gender VARCHAR(20),
    course VARCHAR(100),
    phone VARCHAR(15),
    email VARCHAR(100)
);
```

You can also run the complete script:

```text
src/main/resources/database.sql
```

## JDBC Configuration

Open:

```text
src/main/java/com/studentmanagement/DBConnection.java
```

Update these values according to your MySQL setup:

```java
private static final String URL =
        "jdbc:mysql://localhost:3306/student_db";
private static final String USER = "root";
private static final String PASSWORD = "YOUR_MYSQL_PASSWORD";
```

**Do not upload your real database password to GitHub.**

For a public repository, use an environment variable or local configuration for credentials.

## Run with Maven

From the project root:

```bash
mvn clean compile
mvn exec:java
```

## Run from an IDE

1. Import the project as a Maven project.
2. Make sure MySQL is running.
3. Create the `student_db` database and `students` table.
4. Update the database password in `DBConnection.java`.
5. Run `StudentManagementSystem.java`.

## Sample Menu

```text
======================================
     STUDENT MANAGEMENT SYSTEM
======================================

----------- MENU -----------
1. Add Student
2. View All Students
3. Search Student
4. Update Student
5. Delete Student
6. Exit
----------------------------
```

## Screenshots

Add your screenshots inside the `screenshots` folder.

Recommended screenshots:

| Screenshot | File |
|---|---|
| Main Menu | `01-main-menu.png` |
| Add Student | `02-add-student.png` |
| View Students | `03-view-students.png` |
| Search Student | `04-search-student.png` |
| Update Student | `05-update-student.png` |
| Delete Student | `06-delete-student.png` |
| MySQL Database | `07-database.png` |

## GitHub Upload

Initialize Git:

```bash
git init
git add .
git commit -m "Initial commit - Student Management System"
```

Create a new repository on GitHub, then connect it:

```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/student-management-system.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

## Resume Description

**Student Management System | Java, MySQL, JDBC**

- Developed a console-based Student Management System using Java and MySQL.
- Implemented CRUD operations including add, search, update, view, and delete.
- Used JDBC and PreparedStatement for secure database connectivity and SQL operations.
- Managed project dependencies using Maven.

## Future Enhancements

- Login and authentication
- Java Swing/JavaFX GUI
- Spring Boot REST API
- Role-based access
- Student attendance module
- Export student data to Excel/PDF

## Author

Nishant Kumar
