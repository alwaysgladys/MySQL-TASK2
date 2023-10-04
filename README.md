# Modification of tables

# Introduction
Modifying tables in MySQL is a crucial aspect of database management, allowing you to adapt your database structure to changing requirements or optimize its performance. This process involves altering existing tables, adding or removing columns, changing data types, and implementing constraints.

MySQL provides a set of powerful commands and syntax for making these adjustments. Whether you need to accommodate new data, improve efficiency, or enhance data integrity, understanding how to modify tables is fundamental for effective database administration.

# Problem Statement
1. Rename the tables to Employee_Info and Employee_Salary
2. Change the ID columns right Employee_ID
3. Create a new column in the Employee_Salary named ‘Department’
4. For employee’s with the following IDs, update their department with the ones specified
1,3,7 - IT
2,5,9 - Advertising

4,6,8,10 - Communications
5. Change the data type of the IDs in both columns to Text data type
6. Run a query that returns the month, year, and day each employee came into the company
7. Return a query that adds 10 years to the year the employees came into the company as their year_of_exit
8. 

![table renaming](https://github.com/alwaysgladys/MySQL-TASK2/assets/144185133/5ff6424d-8eb1-46d4-a9b3-96fc6899e8fb)

The above image demonstrates the effective renaming of the tables to 'Employee_Info' and 'Employee_Salary.' This was done through the use of the following syntax:

Use 'database name', Alter table Staff_info “Rename 'Employee_Info.'"

![change column ID](https://github.com/alwaysgladys/MySQL-TASK2/assets/144185133/29cdeaef-1c47-48a0-925a-67105e7d513c)

The above image illustrates the modification made to the altered column and the syntax used is as follows;

USE 'database_name'; ALTER TABLE employee_info CHANGE COLUMN ID employee_id datatype;

This syntax is used to make a change to the column name in the table by specifying the data type.

![employee salary with dept](https://github.com/alwaysgladys/MySQL-TASK2/assets/144185133/8164bfe4-8b25-4963-8a38-d59653478d65)

The image above indicates the addition of a new column to an existing table, and the syntax used is as follows:

ALTER TABLE Employee_Info ADD COLUMN Department VARCHAR(50);

This command adds a new column named 'Department' with a VARCHAR data type to the 'Employee_Info' table.


This same image also shows the updated table using the employee's_ID and the syntax used is;

UPDATE 'table_name' SET Department = CASE WHEN employee_ID = 1 THEN 'IT' WHEN employee_ID = 3 THEN 'IT' WHEN employee_ID = 7 THEN 'IT' WHEN employee_ID = 2 THEN 'Advertising' ... END;

This command updates the 'Department' column based on the specified conditions for different 'employee_IDs' in the 'table_name.


![DAY, MONTH AND YEAR](https://github.com/alwaysgladys/MySQL-TASK2/assets/144185133/ddd772f0-cabd-4fe5-8783-f94e134e6131)

The image above shows the query for presenting the year, month, and day.
it retrieves the year, month and day values from the "Date of Entry" column in the specified database.

![year of exit](https://github.com/alwaysgladys/MySQL-TASK2/assets/144185133/850e1d91-932f-4094-b919-2c973c7111ec)

This particular image potraits a query that adds ten years to the Date of Entry in the "Employee_Info" table as 'Year of Exit' and the syntax is as follows;

USE Staff; SELECT NAME, DATE_ADD(DOE, INTERVAL 10 YEAR) FROM Employee_Info;

# Conclusion
 Mastering the art of modifying and updating tables in MySQL is essential for any database administrator
 The ability to adapt database structures to evolving requirements is a cornerstone of effective data management.
 With a solid understanding of MySQL's powerful commands and syntax for table modification, you have the tools to ensure your database remains agile, efficient, and aligned with your application's needs. 
