# sql_challenge
# Employee Database

This project defines an SQL schema and a set of queries for an Employee Management Database. The schema comprises several tables, including `employees`, `departments`, `dept_emp`, `dept_manager`, `salaries`, and `titles`, each with defined relationships and constraints. The SQL queries extract specific information from these tables to answer common business questions.

## Database Schema Overview

The schema consists of the following tables:

- **employees**: Contains employee details, including employee number, birth date, first name, last name, gender, and hire date. The primary key is `emp_no`.
- **departments**: Contains department details, including department number and name. The primary key is `dept_no`.
- **dept_emp**: Links employees to departments, with `emp_no` and `dept_no` as foreign keys.
- **dept_manager**: Associates managers with departments, using `emp_no` and `dept_no` as foreign keys.
- **salaries**: Stores employee salaries with `emp_no` as a foreign key.
- **titles**: Holds job titles with a primary key `title_id`.

## Foreign Key Relationships

- `dept_emp.emp_no` references `employees.emp_no`
- `dept_emp.dept_no` references `departments.dept_no`
- `dept_manager.dept_no` references `departments.dept_no`
- `dept_manager.emp_no` references `employees.emp_no`
- `salaries.emp_no` references `employees.emp_no`

## Queries Overview

The provided SQL queries demonstrate common operations on this schema:

1. **List Employee Details with Salary**:
   - Retrieves employee number, last name, first name, gender, and salary.
   - Uses a JOIN between `employees` and `salaries`.

2. **Employees Hired in 1986**:
   - Lists first name, last name, and hire date for employees hired in 1986.

3. **Managers of Each Department**:
   - Retrieves department details along with the employee information for each department manager.

4. **Employee Department Details**:
   - Lists each employee's department, employee number, last name, first name, and department name.

5. **Employees Named Hercules with Last Name Starting with B**:
   - Lists first name, last name, and gender for employees with specific name criteria.

6. **Employees in Sales Department**:
   - Lists employees in the Sales department, including their employee number, last name, and first name.

7. **Employees in Sales and Development Departments**:
   - Lists employees in both Sales and Development departments with their details.

8. **Frequency of Employee Last Names**:
   - Counts and orders by frequency the number of employees sharing each last name.

## Running the Queries

To execute these queries, follow these steps:

1. Ensure you have a running SQL server instance (e.g., PostgreSQL, MySQL, SQLite).
2. Import the SQL schema to create the database tables.
3. Run the provided queries to extract the desired information.
4. Use SQL client software or database management tools to execute the queries and view the results.


