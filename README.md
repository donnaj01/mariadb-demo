# SQL Devlopment with MariaDB/MySQL

##Tasks to perform on the provided data:
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

5. Optimization Techniques
   - Task 7: Rewrite an existing query to improve its performance by creating a materialized view of frequently accessed data (for example, the list of clients with high total spending).
   - Challenge: Analyze and optimize a complex SQL query that involves multiple joins, aggregations, subqueries, and/or views. Learners should focus on indexes, execution plans, and query optimization techniques like using EXISTS instead of IN when checking for existence in tables.

By gradually increasing the difficulty and incorporating different SQL topics, learners can build a solid foundation while mastering advanced concepts to effectively manage and query data within this relational database system.
