# Database Design & Student Registration System

<div align="center">

[![Live Demo](https://img.shields.io/badge/▶_Live_Demo-3B82F6?style=for-the-badge)](https://sazzadmahfuz.github.io/database-design-system)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](.)
[![Database Design](https://img.shields.io/badge/Database-ER_Modeling-00FFD1?style=for-the-badge)](.)
[![SQL](https://img.shields.io/badge/SQL-DDL_&_DML-orange?style=for-the-badge)](.)
[![Normalization](https://img.shields.io/badge/Normalization-1NF→3NF-7B61FF?style=for-the-badge)](.)
[![Course](https://img.shields.io/badge/HAMK-Database_Design-003087?style=for-the-badge)](.)

### Advanced Student Course Registration Database System

Interactive relational database design and SQL analytics system developed using:

**MySQL · ER Modeling · SQL Queries · Database Normalization · Relational Schema · Interactive Dashboard**

---

### Developed by

# Sazzad Ibna Mahfuz

Bachelor of Engineering — ICT Robotics  
Häme University of Applied Sciences (HAMK), Finland

</div>

---

# Project Overview

This project demonstrates a complete **Student Course Registration Database Management System** designed for academic administration, enrollment management, and relational database learning.

The system was developed as part of the:

### Database Design & Programming Course — HAMK University of Applied Sciences

The project simulates a university registration environment where:

- Students register for courses
- Instructors manage course sections
- Departments offer academic programs
- Enrollment records store grades and semesters
- SQL queries generate reports and analytics
- Relational constraints maintain data integrity

The system provides a complete workflow for studying:

- Entity–Relationship (ER) modeling
- Relational schema design
- SQL DDL and DML operations
- Primary and foreign key relationships
- Database normalization
- Aggregate SQL queries
- JOIN operations
- Referential integrity
- Academic database systems
- Interactive SQL visualization

The application allows users to:

✅ Design relational database schemas  
✅ Visualize ER diagrams and relationships  
✅ Execute SQL queries interactively  
✅ Analyze student enrollments and transcripts  
✅ Study normalization from 1NF → 3NF  
✅ Explore JOIN and aggregation operations  
✅ Understand associative and weak entities  
✅ Simulate real university registration systems  
✅ Monitor relational constraints and dependencies  
✅ Study practical database implementation concepts

The project combines:

- MySQL 8.0
- SQL
- JavaScript
- HTML5
- CSS3
- Chart.js
- Interactive dashboard systems

into a complete educational database engineering environment.

---

# Project Objectives

The main objectives of this project were:

- Understand relational database design
- Implement ER modeling techniques
- Design normalized database schemas
- Develop SQL DDL and DML operations
- Study referential integrity constraints
- Implement real-world academic database systems
- Practice SQL JOIN and aggregation queries
- Build interactive SQL visualization interfaces
- Understand weak and associative entities
- Apply normalization principles
- Create database reporting systems
- Simulate practical student registration workflows

---

# System Architecture

```text
University Data
        │
        ▼
ER Modeling
        │
        ▼
Relational Schema Design
        │
        ▼
Normalization (1NF → 3NF)
        │
        ▼
MySQL Database Implementation
        │
        ▼
DDL Table Creation
        │
        ▼
DML Data Insertion
        │
        ▼
SQL Query Processing
        │
        ▼
Interactive Dashboard & Reports
```

---

# Core Features

| Feature | Description |
|---|---|
| **ER Diagram Modeling** | Crow’s Foot entity–relationship visualization |
| **Relational Schema Design** | Primary key and foreign key relationships |
| **Interactive SQL Console** | Simulated SQL query execution environment |
| **Database Normalization** | Full 1NF → 3NF normalization proof |
| **DDL & DML Operations** | CREATE, INSERT, UPDATE, DELETE examples |
| **JOIN Query Analysis** | Multi-table relational query demonstrations |
| **Aggregate SQL Queries** | GROUP BY, HAVING, AVG, COUNT operations |
| **Student Transcript Reports** | Real-world reporting system |
| **Enrollment Analytics** | Course registration summary generation |
| **Constraint Validation** | UNIQUE, CHECK, CASCADE operations |
| **Interactive Dashboard UI** | Real-time schema and SQL visualization |
| **MySQL Relational System** | Practical academic database implementation |

---

# University Database Model

The system models a simplified university registration environment.

---

# Project Preview

<div align="center">

| ER Diagram | Relational Schema |
|---|---|
| <img src="Pictures/1%20(5).png" width="420"> | <img src="Pictures/1%20(6).png" width="420"> |

| Student Table Data | Enrollment Table Data |
|---|---|
| <img src="Pictures/1%20(1).png" width="420"> | <img src="Pictures/1%20(2).png" width="420"> |

| SQL Query Operations | Reports & Analytics |
|---|---|
| <img src="Pictures/1%20(3).png" width="420"> | <img src="Pictures/1%20(4).png" width="420"> |

</div>

---

# Main Entities

| Entity | Description |
|---|---|
| STUDENT | Stores student information |
| INSTRUCTOR | Stores instructor and department data |
| DEPARTMENT | Represents academic departments |
| COURSE | Represents university courses |
| SECTION | Course offerings per semester |
| ENROLLMENT | Links students to course sections |
| STUDENT_PHONE | Handles multiple phone numbers |

---

# Entity Relationships

The project implements multiple real-world database relationships:

| Relationship | Type |
|---|---|
| DEPARTMENT → COURSE | 1:N |
| DEPARTMENT → INSTRUCTOR | 1:N |
| COURSE → SECTION | 1:N |
| INSTRUCTOR → SECTION | 1:N |
| STUDENT → ENROLLMENT | M:N |
| STUDENT → STUDENT_PHONE | 1:N |

---

# ER Diagram Design

The database schema was modeled using:

### Crow’s Foot ER Modeling Notation

The design includes:

- Strong entities
- Weak entities
- Associative entities
- Multivalued attributes
- Derived attributes
- Referential integrity constraints

---

# Weak Entity Design

The project implements:

### SECTION

as a weak entity identified by:

```text
(CourseID + SectionNo)
```

This mirrors real academic scheduling systems where multiple sections belong to one course.

---

# Associative Entity

The:

### ENROLLMENT

table acts as an associative entity connecting:

```text
STUDENT ↔ SECTION
```

while storing:

- Enrollment date
- Grade
- Status
- Semester information

---

# Relational Schema

The relational schema maintains strict integrity using:

- Primary Keys (PK)
- Foreign Keys (FK)
- Composite Keys
- UNIQUE constraints
- CHECK constraints
- Cascading updates/deletes

---

# Example Relational Schema

```sql
CREATE TABLE students (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Email VARCHAR(100) UNIQUE NOT NULL,
    Major VARCHAR(50),
    Year VARCHAR(20)
);
```

---

# Composite Key Design

The project demonstrates advanced composite key implementation.

---

## SECTION Primary Key

```text
PK(SECTION) = (CourseID, SectionNo)
```

---

## ENROLLMENT Primary Key

```text
PK(ENROLLMENT) =
(StudentID, CourseID, SectionNo)
```

This prevents duplicate registrations for the same course section.

---

# Database Normalization

The project applies complete normalization principles.

---

# 1NF — First Normal Form

The database removes:

- Repeating groups
- Multi-valued fields
- Non-atomic values

Example:

```text
Student phone numbers moved into STUDENT_PHONE table
```

---

# 2NF — Second Normal Form

The schema removes:

```text
Partial dependencies
```

All non-key attributes depend on the entire primary key.

---

# 3NF — Third Normal Form

The database removes:

```text
Transitive dependencies
```

Instructor and course information are separated into dedicated tables.

Derived attributes such as GPA are not stored directly.

---

# Referential Integrity

The project implements strong relational integrity constraints.

---

# Constraints Used

| Constraint | Purpose |
|---|---|
| PRIMARY KEY | Unique row identification |
| FOREIGN KEY | Relationship enforcement |
| UNIQUE | Prevent duplicate emails |
| CHECK | Validate course credits |
| NOT NULL | Mandatory field validation |
| ON DELETE CASCADE | Automatic dependency cleanup |
| ON UPDATE CASCADE | Relationship synchronization |

---

# SQL Query System

The system demonstrates practical SQL operations.

---

# Query Types Implemented

| Query Type | Purpose |
|---|---|
| SELECT | Retrieve records |
| WHERE | Conditional filtering |
| ORDER BY | Sorting |
| JOIN | Multi-table queries |
| GROUP BY | Aggregation |
| HAVING | Aggregate filtering |
| AVG / COUNT | Statistical queries |
| UPDATE | Data modification |
| DELETE | Record removal |
| Subqueries | Nested query logic |

---

# Example JOIN Query

```sql
SELECT
    s.Name AS StudentName,
    c.CourseName,
    i.Name AS Instructor,
    e.Semester,
    e.Grade
FROM Students s
JOIN Enrollment e
    ON s.StudentID = e.StudentID
JOIN Courses c
    ON e.CourseID = c.CourseID
JOIN Instructors i
    ON c.InstructorID = i.InstructorID;
```

---

# Aggregate Query Example

```sql
SELECT
    c.CourseName,
    COUNT(e.StudentID) AS Total_Students
FROM Courses c
LEFT JOIN Enrollment e
    ON c.CourseID = e.CourseID
GROUP BY c.CourseName;
```

---

# GPA Calculation Query

The project demonstrates SQL aggregate computation:

```sql
ROUND(AVG(
    CASE Grade
        WHEN 'A' THEN 4.0
        WHEN 'A-' THEN 3.7
        WHEN 'B+' THEN 3.3
        WHEN 'B' THEN 3.0
    END
), 2)
```

for calculating average GPA per course.

---

# Database Reports

The system includes real-world reporting examples.

---

# Student Transcript Report

Displays:

- Student name
- Course information
- Instructor
- Semester
- Grade

---

# Course Enrollment Summary

Displays:

- Course names
- Total enrolled students
- Instructor assignments
- Enrollment statistics

---

# Interactive Dashboard System

The project includes an interactive visualization interface built using:

- HTML5
- CSS3
- JavaScript
- Canvas API
- Chart.js

The dashboard provides:

✅ Interactive SQL console  
✅ ER diagram rendering  
✅ Schema visualization  
✅ Database statistics  
✅ Query execution simulation  
✅ Relational analytics panels  
✅ SQL report previews  
✅ Real-time database interaction

---


# SQL Operations Demonstrated

The project demonstrates complete database workflows including:

- Database creation
- Table creation
- Data insertion
- Data retrieval
- Multi-table joins
- Aggregation
- Nested queries
- Referential updates
- Record deletion
- Constraint validation

---

# Database Concepts Implemented

The project combines multiple database engineering concepts including:

- Relational Databases
- ER Modeling
- Crow’s Foot Notation
- SQL Programming
- Normalization
- Primary & Foreign Keys
- Weak Entities
- Associative Entities
- Referential Integrity
- Aggregate Queries
- Relational Algebra
- Database Constraints
- Schema Design
- Academic Information Systems

---

# Engineering Concepts Applied

| Concept | Application |
|---|---|
| Relational Modeling | ER schema development |
| Data Integrity | Constraint enforcement |
| SQL Programming | Query execution |
| Database Engineering | Schema normalization |
| Information Systems | Academic registration system |
| Visualization | Interactive dashboard rendering |
| System Design | Relational architecture |
| Data Analytics | Enrollment reporting |

---

# Real-World Applications

This type of database system is commonly used in:

- University registration systems
- Academic management platforms
- Student information systems
- Enrollment analytics platforms
- Educational ERP systems
- Learning management systems
- Course scheduling platforms
- Institutional reporting systems

---

# Topics Covered

- Database Design
- ER Modeling
- Relational Schema
- SQL
- MySQL
- Database Normalization
- DDL & DML
- JOIN Operations
- Aggregate Queries
- Referential Integrity
- Crow’s Foot Notation
- Student Registration Systems
- Interactive SQL Dashboards
- Relational Databases

---

# Key Learning Outcomes

This project helped develop practical skills in:

✅ Relational database design  
✅ ER diagram development  
✅ SQL DDL & DML operations  
✅ Database normalization  
✅ Composite key implementation  
✅ Referential integrity enforcement  
✅ SQL JOIN operations  
✅ Aggregate query development  
✅ Interactive dashboard systems  
✅ Academic database modeling  
✅ MySQL database implementation  
✅ Database reporting systems

---

# Future Improvements

Potential future developments include:

- Full backend database connectivity
- Real-time MySQL server integration
- Authentication system
- Student login portal
- Course prerequisite system
- GPA automation
- REST API integration
- Stored procedures and triggers
- Advanced analytics dashboards
- Cloud-hosted database systems
- Transaction management
- Role-based access control
- Web-based registration portal
- Real-time enrollment validation

---

# Academic Context

**Course**: Database Design & Programming  
**Programme**: BEng ICT & Robotics, HAMK University of Applied Sciences  
**Database Engine**: MySQL 8.0.43  
**Project Type**: Team Project — Team No. 7  
**Topics covered**: ER modeling, relational schema design, normalization, SQL programming, referential integrity, database implementation. :contentReference[oaicite:0]{index=0}

---

# 👨‍💻 Author

# Sazzad Ibna Mahfuz

Bachelor of Engineering — ICT Robotics  
Häme University of Applied Sciences (HAMK)  
Finland  
[Portfolio](https://sazzadmahfuz.github.io) · [LinkedIn](https://www.linkedin.com/in/sazzad-mahfuz) · [GitHub](https://github.com/sazzadmahfuz)

---

<div align="center">

# ⭐ If you found this database project interesting, consider starring the repository!

</div>
