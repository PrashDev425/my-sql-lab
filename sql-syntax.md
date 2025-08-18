## SQL Syntax:

### Creating Database:

**Syntax:**

```sql
CREATE DATABASE database_name;
```

**Example:**

```sql
CREATE DATABASE school_db;
```

### Creating Table:

**Syntax:**

```sql
CREATE TABLE table_name (
    column1 datatype [constraint],
    column2 datatype [constraint],
    ...
    table_constraints
);
```
**Example:**

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender ENUM('Male','Female','Other') NOT NULL,
    dob DATE NOT NULL,
    gpa DECIMAL(3,2) CHECK (gpa >= 0.00 AND gpa <= 4.00)
);
```

### Query

**Syntax:**

```sql
SELECT column1, column2, aggregate_function(...)
FROM table1
WHERE condition
GROUP BY column
HAVING condition
ORDER BY column [ASC | DESC]
LIMIT number OFFSET number;
```

**Example:**

```sql
SELECT dept, COUNT(student_id) AS total_students, AVG(gpa) AS avg_gpa
FROM students
WHERE gpa >= 2.5
GROUP BY dept
HAVING AVG(gpa) > 3.0
ORDER BY avg_gpa DESC
LIMIT 3 OFFSET 0;
```

**Clause Breakdown:**

- ``SELECT`` → Choose which columns (or expressions) to display.

- ``FROM`` → Table(s) from which data is retrieved.

- ``WHERE`` → Filter rows before grouping/aggregation.

- ``GROUP BY`` → Group rows (used with aggregate functions like COUNT, SUM, AVG).

- ``HAVING`` → Filter groups (applied after GROUP BY).

- ``ORDER BY`` → Sort the results.

- ``LIMIT / OFFSET`` → Limit number of rows returned (pagination).
