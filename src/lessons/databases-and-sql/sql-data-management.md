# Data Management with SQL
To manage the data in a database, we need an _SQL Query_, which are instructions you give to a database to perform specific actions, such as retrieving data, updating records, or creating new database and tables. Think of them as commands or requests to access and manipulate the data stored in your database in various ways.

## Basic SQL Commands
Just like evry other standard language, SQL has its syntax which must adhere to before we can use it. Generally, SQL commands can be broadly categorized into _Data Definition Language_ (DDL) and _Data Manipulation Language_ (DML), _Data Control Language_ (DCL), and _Tranaction Control Language_ (TCL). For this lesson, we'll on only focus on DDL and DML.

![sql-command-categories](./databases-and-sql/sql-command.png)
  
### Data Definition Language (DDL)
DDL are set of commands that deals with the schema and structure of a database. These commands are used to create, alter, and delete databases and their objects like tables and indexes. The key operations performed by DDL commands include:

- **CREATE**: Used to create new tables or databases. The SQL command below creates a new table named `Customers` with columns for _customer ID, first name, last name_, and _sign-up date_.
  ```sql
  CREATE TABLE Customers (
      CustomerID INTEGER,
      FirstName VARCHAR(100),
      LastName VARCHAR(100),
      SignUpDate DATE
  );
  ```

- **ALTER**: Modifies the structure of existing database objects, for example, adding or removing columns from a table. The SQL commands below adds a new column named `Email` to the existing Customers table.

  ```sql
  ALTER TABLE Customers ADD Email VARCHAR(255);
  ```
- **DROP**: Deletes databases, tables, or other objects completely from the database.
  ```sql
  DROP TABLE TempRecords;
  ```

DDL commands do not manipulate or interact with the data itself but rather define how the database, tables, and other objects are structured. 

<aside>

**`NOTE...`**

Changes made by DDL commands are usually permanent and can significantly alter the database's organization.
</aside>

<!-- ### Data Manipulation Language (DML)
DML commands are used for managing data within tables. These commands allow users to insert, update, delete, and retrieve data from a database. The primary focus of DML is on the manipulation of data rather than the structure of the database.

- **SELECT**: Retrieves data from the database.
  ```sql
  SELECT FirstName, LastName FROM Customers WHERE SignUpDate > '2023-01-01';
  ```
- **INSERT**: Adds new records to a table.
  ```sql
  INSERT INTO Customers (CustomerID, FirstName, LastName, SignUpDate)
  VALUES (1, 'John', 'Doe', '2023-01-15');
  ```
- **UPDATE**: Modifies existing records.
  ```sql
  UPDATE Customers SET Email = 'john.doe@example.com' WHERE CustomerID = 1;
  ```
- **DELETE**: Removes records from a table.
  ```sql
  DELETE FROM Customers WHERE CustomerID = 1;
  ```

### Data Types
Understanding data types in SQL is crucial for defining the type of data that can be stored in each column of a table. Common SQL data types include:
- **INTEGER**: A whole number.
- **VARCHAR**: A variable-length string.
- **DATE**: A calendar date (year, month, day).

**Simple Practice**: Have students define a simple table schema for a "Books" table, choosing appropriate data types for columns like `BookID`, `Title`, `Author`, and `PublishDate`.

### Creating and Modifying Tables
Creating and modifying tables are fundamental skills in managing a database schema.

- **Creating Tables**: Use the `CREATE TABLE` statement to define a new table's structure.
  ```sql
  CREATE TABLE Books (
      BookID INTEGER PRIMARY KEY,
      Title VARCHAR(255),
      Author VARCHAR(100),
      PublishDate DATE
  );
  ```
- **Modifying Tables**: Use the `ALTER TABLE` command to add, delete, or modify columns in an existing table.
  ```sql
  ALTER TABLE Books ADD Genre VARCHAR(100);
  ```

**Simple Practice**: Encourage students to create their own table based on a hobby or interest, adding at least four columns with appropriate data types, and then modifying it by adding an additional column.

### Checking Student Understanding
- **Exercise**: Ask students to write a series of SQL commands to create a table, insert records, update a record, and then select a specific record.
- **Quiz**: Prepare a quiz covering the basic SQL commands, data types, and steps for creating and modifying tables, including recognizing the correct syntax and uses for each SQL command.
- **Group Activity**: In small groups, have students design a database schema for a simple application (like a to-do list or a small online store) and present their schema and example SQL commands to the class. -->
