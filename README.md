# SQL-Server

![image sql-server-logo](image/sql-server_logo.png)

## Introduction to SQLServer

### What is Database ?

A database is an organized collection of data so that it can be easily accessed. To manage these databases, **Database Management Systems (DBMS)** are used.



**Database Management System**

Database management System is software which is used to store and retrieve the database.

**Types of DBMS**

In general, there are two common types of databases:

* Non-Relational

* Relational

**Non-Relational Database Management System (Non-RDBMS)**

In Non-RDBMS, data is stored in key-value pairs. For example:

![image Non-RDBMS](image/Nosql.png)

Here, customers' data are stored in key-value pairs.

Commonly used Non-RDBMS: MongoDB, Amazon DynamoDB, Redis, etc.

**Relational Database Management System**

In RDBMS, data is stored in tabular format. For example,

![image RDBMS](image/rdbms.png)

Here, customers is a table inside the database.

The first row is the attributes of the table. Each row after that contains the data of a customer.

In RDBMS, two or more tables may be related to each other. Hence the term "Relational". For example,

![image RDBMS](image/related-tables.png)

Here, orders and customers are related through customer_id.

Commonly used RDBMS: MySQL, PostgreSQL, MSSQL, Oracle etc.

### What is SQL Server ?

SQL Server is a relational database management system, or RDBMS, developed and marketed by Microsoft.

Similar to other RDBMS software, SQL Server is built on top of SQL, a standard programming language for interacting with relational databases. SQL Server is tied to Transact-SQL, or T-SQL, the Microsoft’s implementation of SQL that adds a set of proprietary programming constructs.

**SQL Server Architecture** 

![image sql-arch](image/sql-arch.jpg)

SQL Server consists of two main components:

* Database Engine
* SQLOS

**Database Engine**

![image database engine](image/database-engine.jpg)

The core component of the SQL Server is the Database Engine. 

The Database Engine consists of a relational engine that processes queries and a storage engine that manages database files, pages, indexes, etc. The database objects such as stored procedures, views, and triggers are also created and executed by the Database Engine.

**SQLOS**(SQL Server Operating System)

SQLOS provides many operating system services such as memory and I/O management. Other services include exception handling and synchronization services.

### Difference between MySql and MS Sql Server

**MySQL** is an open source Relational Database Management System (RDBMS) based on Structured Query Language (SQL). It runs on platforms like Linux, UNIX and Windows.

**SQL Server** is owned and developed by Microsoft Corporation. The primary function of SQL Server is the storage and access of data as it is required by other applications, whether they are running on other computers that are connected to a network, or the computer on which the server is stored.


|                                          **_MS SQL Server_**                                          |                                                 **_MySQL_**                                                 |
|:-----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| Developed by Microsoft.                                                                         | Developed by Oracle.                                                                                  |
| It supports programming languages like C++, JAVA, Ruby, Visual Basic, Delphi, R etc.            | MySQL offers extended running support for languages like Perl, Tcl, Haskey etc.                       |
| Expects a large amount of operational storage space.                                            | Expects less amount of operational storage space.                                                     |
| It enables for stopping query execution.                                                        | It doesn’t allow query cancellation mid-way in the process.                                           |
| Doesn’t block the database while backing up the data.                                           | Blocks the database while backing up the data.                                                        |
| It is not free.                                                                                 | It is open source. It is freely available.                                                            |
| It is a highly secured and doesn’t allow any kind of database file manipulation while running.  | It allows database file manipulation while running.                                                   |
| It is available in multiple editions, such as Enterprise, Standard, Web, Workgroup, or Express. | It is available in MySQL Standard Edition, MySQL Enterprise Edition, and MySQL Cluster Grade Edition. |

### Installation of SQL Server
<br>

For complete installation guide [click here](https://github.com/PadmanabhanSwayaan/SQL-Server/blob/sqlserver-v15.0/pdf/SQL-Server-Installation-Guide.pdf)


## Data Types

### Exact Numeric 
<br>

<!-- data-transpose data-type="none" -->
| **_Data Type_** | **_Description_**                          | **_Lower limit_**                   | **_Upper limit_**                    | **_Memory_**       |
|-----------------|--------------------------------------------|-------------------------------------|--------------------------------------|--------------------|
| bigint          | It stores whole numbers in the range given | −2^63 (−9,223,372, 036,854,775,808) | 2^63−1 (−9,223,372, 036,854,775,807) | 8 bytes            |
| int             | It stores whole numbers in the range given | −2^31 (−2,147, 483,648)             | 2^31−1 (−2,147, 483,647)             | 4 bytes            |
| smallint        | It stores whole numbers in the range given | −2^15 (−32,767)                     | 2^15 (−32,768)                       | 2 bytes            |
| tinyint         | It stores whole numbers in the range given | 0                                   | 255                                  | 1 byte             |
| bit             | It can take 0, 1, or NULL values.          | 0                                   | 1                                    | 1 byte/8bit column |
| decimal         | Used for scale and fixed precision numbers | −10^38+1                            | 10^381−1                             | 5 to 17 bytes      |
| numeric         | Used for scale and fixed precision numbers | −10^38+1                            | 10^381−1                             | 5 to 17 bytes      |
| money           | Used monetary data                         | −922,337, 203, 685,477.5808         | +922,337, 203, 685,477.5807          | 8 bytes            |
| smallmoney      | Used monetary data                         | −214,478.3648                       | +214,478.3647                        | 4 bytes            |

### Approximate Numeric
 <br>

<!-- data-transpose data-type="none" -->
| **_Data Type_** | **_Description_**                      | **_Lower limit_** | **_Upper limit_** | **_Memory_**                | **_Precision_** |
|---------------|--------------------------------------|-----------------|-----------------|---------------------------|---------------|
| float(n)      | Used for a floating precision number | −1.79E+308      | 1.79E+308       | Depends on the value of n | 7 Digit       |
| real          | Used for a floating precision number | −3.40E+38       | 3.40E+38        | 4 bytes                   | 15 Digit      |

### Date & Time
<br>

<!-- data-transpose data-type="none" -->
| **_Data Type_**  | **_Description_**                                                                                                         | **_Storage size_** | **_Accuracy_**                              | **_Lower Range_**  | **_Upper Range_**  |
|----------------|-------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------|------------------|------------------|
| DateTime       | Used for specifying a date and time from January 1, 1753 to December 31, 9999. It has an accuracy of 3.33 milliseconds. | 8 bytes          | Rounded to increments of .000, .003, .007 | 1753-01-01       | 9999-12-31       |
| smalldatetime  | Used for specifying a date and time from January 1, 0001 to December 31, 9999. It has an accuracy of 100 nanoseconds    | 4 bytes, fixed   | 1 minute                                  | 1900-01-01       | 2079-06-06       |
| date           | Used to store only date from January 1, 0001 to December 31, 9999                                                       | 3 bytes, fixed   | 1 day                                     | 0001-01-01       | 9999-12-31       |
| time           | Used for storing only time only values with an accuracy of 100 nanoseconds.                                             | 5 bytes          | 100 nanoseconds                           | 00:00:00.0000000 | 23:59:59.9999999 |
| datetimeoffset | Similar to datatime but has a time zone offset                                                                          | 10 bytes         | 100 nanoseconds                           | 0001-01-01       | 9999-12-31       |
| datetime2      | Used for specifying a date and time from January 1, 0001 to December 31, 9999                                           | 6 bytes          | 100 nanoseconds                           | 0001-01-01       | 9999-12-31       |

### Character Strings
<br>

<!-- data-transpose data-type="none" -->
|**_Data Type_**| **_Description_**                                                                                  |**_Lower limit_**| **_Upper limit_**   | **_Memory_**      |
|---------------|----------------------------------------------------------------------------------------------------|-----------------|---------------------|-------------------|
| char          | It is a character string with a fixed width. It stores a maximum of 8,000 characters.              | 0 chars         | 8000 chars          | n bytes           |
| varchar       | This is a character string with variable width                                                     | 0 chars         | 8000 chars          | n bytes + 2 bytes |
| varchar (max) | This is a character string with a variable width. It stores a maximum of 1,073,741,824 characters. | 0 chars         | 2^31 chars          | n bytes + 2 bytes |
| text          | This is a character string with a variable width. It stores a maximum 2GB of text data.            | 0 chars         | 2,147,483,647 chars | n bytes + 4 bytes |

### Unicode Character Strings
<br>

<!-- data-transpose data-type="none" -->
| **_Data Type_** | **_Description_**                        | **_Lower limit_** | **_Upper limit_**  | **_Memory_**              |
|-----------------|------------------------------------------|-------------------|--------------------|---------------------------|
| nchar           | It is a Unicode string of fixed width    | 0 chars           | 4000 chars         | 2 times n bytes           |
| nvarchar        | It is a unicode string of variable width | 0 chars           | 4000 chars         | 2 times n bytes + 2 bytes |
| ntext           | It is a unicode string of variable width | 0 chars           | 1,073,741,823 char | 2 times the string length |

### Binary Strings
<br>

<!-- data-transpose data-type="none" -->
| **_Data Type_** | **_Description_**                                                             | **_Lower limit_** | **_Upper limit_**   | **_Memory_**                                |
|-----------------|-------------------------------------------------------------------------------|-------------------|---------------------|---------------------------------------------|
| binary          | It is a fixed width binary string. It stores a maximum of 8,000 bytes.        | 0 bytes           | 8000 bytes          | n bytes                                     |
| varbinary       | This is a binary string of variable width. It stores a maximum of 8,000 bytes | 0 bytes           | 8000 bytes          | The actual length of data entered + 2 bytes |
| image           | This is a binary string of variable width. It stores a maximum of 2GB.        | 0 bytes           | 2,147,483,647 bytes |                                             |

###  Other Data Type
<br>

<!-- data-transpose data-type="none" -->
| **_Data Type_**        | **_Description_**                                                                                            |
|------------------------|--------------------------------------------------------------------------------------------------------------|
| Cursor                 | Its output is a column of sp_cursor_list and sp_describe_cursor. It returns the name of the cursor variable. |
| Row version            | It version stamps table rows.                                                                                |
| Hierarchyid            | This datatype represents a position in the hierarchy                                                         |
| Uniqueidentifier       | Conversion from a character expression.                                                                      |
| Sql_variant            | It stores values of SQL server supported Datatypes.                                                          |
| XML                    | It stores XML data in a column.                                                                              |
| Spatial Geometry type  | It represents data in a flat coordinate system.                                                              |
| Spatial Geography type | It represents data in the round-earth coordinate system.                                                     |
| table                  | It stores a result set for later processing.                                                                 |


## Constraints

* Constraint is used to define rules to allow or restrict what values can be stored in columns. The purpose of inducing constraints is to enforce the integrity of a database.
* Constraint are used to limit the type of data that can be inserted into a table.
* Constraint can be classified into two types - column level and table level.
* The column level Constraint can apply only to one column where as table level constraints are applied to the entire table.
* Constraint is declared at the time of creating a table.

<br>

**SQL Server Constraints are :**


1. NOT NULL
2. UNIQUE
3. PRIMARY KEY
4. FOREIGN KEY
5. DEFAULT
6. CHECK

<br>

### NOT NULL

<br>

The **_NOT NULL_** constraint enforces a column to NOT accept NULL values.

This enforces a field to always contain a value, which means that you cannot insert a new record, or update a record without adding a value to this field.

<br>

NOT NULL Example

```markdown 
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255) NOT NULL,
    Age int
);
```

<br>

### UNIQUE

<br>

The ***UNIQUE*** constraint ensures that all values in a column are different.

<br>

UNIQUE Constraint Example

```markdown
CREATE TABLE Persons (
    ID int NOT NULL UNIQUE,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);

```

### PRIMARY KEY

<br>

The ***PRIMARY KEY*** constraint uniquely identifies each record in a table.

Primary keys must contain UNIQUE values, and cannot contain NULL values.

<br>

PRIMARY KEY Example

```markdown 
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
```
<br>

### FOREIGN KEY

<br>

The ***FOREIGN KEY*** constraint is used to prevent actions that would destroy links between tables.

A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the ***PRIMARY KEY*** in another table.

![image rdbms](image/related-tables.png)

<br>

FOREIGN KEY Example

```markdown
CREATE TABLE orders (
    order_id int NOT NULL,
    product varchar(255),
    total int,
    customer_id int,
    PRIMARY KEY (order_id),
    FOREIGN KEY (customer_id) REFERENCES Persons(order_id)
);
```

### DEFAULT

<br>

The ***DEFAULT*** constraint is used to set a default value for a column.

<br>

DEFAULT Example

```markdown
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
```

### CHECK

<br>

The ***CHECK*** constraint is used to limit the value range that can be placed in a column.

If you define a ***CHECK*** constraint on a column it will allow only certain values for this column.

If you define a ***CHECK*** constraint on a table it can limit the values in certain columns based on values in other columns in the row.

<br>

CHECK Example

```markdown
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int CHECK (Age>=18)
);
```

## Data Definition Language(DDL)

A data definition language (DDL) is a computer language used to create and modify the structure of database objects in a database. These database objects include views, schemas, tables, indexes, etc.

<br>

| **_Object_**          | **_Description_**                                                         |
|-----------------------|---------------------------------------------------------------------------|
|     Table             |     Basic   unit of storage composed     of rows and columns              |
|     View              |     Logically   represents subsets of     data from one or more tables    |
|     Sequence Index    |     Numeric value generator                                               |
|     Index             |     Improves   the performance of     some queries                        |
|     Synonym           |     Gives   alternative names to     objects                              |
| Schema                | collection of database objects associated with a database                 |

<br>

**Data Definition Laungauge Commands are as follows**

1. CREATE
2. ALTER
3. DROP
4. TRUNCATE

### Create Command

create is a DDL SQL command used to create a table ,database & Schema in relational database management system.

The table creation command requires the following details −

*	Name of the table
*	Name of the fields(Column) 
*	Definitions for each field(Datatype)

<br>

Syntax:

```markdown
    /* to create database */
    CREATE DATABASE database_name;

    /* to create schema */
    CREATE SCHEMA schema_name;

    /* to create table */
	CREATE TABLE schema_name.table_name 
	( 
		column_name1 datatype1, 
		column_name2 datatype2, 
		column_name3 datatype3, 
		column_name4 datatype4 
	);
```

<br>

Create Command Example

```markdown

    /* to create database */
    CREATE DATABASE EmployeeManagement;

    /* to create schema */
    CREATE SCHEMA employee;

    /* to create table */
    CREATE TABLE employee.regions (
	    region_id INT IDENTITY(1,1) PRIMARY KEY,
	    region_name VARCHAR (25) DEFAULT NULL
    );

    CREATE TABLE employee.countries (
	    country_id CHAR (2) PRIMARY KEY,
	    country_name VARCHAR (40) DEFAULT NULL,
	    region_id INT NOT NULL,
	    FOREIGN KEY (region_id) REFERENCES employee.regions (region_id)
    );
```

### Alter Command 

Alter statement is used to add, delete or modify columns in an exisiting table

<br>

* **Add column**

The basic syntax of an ALTER TABLE command to add a New Column in an existing table is as follows.

Syntax:

```markdown
    ALTER  TABLE table_name
    ADD column_name datatype;
```

Example:

```markdown 
    ALTER TABLE employee.employees
    ADD resigned_date DATE;
```

<br>

* **Modify column**

The basic syntax of an ALTER TABLE command to change the DATA TYPE of a column in a table is as follows.

Syntax:

```markdown
    ALTER  TABLE  table_name 
    ALTER  COLUMN column_name  datatype;
```

Example:

```markdown
    ALTER TABLE employee.employees
    ALTER COLUMN resigned_date DateTime;
```

<br>

* **Delete column**

The basic syntax of an ALTER TABLE command to DROP COLUMN in an existing table is as follows.

 Syntax:

```markdown
    ALTER  TABLE table_name 
    DROP  COLUMN column_name;
```

Example:

```markdown
    ALTER TABLE employee.employees
    DROP COLUMN resigned_date;
```

<br>

* **Adding constraints**

Example:

```markdown
    ALTER TABLE employee.employees ADD UNIQUE (email);
```

### Drop Command

It is very easy to drop an existing table, but you need to be very careful while deleting any existing table because the data lost will not be recovered after deleting a table. 

<br>

Syntax:

```markdown
    DROP DATABASE database_name;

    DROP  TABLE  table_name;
```

<br>

Example:

```markdown
    /* to drop database */
    DROP DATABASE IF EXISTS EmployeeManagement;

    /* to drop schema */
    DROP SCHEMA IF EXISTS employee;

    /* to drop table */
    DROP TABLE IF EXISTS employee.employees;
```

### Truncate Command

TRUNCATE command removes all the records from a table. But this command will not destroy the table's structure. 

<br>

Syntax:

```markdown 
    TRUNCATE TABLE table_name ;
```

<br>

Example:

```markdown
    TRUNCATE TABLE employee.employees;
```

## Data Manipulation Langauage(DML)

The DML commands in Structured Query Language change the data present in the SQL database. We can easily access, store, modify, update and delete the existing records from the database using DML commands.

DML Commands are :

* Insert Command
* Update Command
* Delete Command

### Insert Command

* The SQL INSERT INTO Statement is used to add new rows of data to a table in the database.
* Only one row is inserted with this syntax.
* Insert a new row containing values for each column.
* List values in the default order of the columns in the table.
* Optionally,list the columns in the insert clause.
* Enclose character and data values within single quotation marks.

<br>

Syntax:

```markdown
INSERT INTO table_name[(column[,column…..])] VALUES (value[,value….]);

```
<br>

Example:

```markdown 
INSERT INTO employee.regions(region_id,region_name) VALUES (1,'Europe');
```

<br>

**Methods of inserting null values:**

* Implict:  Omit the column from the column list
* Explicit:  Specify the null keyword in the values list,specify the empty string(‘’) in the values list for character strings and dates.

### Update Command

* The UPDATE Query is used to modify the existing records in a table. 
* You can use the WHERE clause with the UPDATE query to update the selected rows, otherwise all the rows would be affected.

<br>

Syntax:

```markdown 
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

<br>

Example:

```markdown
UPDATE employee.employees
SET first_name='steve'
WHERE employee_id='100';
```

### Delete Command

* The SQL DELETE Query is used to delete the existing records from a table.
* You can use the WHERE clause with a DELETE query to delete the selected rows, otherwise all the records would be deleted. 

<br>

Syntax:

```markdown 
/* Delete all record from table */
DELETE FROM table_name;

/* To Delete single record */
DELETE FROM table_name WHERE condition;
```

<br>

Example:

```markdown 
/* Delete all record from table */
DELETE FROM employee.employees;

/* To Delete single record */
DELETE FROM employee.employees WHERE employee_id='100';
```

## Data Control Language

It is used to control privileges in Database. To perform any operation in the database, such as for creating tables, sequences or views, a user needs privileges. 

The DCL statements are

* GRANT
* REVOKE 

### Grant Command

It is used to provide any user access privileges or other priviliges for the database.

<br>

Syntax:

```markdown 
/* Grant read only to a User */
GRANT SELECT ON table_name TO user_name;

/* Grant insert,update,delete & select function to a user */
GRANT INSERT, UPDATE, DELETE, SELECT ON table_name TO user_name;
```

<br>

Example:

```markdown
/* Grant read only to a User */
GRANT SELECT ON employee.employees TO user1;

/* Grant insert,update,delete & select function to a user */
GRANT INSERT, UPDATE, DELETE, SELECT ON employee.employees TO user1;
```

### Revoke Command

It is used to take back the privileges from any user, use the REVOKE command.

<br>

Syntax:

```markdown
/* revoke read only from a User */
REVOKE SELECT ON table_name TO user_name;

/* revoke insert,update,delete & select function from a user */
REVOKE INSERT, UPDATE, DELETE, SELECT ON table_name TO user_name;
```

<br>

Example:

```markdown
/* revoke read only from a User */
GRANT SELECT ON employee.employees TO user1;

/* revoke insert,update,delete & select function from a user */
GRANT INSERT, UPDATE, DELETE, SELECT ON employee.employees TO user1;
```

## Transaction Control Language(TCL)

**Database Transactions:**

A transaction begins with the first statement is encounterd and ends when one of the following occurs.

* A commit or rollback statement is issued.
* A DDL statement, such as create is issued.
* A DCL statement is issued.
* The system crashes.
* After one transaction ends, the next executable SQL statement automatically starts the next transaction.
* A DDL statement or a DCL statement is automatically committed and therefore implicitly ends a transaction.

You can control the logic of transactions by using the

* Commit
* Savepoint
* Rollback

### Commit 

* COMMIT command is used to permanently save any transaction into the database.
* When we use any DML command like INSERT, UPDATE or DELETE, the changes made by these commands are not permanent, until the current session is closed, the changes made by these commands can be rolled back.
* To avoid that, we use the COMMIT command to mark the changes as permanent.

<br>

Syntax:

```markdown
/* start a transaction */
BEGIN TRANSACTION;

-- other statements

-- commit the transaction

COMMIT;
```

<br>

Example:

```markdown
    BEGIN TRANSACTION;
    INSERT INTO employee.regions(region_id,region_name) VALUES ('6','India');
    COMMIT;
```

### Savepoint 

SAVEPOINT command is used to temporarily save a transaction so that you can rollback to that point whenever required.

<br>

Syntax:

```markdown
/* start a transaction */
BEGIN TRANSACTION;
SAVE TRANSACTION savepoint_name;
-- other statements

```

<br>

Example:

```markdown
BEGIN TRANSACTION;
SAVE TRANSACTION TransactionA;
INSERT INTO employee.regions(region_id,region_name) VALUES ('6','India');
```

### Rollback 

* This command restores the database to last commited state. It is also used with SAVEPOINT command to jump to a savepoint in an ongoing transaction.
* If we have used the UPDATE command to make some changes into the database, and realise that those changes were not required, then we can use the ROLLBACK command to rollback those changes, if they were not commited using the COMMIT command.

<br>

Syntax:

```markdown
ROLLBACK TRANSACTION savepoint_name;
```

<br>

Example:

```markdown
ROLLBACK TRANSACTION TransactionA;
```

## Data Query/Retrival Language(DQL/DRL)

***SELECT*** statement is used to retrieve the information from database using select statement you can do the following

* **Projection**: It is used to choose columns in a table that you want returned by the query.

* **Selection**: It is used to choose rows in a table that you want returned by your query.

* **Joining**: You can choose the join capability in SQL to bring together data that is stored in            different tables by creating a link between them.

<br>

Syntax:

```markdown
SELECT column1, column2, ...FROM table_name;

/* select all the fields available in the table */
SELECT * FROM table_name;

Select identifies what columns
From identifies which table
```

Example:

```markdown
SELECT * FROM employee.employees;

SELECT employee_id,first_name,last_name FROM employee.employees;
```
<br>

### Arithmetic Expressions:

* Create expressions with number and date data by using arithematic operators
* Operator Precedence : * , / , + , - 
* If the operators within an expression are of same priority then evaluation is done from left to right.

Example:

```markdown
SELECT employee_id,first_name + last_name,salary,(20*salary-100)/2 FROM employee.employees;
```

### Column aliases

* Renames column heading
* It is useful for calculations
* Immediately followed by the column name, there can also be optional keyword AS keyword betweeen the column name and alias.
* Enclose alias name in double quotations if it contains a special characters such as # or $ or is case sensitive.
* Column aliases can be used in both select clause and the order by clause you cannot use column aliases in where clause.

Example:

```markdown
SELECT employee_id , first_name+ ' ' + last_name AS 'full_name' FROM employee.employees;
``` 

### Clauses

* DISTINCT
* WHERE
* ORDER BY
* GROUP BY
* HAVING 

#### DISTINCT

* The SQL DISTINCT keyword is used in conjunction with the SELECT statement to eliminate all the duplicate records and fetching only unique records.
* There may be a situation when you have multiple duplicate records in a table. While fetching such records, it makes more sense to fetch only those unique records instead of fetching duplicate records and can be used for more than one column
* Distinct keyword should be used immediately after the select keyword.
* Distinct can also be used with multiple columns and it affects all the columns selected

Syntax:

```markdown
SELECT DISTINCT column1, column2, ...FROM table_name;
```

Example:

```markdown
SELECT DISTINCT manager_id FROM employee.employees;
```

#### WHERE

* We restrict the rows returned by using the WHERE clause.
* Where restricts the query to rows that meets the condition
* Condition is composed of column names ,expressions constants ,and a comparison operator.
* Where consists of three elements.

        => column name

        => comparison condition

        => column name, constant or list of values

* Character strings and date values are enclosed in single quotation marks.
* The WHERE clause is not only used in the SELECT statement, but it is also used in the UPDATE, DELETE statement, etc.,

Syntax:

```markdown
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example:

```markdown
SELECT first_name + ' ' + last_name AS 'full_name' FROM employee.employees WHERE manager_id='101';
```

#### ORDER BY 

* We sort rows by using order by clause .

        => ASC: ascending order , default

        => DSC: descending order.

* The order by clause comes last in the select statement.
* Order by clause is executed last in the query execution .it is placed last unless the for update clause is used.
* Default sorting is ascending
* Numeric values are displayed with lowest values first ex: 1-999
* Date values are displayed with earliest value first ex: 01-jan-92 before 01-jan-95.
* Character values are displayed in alphabetic order ex: A-Z.
* Null values are displayed last for ascending sequences and first for descending sequences.
* We can also sort by a column number in the select list.

Syntax:

```markdown
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

Example:

```markdown
SELECT first_name + ' ' + last_name AS 'full_name',manager_id 
FROM employee.employees 
ORDER BY manager_id DESC;
```

#### GROUP BY

* We use GROUP BY clause to divide the rows in a table into groups.
* If you include a group function in a select statement, you cannot select individual results as well ,unless the individual column appears in the GROUP BY clause.
* Using WHERE clause you can include rows before dividing them into groups.
* You must include the columns in the GROUP BY clause.
* You cannot use a column alias in the GROUP BY clause.
* By default, rows are sorted by ascending order of the columns included in the group by list. You can override this by using ORDER BY clause.
* You cannot use WHERE clause to restrict groups

Syntax:

```markdown
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

Example:

```markdown
SELECT job_id,
COUNT (job_id) job_count
FROM employee.employees 
GROUP BY job_id
ORDER BY job_id DESC;
```

#### HAVING

* The HAVING Clause enables you to specify conditions that filter which group results appear in the results.
* The WHERE clause places conditions on the selected columns, whereas the HAVING clause places conditions on groups created by the GROUP BY clause.
* The HAVING clause must follow the GROUP BY clause in a query and must also precede the ORDER BY clause if used.

Syntax: 

```markdown
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

Example:

```markdown
SELECT job_id,
COUNT (job_id) job_count
FROM employee.employees 
GROUP BY job_id
HAVING COUNT (job_id) >= 3
ORDER BY job_id DESC;
```

### Logical conditions

<br>

| **_Operator_**        | **_Meaning_**                                                 |
|-----------------------|---------------------------------------------------------------|
|     AND               |     Returns true if both component conditions   are true      |
|     OR                |     Returns true if either component conditions   are true    |
|     NOT               |     Returns true if false, Returns false if   true            |

Example:

* **AND**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE (salary>1000 AND job_id='1');
```

* **OR**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE (salary>5000 OR job_id='5');
```

* **NOT**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE NOT job_id=5;
```

### Comparision conditions

| **_Operator_**  | **_Meaning_**                   |
|-----------------|---------------------------------|
|     =           |     Equal to                    |
|     >           |     Greater than                |
|     >=          |     Greater than or Equal to    |
|     <           |     Less than                   |
|     <=          |     Less than or Equal to       |
|     <>,!=,^=    |     Not equal to                |

Example:

```markdown
SELECT first_name+' '+last_name AS full_name,salary 
FROM employee.employees
WHERE salary>=5000;
```

### Other Comparision operator

* BETWEEN AND
* IN
* LIKE
* IS NULL

#### BETWEEN AND

* BETWEEN and AND are actually translated by the mysql server to a pair of AND conditions (a>=lower limit) AND (a<= higher limit).
* Using BETWEEN AND has no performance benefits, and it is used logical simplicity.

Example:

```markdown
SELECT first_name+' '+last_name AS full_name,salary 
FROM employee.employees
WHERE salary BETWEEN 1000 AND 10000;
```

#### IN

* It is used to test the values in a list. IN condition is also known as member ship condition
* If characters or dates are used in a list they must be enclosed in a single quotation marks .
* IN is actually translated by a mysql server to a set of OR conditions a=value1 or a= value2 or a=value3.
* Using IN has no performance benefits ,and is used for logical simplicity.

Example:

```markdown
SELECT first_name+' '+last_name AS full_name,job_id 
FROM employee.employees
WHERE job_id IN(1,5);
```

#### LIKE

* It is used for performing wildcard searches of valid search string values.
* Search conditions can contain either literal characters or numbers .
* % denotes zero or many characters .
* _ denotes one character or any single character.

Example:

```markdown
SELECT employee_id,first_name
FROM employee.employees
WHERE first_name LIKE 'a%';
```

#### IS NULL
	
Example:

```markdown
SELECT employee_id,first_name,manager_id
FROM employee.employees
WHERE manager_id is NULL;
```

```markdown
SELECT employee_id,first_name,manager_id
FROM employee.employees
WHERE manager_id is NOT NULL;
```

## SQL SERVER FUNCTIONS

### Aggregate functions

SQL-Server aggregate functions retrieve a single value after performing a calculation on a set of values.

<br>

SQL Server provides various aggregate functions, and the most commonly used aggregate functions are shown in the below table:

| **_Aggregate Function_** | **_Descriptions_**                                                                                   |
|--------------------------|------------------------------------------------------------------------------------------------------|
| COUNT()                  | This function counts the number of elements or rows, including NULL values in the defined set.       |
| SUM()                    | This function calculates the total sum of all NON-NULL values in the given set.                      |
| AVG()                    | This function performs a calculation on NON-NULL values to get the average of them in a defined set. |
| MIN()                    | This function returns the minimum (lowest) value in a set.                                           |
| MAX()                    | This function returns the maximum (highest) value in a set.                                          |

<br>

This table shows some other aggregate functions used in SQL Server:

| **_Aggregate Function_** | **_Descriptions_**                                                                                                                                                                                       |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHECKSUM_AGG             | It calculates the checksum of the values in a defined set.                                                                                                                                               |
| COUNT_BIG()              | It counts the number of elements, including NULL values in a defined set. This function is the same as the COUNT() function, but it returns a BIG INT data type, whereas COUNT returns an INT data type. |
| STDEV()                  | It calculates the statistical standard deviation of each value in the defined expression on the basis of a sample data population.                                                                       |
| STDEVP()                 | It calculates the standard deviation for each value in the given expression on the basis of an entire data population.                                                                                   |
| VAR()                    | It calculates the statistical variance of each element in the defined expression on the basis of a sample data population.                                                                               |
| VARP()                   | It calculates the statistical variance of each element in the defined expression on the basis of an entire data population.                                                                              |
| GROUPING()               | It signifies whether or not a GROUP BY lists specified column expression is aggregated. If the result set shows 1, it means the result set is aggregated and, if not, returns 0.                         |
| GROUPING_ID()            | It is used to computes the level of grouping.                                                                                                                                                            |

**COUNT**

SQL Server COUNT() is an aggregate function that returns the number of items found in a set.

Example:

```markdown
SELECT COUNT (*) AS total_employee FROM employee.employees;
```

**SUM**

The SUM() function calculates the sum of a set of values.

Example:

```markdown
SELECT SUM(salary) AS total_salary FROM employee.employees;
```

**AVG**

The AVG() function returns the average value of an expression.

Example:

```markdown
SELECT AVG(salary) AS avg_salary FROM employee.employees;
```

**MAX**

The MAX() function returns the maximum value in a set of values.

Example:

```markdown
SELECT MAX(salary) AS max_salary FROM employee.employees;
```

**MIN**

The MIN() function returns the minimum value in a set of values.

Example:

```markdown
SELECT MIN(salary) AS min_salary FROM employee.employees;
```

### String Functions

SQL string functions are used primarily for string manipulation.

The following table listed each of the functions with a brief description:

| **_Function Name_** | **_Descriptions_**                                                                                                                                         |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASCII               | This function displays the ASCII value of a character.                                                                                                     |
| CHAR                | This function converts the specified integer code (ASCII) into a single-byte character.                                                                    |
| CHARINDEX           | This function returns the first expression's starting position if a character expression is found inside a second character expression.                    |
| CONCAT              | This function returns a single string by joining two or more strings.                                                                                      |
| CONCAT_WS           | This function concatenates multiple strings into a single and spate them with a separator specified in the first position.                                 |
| DIFFERENCE          | This function returns an integer value by comparing the two strings SOUNDEX() values.                                                                      |
| FORMAT              | This function is used to change the text format of the string into any other format.                                                                       |
| LEFT                | This function returns the substring from the left of the string to a specified number of characters.                                                       |
| LEN                 | This function returns the number of characters in a string, including trailing spaces.                                                                     |
| LOWER               | This function is used to convert the upper case character into lower case.                                                                                 |
| LTRIM               | This function returns a string from a given string after removing all leading spaces.                                                                      |
| NCHAR               | This function is used to get the Unicode character with the provided integer code based on the UNICODE standard.                                           |
| PATINDEX            | This function returns the first occurrence of a pattern in a string's starting place. If the string is not found, it returns zero.                         |
| QUOTENAME           | This function returns a Unicode string including the delimiters, converting the input string into a valid delimited identifier.                            |
| REPLACE             | This function is used to replace all occurrences of the substring in a specified string with another string value.                                         |
| REPLICATE           | This function repeats the string with the specified number of times.                                                                                       |
| REVERSE             | This function displays the character string in reverse order.                                                                                              |
| RIGHT               | This function returns the substring from the right of the string to a specified number of characters.                                                      |
| RTRIM               | This function returns a string from a given string after removing all trailing spaces.                                                                     |
| SOUNDEX             | It is used to calculate the similarity of two strings using a four-character (SOUNDEX) code.                                                               |
| SPACE               | This function is used to finds the string of repeated spaces.                                                                                              |
| STR                 | This function is used to return the character data converted from numeric data.                                                                            |
| STRING_AGG          | This function concatenates the values of string expressions and inserts separator values in between. It does not add a separator at the end of the string. |
| STRING_ESCAPE       | This function escapes special characters in a string and produces a new string containing the characters that were escaped.                                |
| STRING_SPLIT        | It is a table-valued function that divides a string into rows of substrings using a separator of your choice.                                              |
| STUFF               | This function removes a portion of a string and replaces it with another substring beginning at a specified position.                                      |
| SUBSTRING           | This function extracts a substring from a string that begins at a specific position and ends at a specific length.                                         |
| TRANSLATE           | This function combines several one-to-one translations into a single operation.                                                                            |
| TRIM                | This function returns a new string after removing all leading and trailing blanks from a given string.                                                     |
| UNICODE             | This function returns a character's integer value as defined by the Unicode standard.                                                                      |
| UPPER               | This function converts the lower case character into the upper case.                                                                                       |

**ASCII**

The ASCII() function returns the ASCII value for the specific character.

Example:

```markdown
SELECT ASCII('A') FROM employee.employees;
SELECT first_name,ASCII(first_name) FROM employee.employees;
```

**CHARINDEX**

The CHARINDEX() function searches for a substring in a string, and returns the position.

Syntax:

```markdown
CHARINDEX(substring, string, start)
```

Example:

```markdown
SELECT CHARINDEX('l', 'Employee') AS Position;
```

**CONCAT**

The CONCAT() function adds two or more strings together.

Example:

```markdown
SELECT CONCAT('employee','name');
```

**SOUNDEX**

The SOUNDEX() function returns a four-character code to evaluate the similarity of two expressions.

Example:

```markdown
SELECT SOUNDEX('employee'), SOUNDEX('location');
```

**DIFFERENCE**

The DIFFERENCE() function compares two SOUNDEX values, and returns an integer. The integer value indicates the match for the two SOUNDEX values, from 0 to 4.

0 indicates weak or no similarity between the SOUNDEX values. 4 indicates strong similarity or identically SOUNDEX values.

Example:

```markdown
SELECT DIFFERENCE('employee','student');
SELECT DIFFERENCE('Juice','Jucy');
```

**LEFT**

The LEFT() function extracts a number of characters from a string (starting from left).

Example:

```markdown
SELECT LEFT (first_name, 2) AS ExtractString FROM employee.employees;
```

**RIGHT**

The RIGHT() function extracts a number of characters from a string (starting from right).

Example:

```markdown
SELECT RIGHT (first_name, 2) AS ExtractString FROM employee.employees;
```

**LOWER**

The LOWER() function converts a string to lower-case.

Example:

```markdown
SELECT LOWER('EMPLOYEE') AS lowercase;
```

**UPPER**

The UPPER() function converts a string to upper-case.

Example:

```markdown
SELECT UPPER('employee') AS uppercase;
```

**LTRIM**

The LTRIM() function removes leading spaces from a string.

Example:

```markdown
SELECT LTRIM('       Employee') AS lefttrim;
```

**RTRIM**

The RTRIM() function removes trailing spaces from a string.

Example:

```markdown
SELECT RTRIM('Employee     ')AS righttrim;
```

**QUOTENAME**

The QUOTENAME() function returns a Unicode string with delimiters added to make the string a valid SQL Server delimited identifier.

Example:

```markdown
SELECT QUOTENAME('Employee','()');
```

**REPLICATE**

The REPLICATE() function repeats a string a specified number of times.

Example:

```markdown
SELECT REPLICATE (first_name, 3) AS Replicate_name FROM employee.employees;
```

### Date Functions

**Returning the current date and time**

| **_Function_**    | **_Descriptions_**                                                                                                                            |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| CURRENT_TIMESTAMP | This function is used to get the current date and time values without including the time zone offset.                                         |
| GETUTCDATE        | This function is used to get the current UTC date and time values as an integer.                                                              |
| GETDATE           | This function is used to get the system's current date and time on which the SQL Server is installed.                                         |
| SYSDATETIME       | This function is used to get the system's current date and time with more fractional second precision without including the time zone offset. |
| SYSUTCDATETIME    | This function is used to get the system's current date and time value based on the UTC timestamp as an integer.                               |
| SYSDATETIMEOFFSET | This function is used to get the system's current date and time with the time zone offset.                                                    |

**Returning the date and time Parts**

| **_Function_** | **_Descriptions_**                                                                               |
|----------------|--------------------------------------------------------------------------------------------------|
| DATENAME       | This function is used to get a portion of the date in day, month, or year as a character string. |
| DATEPART       | This function is used to get the portion of the date as an integer number.                       |
| DAY            | This function is used to get the day value from the input dates as an integer.                   |
| MONTH          | This function is used to get the month value from the input dates as an integer.                 |
| YEAR           | This function is used to get the year value from the input dates as an integer.                  |

**Returning a difference between two dates**

| **_Function_** | **_Descriptions_**                                                                   |
|----------------|--------------------------------------------------------------------------------------|
| DATEDIFF       | This function is to get the difference in a date part of the two input dates values. |

**Modifying dates**

| **_Function_**   | **_Descriptions_**                                                                                              |
|------------------|-----------------------------------------------------------------------------------------------------------------|
| DATEADD          | This function is used to add an integer value to a date part of the input dates and returns the new date value. |
| EOMONTH          | This function is used to get the last day of the month with the specified date and an optional offset.          |
| SWITCHOFFSET     | This function is used to modify the timezone offset of a datetime offset value and preserves the UTC value.     |
| TODATETIMEOFFSET | This function is used to change the DATETIME2 value into a DATETIMEOFFSET value.                                |

**Constructing date and time from their parts**

| **_Function_**          | **_Descriptions_**                                                                    |
|-------------------------|---------------------------------------------------------------------------------------|
| DATEFROMPARTS           | This function is used to get a date value from the specified day, month, or year.     |
| DATETIME2FROMPARTS      | This function is used to get a DATETIME2 value from the date and time arguments.      |
| DATETIMEOFFSETFROMPARTS | This function is used to get a DATETIMEOFFSET value from the date and time arguments. |
| TIMEFROMPARTS           | This function is used to get a time value from the time parts with precision.         |

**Validating date and time values**

| **_Function_** | **_Descriptions_**                                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| ISDATE         | This function is used to check the entered dates follows the standard format of date, time, or datetime value or not. |

#### Returning the current date and time

**CURRENT_TIMESTAMP()**

The CURRENT_TIMESTAMP function returns the current date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT CURRENT_TIMESTAMP AS currentDateAndTime;
```

**GETDATE()**

The GETDATE() function returns the current database system date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT GETDATE() AS currentDate;
```

**GETUTCDATE()**

The GETUTCDATE() function returns the current database system UTC date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT GETUTCDATE();
```

**SYSDATETIME**

The SYSDATETIME() function returns the date and time of the computer where the SQL Server is running.

Example:

```markdown
SELECT SYSDATETIME();
```

**SYSUTCDATETIME**

The SYSUTCDATETIME() function returns the system's current date and time based on the UTC timestamp as an integer.

Example:

```markdown
SELECT SYSUTCDATETIME() AS Date;  
```

**SYSDATETIMEOFFSET()**

The SYSDATETIMEOFFSET() function returns the system's current date and time with the timezone offset.

Example:

```markdown
SELECT SYSDATETIMEOFFSET() AS Date;  
```

#### Returning the date and time Parts

**DATENAME()**

This function is used to get a portion of the date in day, month, or year as a character string.

Example:

```markdown
SELECT DATENAME(yy, '2017/08/25') AS DatePartString;
SELECT DATENAME(month, '2017/08/25') AS DatePartString;
SELECT DATENAME(hour, '2017/08/25 08:36') AS DatePartString;
SELECT DATENAME(minute, '2017/08/25 08:36') AS DatePartString;
SELECT DATENAME(second, '2017/08/25 08:36:58') AS DatePartString;
```

**DATEPART()**

This function is used to get the portion of the date as an integer number.

Example:

```markdown
SELECT DATEPART(yy, '2017/08/25') AS DatePartString;
SELECT DATEPART(month, '2017/08/25') AS DatePartString;
```

**YEAR()**

This function is used to get the year value from the input dates as an integer.

Example:

```markdown
SELECT YEAR(hire_date) AS year FROM employee.employees;
```

**MONTH()**

This function is used to get the month value from the input dates as an integer.

Example:

```markdown
SELECT MONTH(hire_date) AS month FROM employee.employees;
```

**DAY()**

This function is used to get the day value from the input dates as an integer.  

Example:

```markdown
SELECT DAY(hire_date) AS day FROM employee.employees;
```

#### Returning a difference between two dates

**DATEDIFF**

This function is to get the difference in a date part of the two input dates values.

Example:

```markdown
SELECT DATEDIFF(hour, '2017/08/25 07:00', '2017/08/30 12:45') AS HourDiff;
SELECT DATEDIFF(month, '2011/08/25', '2017/08/25') AS MonthDiff;
SELECT DATEDIFF(day, '2011/08/25', '2011/08/30') AS MonthDiff;
```

#### Modifying dates

**DATEADD()**

This function is used to add an integer value to a date part of the input dates and returns the new date value.

Example:

```markdown
SELECT DATEADD(year, 11, hire_date) AS YearAdd FROM employee.employees;
```

**EOMONTH**

This function is used to get the last day of the month with the specified date and an optional offset.   

Example:

```markdown
SELECT EOMONTH(hire_date) AS EndDateoftheMonth FROM employee.employees;
```

**SWITCHOFFSET**

This function is used to modify the timezone offset of a datetime offset value and preserves the UTC value.

Example:

```markdown
SELECT SWITCHOFFSET(hire_date,'-05:00') AS result FROM employee.employees;
```

**TODATETIMEOFFSET**

This function is used to change the DATETIME2 value into a DATETIMEOFFSET value. 

Example:

```markdown
SELECT TODATETIMEOFFSET(GETDATE(),'-05:00') AS result,TODATETIMEOFFSET(GETDATE(),180);
```

#### Constructing date and time from their parts

**DATEFROMPARTS**

This function is used to get a date value from the specified day, month, or year.

Example:

```markdown
SELECT DATEFROMPARTS(2023, 04, 04) AS Result1, DATEFROMPARTS(2023, NULL, 04) AS Result2;  
```

**DATETIME2FROMPARTS**

This function is used to get a DATETIME2 value from the date and time arguments.

Example:

```markdown
SELECT DATETIME2FROMPARTS ( 2023, 10, 31, 11, 59, 59, 0, 0 ) AS Result1,  DATETIME2FROMPARTS(2023, NULL, 31, 11, 59, 59, 0, 0) AS Result2;    
```

**DATETIMEOFFSETFROMPARTS**

This function is used to get a DATETIMEOFFSET value from the date and time arguments.

Example:

```markdown
SELECT DATETIMEOFFSETFROMPARTS(2023, 10, 11, 20, 35, 30, 4000, 10, 30, 4) AS Result1,  
DATETIMEOFFSETFROMPARTS(NULL, 10, 11, 20, 35, 30, 4000, 10, 30, 4) AS Result2;  
```

**TIMEFROMPARTS**

This function is used to get a time value from the time parts with precision.

Example:

```markdown
SELECT TIMEFROMPARTS(20, 55, 59, 55, 3) AS Result1,  TIMEFROMPARTS(10, NULL, 19, 5, 2) AS Result2;  
```

#### Validating date and time values

**ISDATE**

This function is used to check the entered dates follows the standard format of date, time, or datetime value or not.

Example:

```markdown
SELECT ISDATE('2020-25-01') AS Result1, ISDATE('2020-12-06') AS Result2;
```