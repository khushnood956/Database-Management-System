Database Management System (DBMS) Project
This is a simple Database Management System (DBMS) implemented in Java. It allows users to perform basic database operations such as creating, dropping, inserting, updating, deleting, and selecting data from tables stored as CSV files. The system supports a command-line interface where users can input SQL-like commands to interact with the database.
Features include: 

CREATE TABLE to create a new table with specified columns
DROP TABLE to delete an existing table after confirmation
SHOW ALL to display all existing table names
INSERT to add new records to a table
SELECT to retrieve records from a table with optional filtering (HAVING) and sorting (SORT BY)
UPDATE to modify existing records based on a condition
DELETE to remove records from a table based on a condition
HELP to display syntax and examples for all supported commands
EXIT to terminate the program

Requirements: 

Java Development Kit (JDK) 8 or higher 
A Java-compatible IDE or command-line environment

Installation:

Clone or download this repository to your local machine
Navigate to the project directory
Compile the Java code: javac DBMSproject.java
Run the program: java DBMSproject

Usage:Run the program, and you will be greeted with a prompt:>> Welcome to Database Management System. Enter "HELP" for the syntax details >>Enter commands in the format specified below. Type HELP to view detailed syntax and examples. Type EXIT to quit the program.
Supported Commands:

CREATE TABLE: CREATE TABLE table_name (column1, column2, column3, ...)Example: CREATE TABLE student (name, regno, address)
DROP TABLE: DROP table_name TABLEExample: DROP student TABLE
SHOW ALL: SHOW ALL
INSERT: INSERT IN TABLE table_name VALUES (value1, value2, value3, ...)Example: INSERT IN TABLE student VALUES ("Haq", "FA16-BCT-099", "Islamabad")
SELECT: SELECT FROM TABLE table_name [HAVING column = value] [SORT BY column]Example: SELECT FROM TABLE student HAVING address = "Islamabad" SORT BY name
UPDATE: UPDATE table_name SET column = value WHERE column = valueExample: UPDATE student SET address = "Lahore" WHERE name = "Haq"
DELETE: DELETE FROM TABLE table_name HAVING column = valueExample: DELETE FROM TABLE student HAVING name = "Haq"
HELP: HELP
EXIT: EXIT

Implementation Details:Tables are stored as CSV files in the same directory as the program. Each file represents a table, with the first row containing column headers and subsequent rows containing data. The program removes extra spaces from input commands and validates syntax before processing. The system includes checks for invalid table names, missing files, incorrect syntax, and other potential errors. The SELECT command supports filtering and sorting, with results displayed in a formatted table. Uses Java's file I/O to read and write CSV files, ensuring data persistence.
Limitations: 

Limited to basic SQL-like operations; advanced features like joins or indexes are not supported
No support for data types; all values are treated as strings
Sorting in SELECT is case-insensitive and alphabetical only
CSV files must be in the correct format to avoid parsing errors

Contributing:Feel free to fork this repository, make improvements, and submit pull requests. Suggestions for new features or bug fixes are welcome!
License:This project is licensed under the MIT License. See the LICENSE file for details.
Contact:For questions or feedback, please open an issue on this repository.
