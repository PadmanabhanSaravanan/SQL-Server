# SQL-Server

![image sql-server-logo](/image/sql-server_logo.png)

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

![image Non-RDBMS](/image/Nosql.png)

Here, customers' data are stored in key-value pairs.

Commonly used Non-RDBMS: MongoDB, Amazon DynamoDB, Redis, etc.

**Relational Database Management System**

In RDBMS, data is stored in tabular format. For example,

![image RDBMS](/image/rdbms.png)

Here, customers is a table inside the database.

The first row is the attributes of the table. Each row after that contains the data of a customer.

In RDBMS, two or more tables may be related to each other. Hence the term "Relational". For example,

![image RDBMS](/image/related-tables.png)

Here, orders and customers are related through customer_id.

Commonly used RDBMS: MySQL, PostgreSQL, MSSQL, Oracle etc.

### What is SQL Server ?

SQL Server is a relational database management system, or RDBMS, developed and marketed by Microsoft.

Similar to other RDBMS software, SQL Server is built on top of SQL, a standard programming language for interacting with relational databases. SQL Server is tied to Transact-SQL, or T-SQL, the Microsoft’s implementation of SQL that adds a set of proprietary programming constructs.

**SQL Server Architecture** 

![image sql-arch](/image/sql-arch.jpg)

SQL Server consists of two main components:

* Database Engine
* SQLOS

**Database Engine**

![image database engine](/image/database-engine.jpg)

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

![image rdbms](/image/related-tables.png)

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

## Data Definition Language

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
    MODIFY  COLUMN column_name  datatype;
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

## Data Manipulation Langauage

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

## Transaction Control Language

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
    INSERT INTO employee.regions(region_id,region_name) VALUES ('7','Sri Lanka');
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
