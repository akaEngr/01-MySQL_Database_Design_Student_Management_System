# 01-MySQL_Database_Design_Student_Management_System




# Student Management System

## Project Overview

The Student Management System is a database project built using MySQL.

It stores and manages student information, departments, courses, enrollments, examination sessions, exams, classes, and attendance records.

The main purpose of this project is to practice database design, table relationships, SQL queries, and data management.

## Technologies Used

- MySQL
- SQL
- MySQL Workbench

## Database Name

```sql
Student_Management_System
```

## Requirements

### 1. Departments
- Store department name and description.
- Each department has a unique ID and name.
- One department can have multiple students.
- One department can offer multiple courses.

### 2. Courses
- Store course name, course code, duration, and fees.
- Each course belongs to one department.
- Each course has a unique ID and course code.

### 3. Students
- Store student name, age, address, email, and phone number.
- Each student has a unique ID.
- Email and phone number must be unique.
- Each student belongs to one department.

### 4. Enrollments
- A student can enroll in multiple courses.
- A course can have multiple students.
- A student cannot enroll in the same course twice.

### 5. Examination Sessions
- Store examination year, month, start date, and end date.
- Each examination session has a unique ID.
- The month must be between 1 and 12.
- The end date cannot be earlier than the start date.

### 6. Exams
- Store exam name, exam date, and total marks.
- Each exam belongs to one course.
- Each exam belongs to one examination session.

### 7. Student Exams
- A student can participate in multiple exams.
- An exam can have multiple students.
- Store marks obtained and result status.
- A student cannot have duplicate records for the same exam.

### 8. Classes
- Store class start date and end date.
- Each class belongs to one course.
- A course can have multiple classes.

### 9. Attendance
- Store student attendance for each class.
- Attendance status can be Present, Absent, or Late.
- A student can attend multiple classes.
- A student can have only one attendance record per class.

## Database Tables

| No. | Table Name | Purpose |
|---|---|---|
| 1 | departments | Stores department information |
| 2 | courses | Stores course information |
| 3 | students | Stores student information |
| 4 | enroll | Stores student course enrollments |
| 5 | examination_sessions | Stores examination session details |
| 6 | exams | Stores exam information |
| 7 | student_exams | Stores student exam marks and results |
| 8 | classes | Stores course class periods |
| 9 | attendance | Stores student attendance records |

## Database Relationships

### One-to-Many (1:M)

- Departments → Students
- Departments → Courses
- Courses → Exams
- Courses → Classes
- Examination Sessions → Exams
- Students → Enrollments
- Courses → Enrollments
- Students → Student Exams
- Exams → Student Exams
- Students → Attendance
- Classes → Attendance

### Many-to-Many (M:N)

**Students ↔ Courses**

The `enroll` table manages the relationship between students and courses.

**Students ↔ Exams**

The `student_exams` table manages the relationship between students and exams.

## Constraints Used

| Constraint | Purpose |
|---|---|
| PRIMARY KEY | Uniquely identifies each record |
| FOREIGN KEY | Connects related tables |
| AUTO_INCREMENT | Automatically generates IDs |
| NOT NULL | Prevents empty values |
| UNIQUE | Prevents duplicate values |
| CHECK | Validates column values |
| DEFAULT | Provides a default value |
| ENUM | Restricts values to predefined options |

## SQL Concepts Practiced

### Database Operations
- CREATE DATABASE
- USE
- SHOW DATABASES
- CREATE TABLE
- DROP TABLE
- ALTER TABLE
- DESC

### Data Operations
- INSERT INTO
- SELECT
- UPDATE
- DELETE

### Filtering
- WHERE
- AND
- OR
- LIKE
- IN
- BETWEEN

### Aggregate Functions
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()

### Joins
- INNER JOIN
- LEFT JOIN

### Grouping
- GROUP BY
- HAVING

### Other Concepts
- Primary and Foreign Keys
- One-to-One Relationships
- One-to-Many Relationships
- Many-to-Many Relationships
- Junction Tables
- Composite UNIQUE Constraints

## How to Run

1. Install MySQL Server and MySQL Workbench.
2. Open MySQL Workbench.
3. Create a new SQL query tab.
4. Open the project SQL file.
5. Execute the SQL statements in order.
6. Check the inserted records using SELECT queries.

## Project Structure

```text
Student-Management-System/
│
├── README.md
│
└── student_management_system.sql
```

## Learning Objectives

Through this project, I practiced:

- Identifying entities and attributes from requirements.
- Designing relational database tables.
- Creating primary and foreign keys.
- Understanding 1:1, 1:M, and M:N relationships.
- Creating junction tables.
- Applying database constraints.
- Inserting data while maintaining foreign key relationships.
- Retrieving related data using JOIN queries.
- Using aggregate functions and GROUP BY.

## Future Improvements

- Add teacher management.
- Add student fee management.
- Add course completion status.
- Add individual class schedules.
- Add attendance reports.
- Add student performance reports.
- Add database normalization improvements.
- Add transactions and indexes.

---

**Project:** Student Management System  
**Database:** MySQL  
**Level:** Beginner to Intermediate  
**Purpose:** SQL and Relational Database Design Practice
