# MySQL-Lab

## Hierarchical / Tree View :

**school_db**

```
+----------------------+
| school_db [Database] |
+----------------------+
    |
    |   +------------------+
    └── | students [Table] |
        +------------------+
            ├── student_id (INT, PK, AUTO_INCREMENT)
            ├── first_name (VARCHAR(50))
            ├── last_name (VARCHAR(50))
            ├── gender (ENUM: 'Male', 'Female', 'Other')
            ├── dob (DATE)
            ├── department (VARCHAR(100))
            ├── admission_year (INT)
            └── gpa (DECIMAL(3,2))
```
> This shows the structure of the database and table

## Table Schema:

**students**

| Column Name     | Data Type                         | Constraints                            |
| --------------- | --------------------------------- | -------------------------------------- |
| student_id      | ``INT``                           | PRIMARY KEY, AUTO_INCREMENT, NOT NULL  |
| first_name      | ``VARCHAR(50)``                   | NOT NULL                               |
| last_name       | ``VARCHAR(50)``                   | NOT NULL                               |
| gender          | ``ENUM('Male','Female','Other')`` | NOT NULL                               |
| dob             | ``DATE``                          | NOT NULL                               |
| department      | ``VARCHAR(100)``                  | NOT NULL                               |
| admission_year  | ``INT``                           | NOT NULL                               |
| gpa             | ``DECIMAL(3,2)``                  | CHECK (gpa BETWEEN 0.00 AND 4.00)      |

## Sample Data:

**students**

|student_id | first_name | last_name | gender | dob        | department       | admission_year | gpa  |
|-----------|------------|-----------|--------|------------|------------------|----------------|------|
| 1         | Prakash    | Shrestha  | Male   | 2002-03-15 | Computer Science | 2020           | 3.75 |
| 2         | Sita       | Shrestha  | Female | 2001-07-22 | Business         | 2019           | 3.60 |
| 3         | Prakash    | Thapa     | Male   | 2003-01-10 | Engineering      | 2021           | 2.40 |
| 4         | Maya       | Lama      | Female | 2000-11-05 | Computer Science | 2018           | 3.85 |
| 5         | Aarav      | KC        | Male   | 2002-05-28 | Arts             | 2020           | 3.20 |
| 6         | Nisha      | Magar     | Female | 2001-09-12 | Engineering      | 2019           | 3.55 |

## Operations:

- **Table Setup** 
    - Create Database & Table 
    - Insert Sample Data 

- **Queries**
    - Select all records and find total number of student.
    - Select specific columns
    - Filter by ``department``
    - Filter by ``GPA`` greater than ``3.5``
    - Order by ``GPA`` (highest first)
    - Show full names using ``CONCAT``
    - Search students by ``first name``, ``last name``, or ``full name`` (combined).
    - Count students in each ``department``
    - Average ``GPA`` by ``department``
    - Find the highest and lowest ``GPA`` student
    - Students admitted after ``2019``
    - Top ``3`` students by ``GPA``
    - Find the oldest ``student`` 
    - Total students admitted each year
    - Total ``GPA`` by ``gender``
    - Show only the full name and pass/fail result [ if **``(gpa >= 2.50)``** ``Pass`` else ``Fail`` ]

- **Update Table**
    - Update ``GPA`` for a student
    - Delete a student by ``ID``

- **Table management** 
    - Add a new column
    - Modify column data type
    - Rename a column
    - Drop a column
    - Rename table
    - Truncate table (delete all records)
    - Drop table

- **Drop database**

---
