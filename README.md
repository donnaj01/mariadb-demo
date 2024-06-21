# SQL Devlopment with MariaDB/MySQL

## SQL Basics
Lesson: Basic SQL - SELECT Statements, Primary Keys & Joins
---------------------------------------------------------

### 1. Introduction to SQL Basics and Key Concepts

SQL (Structured Query Language) is a powerful language for managing and querying relational databases. let's look at the basic syntax and key concepts of SQL necessary for working with a relational database like the one described in the initial question.

### 1.1 Introduction to SELECT Statements

A **SELECT** statement is used to retrieve data from a table. It consists of the following parts:

1. **Table Name**: The name of the table we want to retrieve data from, e.g., Employees, Stock.
2. **Column List**: A comma-separated list of column names in the selected row(s).
3. **WHERE Clause** (optional): Filters applied to rows retrieved by the query. For example: "SELECT EmployeeID, FirstName FROM Employees WHERE FirstName LIKE 'J%'" would retrieve all employees with a first name starting with the letter J.
4. **ORDER BY Clause** (optional): Sorts the result set in ascending order based on the column specified.
5. **LIMIT Clause** (optional): Limits the number of rows returned by the query.
6. **GROUP BY Clause** (optional): Groups data by one or more columns and calculates aggregates like SUM, AVG, MAX, MIN.
7. **HAVING Clause** (optional): Filters groups based on aggregate functions.
8. **JOIN Clause**: Connects two or more tables based on a common column(s). For example, to join the Employees and Sales tables, you'd use a JOIN like this: "SELECT e.EmployeeID, s.SaleDate FROM Employees AS e JOIN Sales AS s ON e.EmployeeID = s.EmployeeID".

### 1.2 Introduction to Primary Keys

A **primary key** is a unique identifier for each row in a table (e.g., EmployeeID in the Employees table). A primary key constraint ensures that no two rows in a table have the same value. This constraint also prevents NULL values from being entered, as NULL values are not unique.

### 1.3 Introduction to Foreign Keys

A **foreign key** is a column(s) in one table that refers to the primary key of another table (e.g., EmployeeID in Sales table referring to EmployeeID in Employees table). This constraint ensures that data entered into the foreign key column(s) must exist in the referenced primary key column(s), and prevents deletion or insertion of invalid data.

### 1.4 Introduction to Joins - I (1-to-1 relationship)

A **join** is a way to combine two or more tables based on common values in one or more columns, creating a new table with all possible combinations of rows from the original tables. The most basic join type is a 1-to-1 relationship, where each row in either table can be matched to exactly one row in the other table.

### 1.5 Introduction to Joins - II (Many-to-One relationship)

A **many-to-one** relationship exists when a record in one table is related to multiple records in another table, and vice versa. In this case, you would join the tables on a column(s) that represents the relationship between them (e.g., EmployeeID and ClientID in the Sales table).

### 1.6 Introduction to Joins - III (Many-to-Many relationship)

A **many-to-many** relationship exists when a record in one table is related to multiple records in another table, but vice versa, and each record may be related to many other records. In this case, you would join the tables on a column(s) that represents the relationship between them (e.g., EmployeeID and SupplierID in the Sales table).

### 1.7 Basic SQL Examples

Practice writing simple SELECT statements using the concepts introduced above:

* Show all employees who haven't made any sales yet.
* Find the total spent by a specific client (e

## Tasks to perform on the provided data:
1. SQL Basic Syntax and Key Concepts
   - Task 1: Select all sales from the Sales table
   - Task 2: Display client names with their respective total spent on purchases using a simple join between Clients and Sales tables.

2. Joins and Relationships in SQL
   - Task 3: Show all employees who have not completed any sales yet by performing a left join operation between Employees and Sales table, filtering for NULL values in the SalesID column.
   - Task 4: Create a view that combines client and supplier details to identify high-value clients (based on their total spent) with their corresponding suppliers' information. This will require joining multiple tables using inner joins or left/right outer joins, depending on how you want the data presented.

3. Subqueries and Aggregation
   - Task 5: Find out which client has made the most purchases (i.e., highest total spending) in a given period by calculating aggregates using subqueries or group by statements.
   - Challenge: Write an SQL query to find suppliers who have not provided any stock yet. This requires nested subqueries and joins between Supplier, StockSuppliers, and Product tables.

4. Advanced Joins and Views
   - Task 6: Create a left join view that lists all products in the inventory along with their respective stock levels (quantity) using the Stock table joined with itself through the StockDetails table.
   - Challenge: Write an SQL query to find out which employee has made sales of a product not available in the inventory by joining tables and filtering for NULL values in quantity from the StockDetails table. This involves more complex joins, subqueries or left/right outer joins, and multiple tables being joined together.

5. Optimisation Techniques
   - Task 7: Rewrite an existing query to improve its performance by creating a materialized view of frequently accessed data (for example, the list of clients with high total spending).
   - Challenge: Analyze and optimize a complex SQL query that involves multiple joins, aggregations, subqueries, and/or views. Learners should focus on indexes, execution plans, and query optimization techniques like using EXISTS instead of IN when checking for existence in tables.

By gradually increasing the difficulty and incorporating different SQL topics, learners can build a solid foundation while mastering advanced concepts to effectively manage and query data within this relational database system.
