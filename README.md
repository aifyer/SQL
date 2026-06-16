SQL Database Project

Overview

This project demonstrates the process of creating and managing a PostgreSQL database, including database setup, table creation, data import, and SQL querying.

The goal of the project is to practice fundamental database concepts and SQL skills commonly used in data science, bioinformatics, and data engineering workflows.

Objectives

* Install and configure PostgreSQL
* Create a relational database
* Define database schemas and tables
* Import data from external files
* Perform SQL queries for data exploration and analysis
* Practice database management and data manipulation techniques

⸻

Technologies Used

* PostgreSQL
* SQL
* pgAdmin
* CSV data files
* Command-line PostgreSQL tools


⸻

Database Setup

Create Database

CREATE DATABASE mydatabase;

Connect to the database:

\c mydatabase

⸻

Create Tables

Example:

CREATE TABLE employees (
    employee_id SERIAL PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department VARCHAR(50),
    salary NUMERIC
);

⸻

Import Data

Example using PostgreSQL’s COPY command:

COPY employees
FROM '/path/to/employees.csv'
DELIMITER ','
CSV HEADER;

⸻

Example Queries

Retrieve All Records

SELECT *
FROM employees;

Count Records

SELECT COUNT(*)
FROM employees;

Filter Data

SELECT *
FROM employees
WHERE salary > 50000;

Aggregate Statistics

SELECT
    department,
    AVG(salary) AS average_salary
FROM employees
GROUP BY department;

⸻

Skills Demonstrated

Database Design

* Creating relational database structures
* Defining primary keys
* Managing data types and constraints

Data Import

* Loading external datasets
* Handling CSV-formatted data
* Verifying imported records

SQL Querying

* SELECT statements
* Filtering with WHERE
* Sorting with ORDER BY
* Aggregations using GROUP BY
* Joins between tables
* Data summarization

Database Administration

* Database creation
* Table management
* Data validation
* Query optimization basics

⸻

Example Workflow

1. Create PostgreSQL database.
2. Define table schemas.
3. Import data files.
4. Verify imported records.
5. Run analytical queries.
6. Export results for further analysis.


⸻

Author

Sophie Hongfei Liu

* Ph.D. in Genetics
* Data Scientist
* Bioinformatics and Data Science Enthusiast

GitHub: aifyer⁠￼

⸻

License

This project is intended for educational and portfolio purposes.

For a portfolio repository, I’d also recommend adding:

* 2–3 screenshots of pgAdmin showing your tables and queries
* An ER diagram (if you have multiple tables)
* A section titled “Key SQL Concepts Demonstrated” listing JOINs, GROUP BY, subqueries, indexes, etc. Recruiters often look for those keywords.
