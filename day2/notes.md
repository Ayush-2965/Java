
## DataBase

A database is a collection of interrelated data stored in the form of files.

## DBMS

A Database Management System (DBMS) is software that allows us to manage data stored in a database.

**Examples:** `Oracle`, `MySQL`

## RDBMS

A Relational Database Management System (RDBMS) stores data in tables (also called relations). Data is accessed through these tables, making data fetching faster compared to traditional DBMS, especially for large datasets.

- **Rows:** Tuples
- **Columns:** Fields, Keys

### Primary Key

A primary key is a column (or set of columns) that contains unique values for each row. It cannot have any `NULL` values.

### Unique Key

A unique key also ensures uniqueness for each row, but it can contain `NULL` values.

### Foreign Key

A foreign key is a column in one table that refers to the primary key of another table. It is used to establish a relationship between two tables.

- Both foreign keys and primary keys are used to relate tables.

## JDBC (Java Database Connectivity)

JDBC is an API in Java that allows Java programs to connect and interact with databases.

### Steps for JDBC Connectivity

1. Create a table with the required fields in the database.
2. Add the appropriate JDBC driver to your project to enable database connectivity.
3. Write SQL queries to manipulate data in the database (e.g., insert, update, delete, select).

### Basic JDBC Classes and Interfaces

- `java.io` contains `DataInputStream` for input operations.
- `java.sql` contains classes and interfaces for database operations.

#### JDBC Driver Types

- **Type 1 to Type 4 drivers** exist for JDBC connectivity.
- Type 4 drivers are written entirely in Java.

#### Example: Oracle JDBC Driver

- Driver class: `oracle.jdbc.driver.OracleDriver`
- Maven dependency: `oracle-jdbc-driver-oracledriver`
- Default Oracle port: `1521`

#### Establishing a Connection

```java
Connection con = DriverManager.getConnection(
    "jdbc:oracle:thin:@localhost:1521:xe", "username", "password"
);
```

- `DriverManager` is a class responsible for managing JDBC drivers and establishing connections to the database.

## Steps for Creating a Table in SQL

1. Open the database console or SQL editor.
2. Use the `CREATE TABLE` statement to define the table structure.

**Example:**

```sql
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50) UNIQUE,
    age INT,
    course_id INT,
    FOREIGN KEY (course_id) REFERENCES courses(id)
);
```

- Define primary keys, unique keys, and foreign keys as needed.

---

**Summary Table:**

| Term         | Description                                                      |
|--------------|------------------------------------------------------------------|
| Database     | Collection of interrelated data                                  |
| DBMS         | Software to manage databases                                     |
| RDBMS        | DBMS with data stored in tables (relations)                      |
| Primary Key  | Unique, non-null identifier for table rows                       |
| Unique Key   | Unique identifier, allows nulls                                  |
| Foreign Key  | Key in one table referencing primary key in another table        |
| JDBC         | Java API for database connectivity                               |

