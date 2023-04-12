# SQL-Server

![image sql-server-logo](image/sql-server_logo.png)

## Table of Content 

1. [**Introduction to SQLServer**](#introduction-to-sqlserver) <!-- style="font-size:20px" -->
2. [**Data Objects**](#data-objects) <!-- style="font-size:20px" -->
3. [**Data Types**](#data-types) <!-- style="font-size:20px" -->
4. [**Constraints**](#constraints)<!-- style="font-size:20px" -->
5. [**Data Definition Language**](#data-definition-language)<!-- style="font-size:20px" -->
6. [**Data Manipulation Langauage**](#data-manipulation-langauage)<!-- style="font-size:20px" -->
7. [**Data Control Language**](#data-control-language)<!-- style="font-size:20px" -->
8. [**Transaction Control Language**](#transaction-control-language)<!-- style="font-size:20px" -->
9. [**Data Query or Retrival Language**](#data-query-or-retrival-language)<!-- style="font-size:20px" -->
10. [**SQL-Server Joins**](#joins)<!-- style="font-size:20px" -->
11. [**SQL-Server Views**](#views)<!-- style="font-size:20px" -->
12. [**SQL-Server Stored Procedure**](#stored-procedure)<!-- style="font-size:20px" -->
13. [**SQL-Server Cursor**](#sql-server-cursor)<!-- style="font-size:20px" -->
14. [**SQL-Server Triggers**](#sql-server-triggers)<!-- style="font-size:20px" -->
15. [**SQL-Server Control flow Statements**](#sql-server-control-flow-statements)<!-- style="font-size:20px" -->
16. [**SQL-Server Functions**](#sql-server-functions)<!-- style="font-size:20px" -->
17. [**Reference**](#reference)<!-- style="font-size:20px" -->

## Introduction to SQLServer

* [**What is Database**](#what-is-database) <!-- style="font-size:20px" -->
* [**What is SQL Server**](#what-is-sql-server) <!-- style="font-size:20px" -->
* [**Installation of SQL Server**](#installation-of-sql-server) <!-- style="font-size:20px" -->
* [**Sample Database**](#sample-database)<!-- style="font-size:20px" -->

### What is Database

A database is a systematic collection of data. They support electronic storage and manipulation of data. Databases make data management easy.

**Types of Databases**

* [Centralized Database](#centralized-database)  
* [Distributed Databse](#distributed-databse) 
* [NoSql Database](#nosql-database) 
* [Cloud Database](#cloud-database) 
* [Relational Database](#relational-database) 
* [Network Database](#network-database) 
* [Object-Oriented Database](#object-oriented-database) 
* [Hierarchical Database](#hierarchical-database) 

#### Centralized Database

A centralized database is stored at a single location such as a mainframe computer. It is maintained and modified from that location only and usually accessed using an internet connection such as a LAN or WAN. The centralized database is used by organisations such as colleges, companies, banks etc.

![img centralized](image/Centralized.png)

#### Distributed Databse

A distributed database is basically a database that is not limited to one system, it is spread over different sites, i.e, on multiple computers or over a network of computers.

![img distributed](image/distributed.jpg)

#### NoSql Database

NoSQL Database is a non-relational Data Management System, that does not require a fixed schema.

![img nosql](image/Nosql-1.png)

#### Cloud Database

A cloud database is a database service built and accessed through a cloud platform. It serves many of the same functions as a traditional database with the added flexibility of cloud computing.

![img cloud](image/cloud.png)

#### Relational Database

A relational database organizes data into rows and columns, which collectively form a table. Data is typically structured across multiple tables, which can be joined together via a primary key or a foreign key.

![img relational](image/relational.png)

#### Network Database

A network database is a type of database model wherein multiple member records or files can be linked to multiple owner files and vice versa.

![img network](image/network.png)

#### Object-Oriented Database

object-oriented database management system is the data model in which data is stored in form of objects, which are instances of classes. These classes and objects together make an object-oriented data model.

![img oops](image/oops.png)

#### Hierarchical Database

A hierarchical model represents the data in a tree-like structure in which there is a single parent for each record.

![img Hierarchical](image/hierarchical.png)

### What is SQL Server

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

### Installation of SQL Server
<br>

* [**Normal Installation**](#normal-installation) 
* [**Docker SQL Server Installation**](#docker-sql-server-installation)

#### Normal Installation 

* [**Download SQL-Server**](#download-sql-server)
* [**Install SQL-Server**](#install-sql-server)
* [**Install SQL-Server Management Studio**](#install-sql-server-management-studio)
* [**Connect to SQL-Server**](#connect-to-sql-server)

##### Download SQL-Server

**Step 1:** Go to the official page through this URL: https://www.microsoft.com/en-in/sql-server/sql-server-downloads.

**Step 2:** Sekect the Developer version ,Click on the "Download now" button. Immediately the SQL Server setup starts downloading on our system.
![image sql-step1](image/sql-step-1.PNG)

**Step 3:** Once the file has been downloaded, we will get the setup named "SQL2022-SSEI-DEV.exe."
![image sql-step2](image/sql-step-2.PNG)

##### Install SQL-server

**Step 1:** Double click on "SQL2022-SSEI-DEV.exe" setup file. We will get the below screen with three options: Basic, Custom, and Download Media files. Here, we will select the 'Basic' option to install the basic version that includes all of the default configurations needed to learn Microsoft SQL Server.
![image install-sql-server](image/install-ms-sql-step1.png)

**Step 2:** Next, the installer will ask where to save the download. Once selected press Install.

![image install-sql-server](image/install-ms-sql-server2.png)

**Step 3:** This will download and run the install package.
![image install-sql-server](image/install-ms-sql-server3.png)

**Step 4:** The SQL Server Installation Center will open after the download completes and on the Installation page, we have the following install options:
![image install-sql-server](image/install-ms-sql-server4.png)
We will pick "New SQL Server stand-alone installation or add features to an existing installation".

**Step 5:** On the next screen, you can enter a product key or use a free edition. The free evaluation edition is good for 180 days, which is what we will use.
![image install-sql-server](image/install-ms-sql-server5.png)

**Step 6:** Read the license terms to make sure that you agree and press Next.
![image install-sql-server](image/install-ms-sql-server6.png)

**Step 7:** The Microsoft Update can check if there are updates. You can enable this option and Microsoft Update will check for updates. Press Next to continue.
![image install-sql-server](image/install-ms-sql-server7.png)

**Step 8:** The install rules window verifies possible problems during the installation.
![image install-sql-server](image/install-ms-sql-server8.png)

**Step 9:** Feature Selection, Select Database Engine Service
![image install-sql-server](image/install-ms-sql-server10.png)

**Step 10:** In the instance configuration, we enter a name to be used for the SQL Server instance.
![image install-sql-server](image/install-ms-sql-server11.png)

**Step 11:** The server configuration allows creating or adding service accounts for the different services used by SQL Server. You can use the defaults or create new accounts with custom security and passwords to run the services.
![image install-sql-server](image/install-ms-sql-server12.png)

**Step 12:** The database engine configuration allows you to configure several parts of the installation.
![image install-sql-server](image/install-ms-sql-server13.png)

**Step 13:** Once everything is configured, you can check the configuration and press the Install button to continue.
![image install-sql-server](image/install-ms-sql-server14.png)

**Step 14:** If everything is successful, MS SQL Server 2022 will be installed, and the relational database management system is ready for use.
![image install-sql-server](image/install-ms-sql-server15.png)

##### Install SQL-Server Management Studio

**Step 1:** Click to download sql server management studio from below link

https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16

double-click the installation file SSMS-Setup-ENU.exe to launch the SSM installer. The installation process of SMSS is straightforward. you need to follow the screen sequence.

**Step 2:** Click the Install button
![image install-sql-server](image/install-SSMS-step-1-1.png)

**Step 3:** Wait for a few minutes while the installer sets up the software:
![image install-sql-server](image/install-SSMS-step-2-1.png)

**Step 4:** Once setup is completed, click the Close button:
![image install-sql-server](image/install-SSMS-step-3-1.png)
Now, you should have SQL Server 2022  and SQL Server Management Studio installed on your computer.

##### Connect to SQL Server

**Step 1:** First, launch the Microsoft SQL Server Management Studio from the Start menu:
![image connect-sql-server](image/SSMS-connect-to-SQL-Server.png)

**Step 2:** Next, from the Connect menu under the Object Explorer, choose the Database Engine…
![image connect-sql-server](image/SSMS-connect-to-SQL-Server-2.png)

**Step 3:** Then, enter the information for the Server name (localhost), Authentication (SQL Server Authentication), and password for the  sa user and click the Connect button to connect to the SQL Server. Note that you should use the sa user and password that you entered during the installation.
![image connect-sql-server](image/SSMS-connect-to-SQL-Server-3.png)

**Step 4:** if the connection is established successfully, then you will see the following Object Explorer panel:
![image connect-sql-server](image/SSMS-connect-to-SQL-Server-4.png)

#### Docker SQL Server Installation

**Step 1:** Install Docker to the system click on below link to download and then install .

https://docs.docker.com/desktop/install/windows-install/


**Step 2:** Now that you’ve installed Docker, you can open up the terminal and supply the following command to check if Docker has been successfully installed on your device:

```markdown
docker -v 
```

Output:

![image docker](image/docker-1.jpg)

**Step 3:** As you can see from the figure above, Docker has been installed successfully and you can see the installed version as well. With Docker up and running, the next step is to pull the official SQL Server Docker image from Docker Hub and get down to brass tacks.

Next, you will be creating a directory for this exercise and opening the terminal in that directory. Once in the directory, run the command given below to pull the docker image from the repository to your local device:

```markdown
 docker pull mcr.microsoft.com/mssql/server
```

Output:

![image docker](image/docker-2.jpg)

**Step 4:** Once the SQL Server Docker Image has been pulled and extracted, you need to start the SQL Server Docker Container for this image. A Container in Docker is a running instance of the Docker image that can be started by performing the command as follows:

```markdown
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<YourStrong@Passw0rd>" -p 1433:1433 --name sql1 --hostname sql1 -d mcr.microsoft.com/mssql/server:2022-latest
```

Output:

![image docker](image/docker-3.jpg)

**Step 5:** As visible from the figure above, on running the command as mentioned in the previous step, an ID is returned. This is the unique ID of the SQL Server Docker Container that is currently running the SQL Server Instance. You can also verify the containers that currently running by leveraging the command as follows:

```markdown
docker container ls 
```

![image docker](image/docker-4.jpg)

### Sample Database 

Click on the link for sample database [link](https://github.com/PadmanabhanSwayaan/SQL-Server/tree/sqlserver-v15.0/sql)

## Data Objects 

A database object is any defined object in a database that is used to store or reference data.Anything which we make from create command is known as Database Object.It can be used to hold and manipulate the data.Some of the examples of database objects are : view, sequence, indexes, etc.

<br>

| **_Object_**          | **_Description_**                                                         |
|-----------------------|---------------------------------------------------------------------------|
|     Table             |     Basic   unit of storage composed     of rows and columns              |
|     View              |     Logically   represents subsets of     data from one or more tables    |
|     Sequence Index    |     Numeric value generator                                               |
|     Index             |     Improves   the performance of     some queries                        |
|     Synonym           |     Gives   alternative names to     objects                              |
| Schema                | collection of database objects associated with a database                 |

## Data Types

A Data Type in SQL server is defined as the type of data that any column or variable can store. It is a type of data that an object holds like integer, character, string, etc.

The Different types of datatypes are :

* [**Exact Numeric**](#exact-numeric)
* [**Approximate Numeric**](#approximate-numeric)
* [**Date & Time**](#date-and-time)
* [**Character Strings**](#character-strings)
* [**Unicode Character Strings**](#unicode-character-strings)
* [**Binary Strings**](#binary-strings)
* [**Other DataTypes**](#other-data-type)

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

### Date and Time
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


1. [NOT NULL](#not-null)
2. [UNIQUE](#unique)
3. [PRIMARY KEY](#primary-key)
4. [FOREIGN KEY](#foreign-key)
5. [DEFAULT](#default)
6. [CHECK](#check)

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

Output:

![image output](image/output66.PNG)

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

Output:

![image output](image/output67.PNG)

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
Output:

![image output](image/output68.PNG)

### FOREIGN KEY

<br>

The ***FOREIGN KEY*** constraint is used to prevent actions that would destroy links between tables.

A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the ***PRIMARY KEY*** in another table.

![image rdbms](image/related-tables.png)

<br>

FOREIGN KEY Example

```markdown
CREATE TABLE Customers (
  id INT,
  first_name VARCHAR(40),
  last_name VARCHAR(40),
  age INT,
  country VARCHAR(10),
  CONSTRAINT CustomersPK PRIMARY KEY (id)
);

CREATE TABLE Orders (
  order_id INT,
  item VARCHAR(40),
  amount INT,
  customer_id INT REFERENCES Customers(id),
  CONSTRAINT OrdersPK PRIMARY KEY (order_id)
);
```

Output:

![image output](image/output69.PNG)

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

Output:

![image output](image/output70.PNG)

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

Output:

![image output](image/output71.PNG)

## Data Definition Language

A data definition language (DDL) is a computer language used to create and modify the structure of database objects in a database. These database objects include views, schemas, tables, indexes, etc.

**Data Definition Laungauge Commands are as follows**

1. [CREATE](#create-command)
2. [ALTER](#alter-command)
3. [DROP](#drop-command)
4. [TRUNCATE](#truncate-command)

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
CREATE DATABASE EmployeeManagement;
GO

    /* to create schema */
CREATE SCHEMA employees;
GO

    /* to create table */
CREATE TABLE employees.regions (
	    region_id INT IDENTITY(1,1) PRIMARY KEY,
	    region_name VARCHAR (25) DEFAULT NULL
    );

CREATE TABLE employees.countries (
	    country_id CHAR (2) PRIMARY KEY,
	    country_name VARCHAR (40) DEFAULT NULL,
	    region_id INT NOT NULL,
	    FOREIGN KEY (region_id) REFERENCES employees.regions (region_id)
    );
```

Output:

![image output](image/output72.PNG)

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

Output:

![image output](image/output73.PNG)

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

Output:

![image output](image/output74.PNG)

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

Output:

![image output](image/output75.PNG)

<br>

* **Adding constraints**

Example:

```markdown
    ALTER TABLE employee.employees ADD UNIQUE (email);
```

Output:

![image output](image/output76.PNG)

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

Output:

![image output](image/output77.PNG)

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

Output:

![image output](image/output78.PNG)

## Data Manipulation Langauage

The DML commands in Structured Query Language change the data present in the SQL database. We can easily access, store, modify, update and delete the existing records from the database using DML commands.

DML Commands are :

* [Insert Command](#insert-command)
* [Update Command](#update-command)
* [Delete Command](#delete-command)

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

Output:

![image output](image/output79.PNG)

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
WHERE employee_id='101';
```

Output:

![image output](image/output80.PNG)

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
DELETE FROM employee.employees WHERE employee_id='101';
```

Output:

![image output](image/output81.PNG)

## Data Control Language

It is used to control privileges in Database. To perform any operation in the database, such as for creating tables, sequences or views, a user needs privileges. 

The DCL statements are

* [GRANT](#grant-command)
* [REVOKE](#revoke-command) 

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

Output:

![image output](image/output82.PNG)

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
REVOKE SELECT ON employee.employees TO user1;

/* revoke insert,update,delete & select function from a user */
REVOKE INSERT, UPDATE, DELETE, SELECT ON employee.employees TO user1;
```

Output:

![image output](image/output83.PNG)

## Transaction Control Language

**Database Transactions:**

A transaction begins with the first statement is encounterd and ends when one of the following occurs.This command is used to manage changes to DML statements.

* A commit or rollback statement is issued.
* A DDL statement, such as create is issued.
* A DCL statement is issued.
* The system crashes.
* After one transaction ends, the next executable SQL statement automatically starts the next transaction.
* A DDL statement or a DCL statement is automatically committed and therefore implicitly ends a transaction.

You can control the logic of transactions by using the

* [Commit](#commit)
* [Savepoint](#savepoint)
* [Rollback](#rollback)

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
    INSERT INTO employee.regions(region_id,region_name) VALUES ('10','India');
    COMMIT;
```

Output:

![image output](image/output84.PNG)

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
INSERT INTO employee.regions(region_id,region_name) VALUES ('11','India');
```

Output:

![image output](image/output85.PNG)

![image output](image/output86.PNG)

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

Output:

![image output](image/output87.PNG)

in below image region id 11 is been roll backed

![image output](image/output88.PNG)

## Data Query or Retrival Language

**SELECT** statement is used to retrieve the information from database using select statement you can do the following

* **Projection**: It is used to choose columns in a table that you want returned by the query.

* **Selection**: It is used to choose rows in a table that you want returned by your query.

* **Joining**: You can choose the join capability in SQL to bring together data that is stored in different tables by creating a link between them.

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

Output:

![image output](image/output89.PNG)

<br>

### Arithmetic Expressions:

* Create expressions with number and date data by using arithematic operators
* Operator Precedence : * , / , + , - 
* If the operators within an expression are of same priority then evaluation is done from left to right.

Example:

```markdown
SELECT employee_id,first_name + last_name,salary,(20*salary-100)/2 FROM employee.employees;
```

Output:

![image output](image/output90.PNG)

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

Output:

![image output](image/output91.PNG)

### Clauses

* [DISTINCT](#distinct)
* [WHERE](#where)
* [ORDER BY](#order-by)
* [GROUP BY](#group-by)
* [HAVING](#having) 

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

Output:

![image output](image/output92.PNG)

#### WHERE

* We restrict the rows returned by using the WHERE clause.
* Where restricts the query to rows that meets the condition
* Condition is composed of column names ,expressions constants ,and a comparison operator.
* Where consists of three elements.

        -column name

        -comparison condition

        -column name, constant or list of values

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

Output:

![image output](image/output93.PNG)

#### ORDER BY 

* We sort rows by using order by clause .

        -ASC: ascending order , default

        -DSC: descending order.

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

Output:

![image output](image/output94.PNG)

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

Output:

![image output](image/output95.PNG)

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

Output:

![image output](image/output96.PNG)

### Logical conditions

<br>

| **_Operator_**        | **_Meaning_**                                                 |
|-----------------------|---------------------------------------------------------------|
|     AND               |     Returns true if both component conditions   are true      |
|     OR                |     Returns true if either component conditions   are true    |
|     NOT               |     Returns true if false, Returns false if   true            |

Examples:

* **AND**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE (salary>1000 AND job_id='1');
```

Output:

![image output](image/output97.PNG)

* **OR**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE (salary>5000 OR job_id='5');
```

Output:

![image output](image/output98.PNG)

* **NOT**

```markdown
SELECT first_name+' '+last_name AS full_name,salary,job_id 
FROM employee.employees
WHERE NOT job_id=5;
```

Output:

![image output](image/output99.PNG)

### Comparision conditions

| **_Operator_**  | **_Meaning_**                   |
|-----------------|---------------------------------|
|     =           |     Equal to                    |
|      >          |     Greater than                |
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

Output:

![image output](image/output100.PNG)

### Other Comparision operator

* [BETWEEN AND](#between-and)
* [IN](#in)
* [LIKE](#like)
* [IS NULL](#is-null)

#### BETWEEN AND

* BETWEEN and AND are actually translated by the sql server server to a pair of AND conditions (a>=lower limit) AND (a<= higher limit).
* Using BETWEEN AND has no performance benefits, and it is used logical simplicity.

Example:

```markdown
SELECT first_name+' '+last_name AS full_name,salary 
FROM employee.employees
WHERE salary BETWEEN 1000 AND 10000;
```

Output:

![image output](image/output101.PNG)

#### IN

* It is used to test the values in a list. IN condition is also known as member ship condition
* If characters or dates are used in a list they must be enclosed in a single quotation marks .
* IN is actually translated by a sql server to a set of OR conditions a=value1 or a= value2 or a=value3.
* Using IN has no performance benefits ,and is used for logical simplicity.

Example:

```markdown
SELECT first_name+' '+last_name AS full_name,job_id 
FROM employee.employees
WHERE job_id IN(1,5);
```

Output:

![image output](image/output102.PNG)

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

Output:

![image output](image/output103.PNG)

#### IS NULL
	
Example:

```markdown
SELECT employee_id,first_name,last_name
FROM employee.employees
WHERE phone_number is NULL;
```

Output:

![image output](image/output104.PNG)

## Joins 

SQL Server (Transact-SQL) JOINS are used to retrieve data from multiple tables. A SQL Server JOIN is performed whenever two or more tables are joined in a SQL statement.

There are 4 different types of SQL Server joins:

* [INNER JOIN](#inner-join) 
* [LEFT JOIN](#left-join) 
* [RIGHT JOIN](#right-join)
* [FULL JOIN](#full-join)

### INNER JOIN

The INNER JOIN keyword selects records that have matching values in both tables.

Syntax:

```markdown
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

<br>

Example:

```markdown
SELECT departments.location_id,locations.city
FROM employee.departments
INNER JOIN employee.locations
ON departments.location_id = locations.location_id;
```

Output:

![image output](image/output1.PNG)

### LEFT JOIN

The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

Syntax:

```markdown
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

Example:

```markdown
SELECT departments.location_id,locations.city
FROM employee.locations
LEFT JOIN employee.departments
ON locations.location_id = departments.location_id;
```

Output:

![image output](image/output2.PNG)

### RIGHT JOIN

The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.

Syntax:

```markdown
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

Example:

```markdown
SELECT employees.employee_id, employees.first_name AS Parent ,dependents.first_name AS Child
FROM employee.employees
RIGHT JOIN employee.dependents
ON employees.employee_id = dependents.employee_id
ORDER BY employees.employee_id ASC;
```

Output:

![image output](image/output3.PNG)

### FULL JOIN

The FULL JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.

Syntax:

```markdown
SELECT column_name(s)
FROM table1
FULL JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

Example:

```markdown
SELECT employees.employee_id, employees.first_name AS Parent ,dependents.first_name AS Child
FROM employee.employees
FULL JOIN employee.dependents
ON employees.employee_id = dependents.employee_id
ORDER BY employees.employee_id;
```

Output:

![image output](image/output4.PNG)

## Views

* View is a data object which does not contain any data. 
* Contents of the view are the resultant of a base table. They are operated just like base table but they don’t contain any data of their own. 
* The difference between a view and a table is that views are definitions built on top of other tables (or views).
* If data is changed in the underlying table, the same change is reflected in the view. 
* A view can be built on top of a single or multiple tables.
* Views can have column names and expressions.
* You can use any clauses in views.
* Views can be used in INSERT/UPDATE/DELETE.
* Views can contain expressions in the select list.

View Commands are:

* [Create View](#create-view)
* [Alter View](#alter-view)
* [Drop View](#drop-view)

### Create View 

A view is created with the CREATE VIEW statement. 

Syntax:

```markdown 
CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example:

```markdown
USE Employee;
GO

CREATE VIEW employee.employee_relationship AS
SELECT employees.employee_id, employees.first_name AS Parent ,dependents.first_name AS Child
FROM employee.employees
FULL JOIN employee.dependents
ON employees.employee_id = dependents.employee_id;
```

Output:

![image output](image/output5.PNG)

### Alter View 

A view can be updated with the ALTER VIEW statement.

Syntax:

```markdown
ALTER VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example:

```markdown
ALTER VIEW employee.employee_relationship AS
SELECT employees.employee_id, employees.first_name AS Parent,employees.last_name ,dependents.first_name AS Child
FROM employee.employees
FULL JOIN employee.dependents
ON employees.employee_id = dependents.employee_id;
```

Output:

![image output](image/output6.PNG)

### Drop View

A view is deleted with the DROP VIEW statement.

Syntax:

```markdown
DROP VIEW view_name;
```

Example:

```markdown
DROP VIEW employee.employee_relationship;
```

Output:

![image output](image/output7.PNG)

## Stored Procedure

* A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.
* So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.
* You can also pass parameters to a stored procedure, so that the stored procedure can act based on the parameter value(s) that is passed.

1. [Create Procedure](#create-procedure)
2. [Execute Procedure](#execute-procedure)
3. [Alter Procedure](#alter-procedure)
4. [Drop Procedure](#drop-procedure)
5. [Stored Procedure Parameter](#stored-procedure-parameter)
6. [Stored Procedure Variable](#stored-procedure-variable)

### Create Procedure

A procedure is created with the CREATE PROCEDURE statement. 

Syntax:

```markdown
CREATE PROCEDURE procedure_name
AS
BEGIN
sql_statement
END;
```

Example:

```markdown
CREATE PROCEDURE employee.emoloyee_children
AS
BEGIN
SELECT employees.employee_id, employees.first_name AS Parent ,dependents.first_name AS Child
FROM employee.employees
FULL JOIN employee.dependents
ON employees.employee_id = dependents.employee_id;
END;
```

Output:

![image output](image/output8.PNG)

### Execute Procedure

A Procedure is executed using EXECUTE OR EXEC statement.

Syntax:

```markdown
EXEC procedure_name;
```

Example:

```markdown
EXEC employee.emoloyee_children;
```

Output:

![image output](image/output9.PNG)

### Alter Procedure

A Procedure is modified using ALTER PROCEDURE statement.

Syntax:

```markdown
ALTER PROCEDURE procedure_name
AS
BEGIN
sql_statement
END;
```

Example:

```markdown
ALTER PROCEDURE employee.emoloyee_children
AS
BEGIN
SELECT employees.employee_id, employees.first_name+' '+employees.last_name AS Parent ,dependents.first_name AS Child
FROM employee.employees
FULL JOIN employee.dependents
ON employees.employee_id = dependents.employee_id;
END;
```
Output:

![image output](image/output10.PNG)

Executing procedure after altering procudere:

![image output](image/output11.PNG)

### Drop Procedure

A Procedure is droped using DROP PROCEDURE statement.

Syntax:

```markdown
DROP PROCEDURE procedure_name
```

Example:

```markdown
DROP PROCEDURE employee.emoloyee_children;
```

Output:

![image output](image/output12.PNG)

### Stored Procedure Parameter

* [Creating a stored procedure with one parameter](#creating-a-stored-procedure-with-one-parameter)
* [Creating a stored procedure with multiple parameters](#creating-a-stored-procedure-with-multiple-parameters)
* [Creating text parameters](#creating-text-parameters)
* [Creating optional parameters](#creating-optional-parameters)

#### Creating a stored procedure with one parameter

Example:

```markdown
CREATE PROCEDURE employee.minsalary(@min_salary AS DECIMAL)
AS
BEGIN
    SELECT
        first_name+' '+last_name AS full_name,
        salary
    FROM 
    employee.employees    
      WHERE
        salary >= @min_salary
    ORDER BY
        salary;
END;
```

Execute Query:

```markdown
EXEC employee.minsalary 10000;
```

Output:

![image output](image/output13.PNG)

![image output](image/output14.PNG)

#### Creating a stored procedure with multiple parameters

Example:

```markdown
CREATE PROCEDURE employee.salary(@min_salary AS DECIMAL,@max_salary AS DECIMAL)
AS
BEGIN
    SELECT
        first_name+' '+last_name AS full_name,
        salary
    FROM 
    employee.employees    
      WHERE
        salary >= @min_salary AND
		salary <= @max_salary
    ORDER BY
        salary;
END;
```

Execute Query:

```markdown
EXEC employee.salary 5000,10000;
```

Output:

![image output](image/output15.PNG)

![image output](image/output16.PNG)

#### Creating text parameters

Example:

```markdown
CREATE PROCEDURE employee.name(@min_salary AS DECIMAL,
                               @max_salary AS DECIMAL,
							   @name AS VARCHAR(max))
AS
BEGIN
    SELECT
        first_name,
        salary
    FROM 
    employee.employees    
      WHERE
        salary >= @min_salary AND
		salary <= @max_salary AND
		first_name LIKE '%' + @name + '%'
    ORDER BY
        salary;
END;
```

Execute Query:

```markdown
EXEC employee.name 5000,10000,'ALEX';
```

Output:

![image output](image/output17.PNG)

![image output](image/output18.PNG)

#### Creating optional parameters

Example:

```markdown
CREATE PROCEDURE employee.optionalprocedure(@min_salary AS DECIMAL = 0,
                               @max_salary AS DECIMAL = 15000,
							   @name AS VARCHAR(max))
AS
BEGIN
    SELECT
        first_name,
		last_name,
        salary
    FROM 
    employee.employees    
      WHERE
        salary >= @min_salary AND
		salary <= @max_salary AND
		first_name LIKE '%' + @name + '%'
    ORDER BY
        salary;
END;
```

Execute Query:

```markdown
EXEC employee.optional @min_salary = 0, @max_salary = 15000 , @name = 'jo';
```

Output:

![image output](image/output19.PNG)

![image output](image/output20.PNG)

### Stored Procedure Variable

A variable is an object that holds a single value of a specific type e.g., integer, date, or varying character string.

* Declaring a variable

To declare a variable use the DECLARE statement.

```markdown
DECLARE @min_salary DECIMAL;
```

* Assigning a value to a variable

To assign value to variable use SET statement.

```markdown
SET @min_salary = 0;
```

Example:

```markdown
CREATE PROCEDURE employee.variable(@name AS VARCHAR(max))
AS
BEGIN

DECLARE @min_salary DECIMAL;
DECLARE @max_salary DECIMAL;

SET @min_salary = 0;
SET @max_salary = 15000;

     SELECT
        first_name,
		last_name,
        salary
    FROM 
    employee.employees    
      WHERE
        salary >= @min_salary AND
		salary <= @max_salary AND
		first_name LIKE '%' + @name + '%'
    ORDER BY
        salary;
END;
```

Execute Query:

```markdown
EXEC employee.variable @name='ha';
```

Output:

![image output](image/output21.PNG)

![image output](image/output22.PNG)

## SQL-Server Cursor

* A database cursor is a control structure that enables traversal over the records in a database. Cursors are used by database programmers to process individual rows returned by database system queries. 
* Cursors enable manipulation of whole result sets at once. In this scenario, a cursor enables the rows in a result set to be processed sequentially. 
* In SQL procedures, a cursor makes it possible to define a result set (a set of data rows) and perform complex logic on a row by row basis. 
* SQL Server supports cursors inside stored programs. The syntax is as in embedded SQL. Cursors have these properties

    1. Asensitive: The server may or may not make a copy of its result table
    2. Read only: Not updatable
    3. Nonscrollable: Can be traversed only in one direction and cannot skip rows

SQL Server Cursor Life Cycle:

![image cursor](image/SQL-Server-Cursor.png)

### To use cursors in SQL-Server Procedures

**Declare a cursor:**

The following statement declares a cursor and associates it with a SELECT statement that retrieves the rows to be traversed by the cursor.

```markdown
DECLARE cursor_name 
CURSOR FOR select_statement
```

**Open a cursor:**

The following statement opens a previously declared cursor.

```markdown
OPEN cursor_name
```

**Fetch the data into variables :**

This statement fetches the next row for the SELECT statement associated with the specified cursor (which must be open) and advances the cursor pointer.

If a row exists, the fetched columns are stored in the named variables. The number of columns retrieved by the SELECT statement must match the number of output variables specified in the FETCH statement.

```markdown
FETCH NEXT FROM cursor INTO variable_list;
```

**Close the cursor when done :**

This statement closes a previously opened cursor. An error occurs if the cursor is not open.

```markdown
CLOSE cursor_name
```

**Deallocate the cursor:**

It is used to delete a cursor and releases all resources used by cursor.

```markdown
DEALLOCATE cursor_name
```

### Example:

```markdown
CREATE PROCEDURE employee.employeesalary(@salary AS Decimal,@name AS VARCHAR(max))
AS
BEGIN

DECLARE EmployeeCursor CURSOR FOR 
SELECT first_name+' '+last_name AS full_name,salary FROM employee.employees
WHERE
		salary <= salary AND
		first_name LIKE '%' + @name + '%'

OPEN EmployeeCursor 

FETCH NEXT FROM EmployeeCursor INTO @name,@salary

WHILE(@@FETCH_STATUS = 0)
BEGIN 

	PRINT @name +' = ' + CAST(@salary AS varchar)

	FETCH NEXT FROM EmployeeCursor INTO @name,@salary
END

CLOSE EmployeeCursor

DEALLOCATE EmployeeCursor

END;
```

Execute Query:

```markdown
EXEC employee.employeesalary 15000,'jo';
```

Output:

![image output](image/output28.PNG)

![image output](image/output29.PNG)

## SQL-Server Triggers

SQL Server triggers are special stored procedures that are executed automatically in response to the database object, database, and server events.

SQL Server provides three type of triggers:

* Data manipulation language (DML) triggers which are invoked automatically in response to INSERT, UPDATE, and DELETE events against tables.
* Data definition language (DDL) triggers which fire in response to CREATE, ALTER, and DROP statements. DDL triggers also fire in response to some system stored procedures that perform DDL-like operations.

<br>

1. [Creating Triggers in SQL-Server](#sql-server-create-trigger)
2. [SQL Server INSTEAD OF Trigger](#sql-server-instead-of-trigger)
3. [SQL Server DDL Trigger](#sql-server-ddl-trigger)
4. [SQL Server DISABLE TRIGGER](#sql-server-disable-trigger)
5. [SQL Server ENABLE TRIGGER](#sql-server-enable-trigger)
6. [SQL Server MODIFY TRIGGER](#modify-trigger)
7. [SQL Server DROP TRIGGER](#sql-server-drop-trigger)

### SQL-Server Create Trigger

The CREATE TRIGGER statement allows you to create a new trigger that is fired automatically whenever an event such as INSERT, DELETE, or UPDATE occurs against a table.

Syntax:

```markdown
CREATE TRIGGER [schema_name.]trigger_name
ON table_name
AFTER  {[INSERT],[UPDATE],[DELETE]}
[NOT FOR REPLICATION]
AS
{sql_statements}
```

1. **Create a table for logging the changes**

```markdown
CREATE TABLE employee.regions_log (
	change_id INT IDENTITY PRIMARY KEY,
	region_id INT NOT NULL,
	region_name VARCHAR (25) DEFAULT NULL,
	updated_at DATETIME NOT NULL,
    operation CHAR(3) NOT NULL,
    CHECK(operation = 'INS' or operation='DEL')
);
```

Output:

![image output](image/output30.PNG)

2. **Creating an after DML trigger**

```markdown
CREATE TRIGGER employee.region_trigger
ON employee.regions
AFTER INSERT,DELETE
AS
BEGIN 
     SET NOCOUNT ON;
	 INSERT INTO employee.regions_log(region_id,region_name,updated_at,operation)
	 SELECT i.region_id,i.region_name,GETDATE(),'INS'
	 FROM inserted i
	 UNION ALL 
	 SELECT d.region_id,d.region_name,GETDATE(),'DEL'
	 FROM deleted d;
END
```

Output:

![image output](image/output31.PNG)

3. **Testing the trigger**

```markdown
SET IDENTITY_INSERT employee.regions ON

INSERT INTO employee.regions(region_id,region_name) VALUES (10,'INDIA')
```

Output:

![image output](image/output32.PNG)

```markdown
SELECT * FROM employee.regions_log;
```

![image output](image/output33.PNG)

Delete any id from employee.regions

```markdown
DELETE FROM employee.regions WHERE region_id=10;
```

![image output](image/output34.PNG)

![image output](image/output35.PNG)

### SQL Server INSTEAD OF Trigger

INSTEAD OF trigger skips a DML statement and execute other statements.

Syntax:

```markdown
CREATE TRIGGER [schema_name.] trigger_name
ON {table_name | view_name }
INSTEAD OF {[INSERT] [,] [UPDATE] [,] [DELETE] }
AS
{sql_statements}
```

Example:

1. **create a new table named employee.employees_approval for storing pending approval employees**

```markdown
CREATE TABLE employee.employees_approval (
employee_id INT IDENTITY(1,1) PRIMARY KEY,
	first_name VARCHAR (20) DEFAULT NULL,
	last_name VARCHAR (25)  NULL,
	email VARCHAR (100)  NULL,
	phone_number VARCHAR (20) DEFAULT NULL,
	hire_date DATE  NULL,
	job_id INT  NULL,
	salary DECIMAL (8, 2)  NULL,
	manager_id INT DEFAULT NULL,
	department_id INT DEFAULT NULL,
);
```

Output:

![image output](image/output36.PNG)

2. **Create view named employee.view_empl**

```markdown
CREATE VIEW employee.view_empl
AS
SELECT 
employee_id,
'Approved' approval_status
FROM employee.employees
UNION 
SELECT 
employee_id,
'Pending Approval' approval_status
FROM 
employee.employees_approval;
```

Output:

![image output](image/output37.PNG)

3. **Create trigger for the above view INSTEAD OF INSERT**

```markdown
CREATE TRIGGER employee.trigger_view_empl
ON employee.view_empl
INSTEAD OF INSERT 
AS
BEGIN
	SET NOCOUNT ON;
	INSERT INTO employee.employees_approval(employee_id)
	SELECT  i.employee_id
	FROM inserted i
	WHERE i.employee_id NOT IN(
	SELECT employee_id FROM employee.employees
	);
END
```

Output:

![image output](image/output38.PNG)

4. **Insert value in view**

```markdown
INSERT INTO employee.view_empl(employee_id) VALUES (256);
```

Output:

![image output](image/output39.PNG)

5. **If you query data from the employee.view_empl table, you will see a new row appear**

```markdown
SELECT employee_id,approval_status FROM employee.view_empl;
```

![image output](image/output40.PNG)

The following statement shows the contents of the production.brand_approvals table

```markdown
SELECT employee_id FROM employee.employees_approval
```

![image output](image/output145.PNG)

### SQL Server DDL Trigger

SQL Server DDL triggers respond to server or database events rather than to table data modifications. These events created by the Transact-SQL statement that normally starts with one of the following keywords CREATE, ALTER, DROP, GRANT, DENY, REVOKE, or UPDATE STATISTICS.

The DDL triggers are useful in the following cases:

* Record changes in the database schema.
* Prevent some specific changes to the database schema.
* Respond to a change in the database schema.

Syntax:

```markdown
CREATE TRIGGER trigger_name
ON { DATABASE |  ALL SERVER}
[WITH ddl_trigger_option]
FOR {event_type | event_group }
AS {sql_statement}
```

Example:

1. **First, create a new table named index_logs to log the index changes**

```markdown
CREATE TABLE employee.index_logs (
    log_id INT IDENTITY PRIMARY KEY,
    event_data XML NOT NULL,
    changed_by SYSNAME NOT NULL
);
GO
```

Output:

![image output](image/output42.PNG)

2. **Create a DDL trigger to track index changes and insert events data into the index_logs table**

```markdown
CREATE TRIGGER trg_index_changes
ON DATABASE
FOR	
    CREATE_INDEX,
    ALTER_INDEX, 
    DROP_INDEX
AS
BEGIN
    SET NOCOUNT ON;

    INSERT INTO employee.index_logs (
        event_data,
        changed_by
    )
    VALUES (
        EVENTDATA(),
        USER
    );
END;
```

Output:

![image output](image/output41.PNG)

3. **Create indexes for the first_name and last_name columns of the employee.employees table**

```markdown
CREATE NONCLUSTERED INDEX nidx_fname
ON employee.employees(first_name);
GO

CREATE NONCLUSTERED INDEX nidx_lname
ON employee.employees(last_name);
GO
```

Output:

![image output](image/output43.PNG)

4. **Query data from the employee.index_changes table to check whether the index creation event was captured by the trigger properly**

```markdown
SELECT * FROM employee.index_logs;
```

Output:

![image output](image/output44.PNG)

### SQL Server DISABLE TRIGGER

Triggers when created in SQL Server are enabled by default. You can disable a trigger temporarily using the DISABLE TRIGGER statement.

Disable trigger does not delete the trigger. The trigger exists in the current database but it doesn't fire

Syntax:

```markdown
DISABLE TRIGGER [schema_name.][trigger_name] 
ON [object_name | DATABASE | ALL SERVER]
```

Example:

```markdown
DISABLE TRIGGER ALL ON employee.regions;
```

Output:

In the below image check on objet explorer you can see region_trigger is disabled indicated by * mark on the trigger

![image output](image/output45.PNG)

### SQL Server ENABLE TRIGGER

Enable trigger reactivates the disabled trigger. Use the ENABLE TRIGGER statement to enable a trigger to fire when an event occurs.

Syntax:

```markdown
ENABLE TRIGGER [schema_name.][trigger_name] 
ON [object_name | DATABASE | ALL SERVER]
```

Example:

```markdown
ENABLE TRIGGER region_trigger ON employee.regions;
```

Output:

In the below image check on objet explorer you can see region_trigger is enabled

![image output](image/output46.PNG)

### Modify Trigger 

The ALTER TRIGGER statement is used to modify the definition of an existing trigger without altering the permissions or dependencies.

Syntax:

```markdown
ALTER TRIGGER trigger_name   
ON { Table name or view name }   
[ WITH  ]  
{ FOR | AFTER | INSTEAD OF }   
{ [INSERT], [UPDATE] , [DELETE] }   
AS
    sql_statements 

```

Example:

ALTER TRIGGER employee.region_trigger
ON employee.regions
AFTER INSERT,DELETE
AS
BEGIN 
     SET NOCOUNT ON;
	 INSERT INTO employee.regions_log(region_id,region_name,updated_at,operation)
	 SELECT i.region_id,i.region_name,GETUTCDATE(),'INS'
	 FROM inserted i
	 UNION ALL 
	 SELECT d.region_id,d.region_name,GETUTCDATE(),'DEL'
	 FROM deleted d;
END

Output:

![image output](image/output47.PNG)

### SQL Server DROP TRIGGER

The SQL Server DROP TRIGGER statement drops one or more triggers from the database

Syntax:

```markdown
DROP TRIGGER [ IF EXISTS ] [schema_name.]trigger_name [ ,...n ];
```

Example:

```markdown
DROP TRIGGER IF EXISTS sales.trg_member_insert;
```

Output:

![image output](image/output48.PNG)

## SQL-Server Control flow Statements

Control statements are SQL statements that allow SQL to be used as a structured programming language. SQL control statements provide the capability to control the logic flow, declare and set variables, and handle warnings.

* [SQL-Server IF ELSE Statement](#sql-server-if-else-statement)
* [SQL-Server WHILE Loop](#sql-server-while-loop)
* [SQL-Server BREAK](#sql-server-break)
* [SQL-Server CONTINUE](#sql-server-continue)

### SQL-Server IF ELSE Statement

The IF...ELSE statement is a control-flow statement that allows you to execute based on a specified condition.

Syntax:

```markdown
IF boolean_expression   
BEGIN
    { statement_block }
END
```

Example:

```markdown
DECLARE @marks INT = 30 ;  
  
IF @marks >= 45  
BEGIN  
   PRINT 'Congratulations! You pass the Examination';  
END  
ELSE 
BEGIN 
     PRINT 'You failed in Examination';
END
```

Output:

![image output](image/output23.PNG)

![image output](image/output24.PNG)

### SQL-Server WHILE Loop

The WHILE statement is a control-flow statement that allows you to execute a statement block repeatedly as long as a specified condition is TRUE.

Syntax:

```markdown
WHILE Boolean_expression   
BEGIN
     { sql_statement | statement_block}  
END
```

Example:

```markdown
DECLARE @count INT = 10;

WHILE @count <= 13
BEGIN
    PRINT @count;
    SET @count = @count + 1;
END;
PRINT 'Query Executed';
```

Output:

![image output](image/output25.PNG)

### SQL-Server BREAK

We use WHILE statement to create a loop,To exit the current iteration of a loop use the BREAK statement.

Syntax:

```markdown
WHILE Boolean_expression
BEGIN
    -- statements
   IF condition
        BREAK;
    -- other statements    
END
```

Example:

```markdown
DECLARE @count INT = 10;

WHILE @count <= 20
BEGIN
	SET @count = @count + 1;
	IF (@count =15)
	BREAK;
    PRINT @count;
END;
PRINT 'Query Executed';
```

Output:

![image output](image/output26.PNG)

### SQL-Server CONTINUE

The CONTINUE statement stops the current iteration of the loop and starts the new one. 

Syntax:

```markdown
WHILE Boolean_expression
BEGIN
    -- code to be executed
    IF condition
        CONTINUE;
    -- code will be skipped if the condition is met
END
```

Example:

```markdown
DECLARE @count INT = 10;

WHILE @count < 15
BEGIN
	SET @count = @count + 1;
	IF (@count =13)
	CONTINUE;
    PRINT @count;
END;
PRINT 'Query Executed';
```

Output: 

![image output](image/output27.PNG)

## SQL SERVER FUNCTIONS

Functions in SQL Server are the database objects that contains a set of SQL statements to perform a specific task. A function accepts input parameters, perform actions, and then return the result.

Different types of sql server functions are as follows

* [**Aggregate functions**](#aggregate-functions)
* [**String Functions**](#string-functions)
* [**Date Functions**](#date-functions)
* [**Windows Function**](#windows-function)
* [**System Functions**](#system-function)


### **Aggregate functions**

SQL-Server aggregate functions retrieve a single value after performing a calculation on a set of values.

<br>

SQL Server provides various aggregate functions, and the most commonly used aggregate functions are shown in the below table:

| **_Aggregate Function_** | **_Descriptions_**                                                                                   |
|--------------------------|------------------------------------------------------------------------------------------------------|
| [COUNT()](#count)        | This function counts the number of elements or rows, including NULL values in the defined set.       |
| [SUM()](#sum)            | This function calculates the total sum of all NON-NULL values in the given set.                      |
| [AVG()](#avg)            | This function performs a calculation on NON-NULL values to get the average of them in a defined set. |
| [MIN()](#min)            | This function returns the minimum (lowest) value in a set.                                           |
| [MAX()](#max)            | This function returns the maximum (highest) value in a set.                                          |

#### **COUNT**

SQL Server COUNT() is an aggregate function that returns the number of items found in a set.

Example:

```markdown
SELECT COUNT (*) AS total_employee FROM employee.employees;
```

Output:

![image output](image/output105.PNG)

#### **SUM**

The SUM() function calculates the sum of a set of values.

Example:

```markdown
SELECT SUM(salary) AS total_salary FROM employee.employees;
```

Output:

![image output](image/output106.PNG)

#### **AVG**

The AVG() function returns the average value of an expression.

Example:

```markdown
SELECT AVG(salary) AS avg_salary FROM employee.employees;
```

Output:

![image output](image/output107.PNG)

#### **MAX**

The MAX() function returns the maximum value in a set of values.

Example:

```markdown
SELECT MAX(salary) AS max_salary FROM employee.employees;
```

Output:

![image output](image/output108.PNG)

#### **MIN**

The MIN() function returns the minimum value in a set of values.

Example:

```markdown
SELECT MIN(salary) AS min_salary FROM employee.employees;
```

Output:

![image output](image/output109.PNG)

### **String Functions**

SQL string functions are used primarily for string manipulation.

The following table listed each of the functions with a brief description:

| **_Function Name_**      | **_Descriptions_**                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ASCII](#ascii)          | This function displays the ASCII value of a character.                                                                                                     |
| [CHAR](#)                | This function converts the specified integer code (ASCII) into a single-byte character.                                                                    |
| [CHARINDEX](#charindex)  | This function returns the first expression's starting position if a character expression is found inside a second character expression.                    |
| [CONCAT](#concat)        | This function returns a single string by joining two or more strings.                                                                                      |
| [CONCAT_WS](#)           | This function concatenates multiple strings into a single and spate them with a separator specified in the first position.                                 |
| [DIFFERENCE](#difference)| This function returns an integer value by comparing the two strings SOUNDEX() values.                                                                      |
| [FORMAT](#)              | This function is used to change the text format of the string into any other format.                                                                       |
| [LEFT](#left)            | This function returns the substring from the left of the string to a specified number of characters.                                                       |
| [LEN](#)                 | This function returns the number of characters in a string, including trailing spaces.                                                                     |
| [LOWER](#lower)          | This function is used to convert the upper case character into lower case.                                                                                 |
| [LTRIM](#ltrim)          | This function returns a string from a given string after removing all leading spaces.                                                                      |
| [NCHAR](#)               | This function is used to get the Unicode character with the provided integer code based on the UNICODE standard.                                           |
| [PATINDEX](#)            | This function returns the first occurrence of a pattern in a string's starting place. If the string is not found, it returns zero.                         |
| [QUOTENAME](#quotename)  | This function returns a Unicode string including the delimiters, converting the input string into a valid delimited identifier.                            |
| [REPLACE](#)             | This function is used to replace all occurrences of the substring in a specified string with another string value.                                         |
| [REPLICATE](#replicate)  | This function repeats the string with the specified number of times.                                                                                       |
| [REVERSE](#)             | This function displays the character string in reverse order.                                                                                              |
| [RIGHT](#right)          | This function returns the substring from the right of the string to a specified number of characters.                                                      |
| [RTRIM](#rtrim)          | This function returns a string from a given string after removing all trailing spaces.                                                                     |
| [SOUNDEX](#soundex)      | It is used to calculate the similarity of two strings using a four-character (SOUNDEX) code.                                                               |
| [SPACE](#)               | This function is used to finds the string of repeated spaces.                                                                                              |
| [STR](#)                 | This function is used to return the character data converted from numeric data.                                                                            |
| [STRING_AGG](#)          | This function concatenates the values of string expressions and inserts separator values in between. It does not add a separator at the end of the string. |
| [STRING_ESCAPE](#)       | This function escapes special characters in a string and produces a new string containing the characters that were escaped.                                |
| [STRING_SPLIT](#)        | It is a table-valued function that divides a string into rows of substrings using a separator of your choice.                                              |
| [STUFF](#)               | This function removes a portion of a string and replaces it with another substring beginning at a specified position.                                      |
| [SUBSTRING](#)           | This function extracts a substring from a string that begins at a specific position and ends at a specific length.                                         |
| [TRANSLATE](#)           | This function combines several one-to-one translations into a single operation.                                                                            |
| [TRIM](#)                | This function returns a new string after removing all leading and trailing blanks from a given string.                                                     |
| [UNICODE](#)             | This function returns a character's integer value as defined by the Unicode standard.                                                                      |
| [UPPER](#)               | This function converts the lower case character into the upper case.                                                                                       |

#### **ASCII**

The ASCII() function returns the ASCII value for the specific character.

Example:

```markdown
SELECT ASCII('A') FROM employee.employees;
SELECT first_name,ASCII(first_name) FROM employee.employees;
```

Output:

![image output](image/output110.PNG)

#### **CHARINDEX**

The CHARINDEX() function searches for a substring in a string, and returns the position.

Syntax:

```markdown
CHARINDEX(substring, string, start)
```

Example:

```markdown
SELECT CHARINDEX('l', 'Employee') AS Position;
```

Output:

![image output](image/output111.PNG)

#### **CONCAT**

The CONCAT() function adds two or more strings together.

Example:

```markdown
SELECT CONCAT('employee','name');
```

Output:

![image output](image/output112.PNG)

#### **SOUNDEX**

The SOUNDEX() function returns a four-character code to evaluate the similarity of two expressions.

Example:

```markdown
SELECT SOUNDEX('employee'), SOUNDEX('location');
```

Output:

![image output](image/output113.PNG)

#### **DIFFERENCE**

The DIFFERENCE() function compares two SOUNDEX values, and returns an integer. The integer value indicates the match for the two SOUNDEX values, from 0 to 4.

0 indicates weak or no similarity between the SOUNDEX values. 4 indicates strong similarity or identically SOUNDEX values.

Example:

```markdown
SELECT DIFFERENCE('employee','student');
SELECT DIFFERENCE('Juice','Jucy');
```

Output:

![image output](image/output114.PNG)

#### **LEFT**

The LEFT() function extracts a number of characters from a string (starting from left).

Example:

```markdown
SELECT LEFT (first_name, 2) AS ExtractString FROM employee.employees;
```

Output:

![image output](image/output115.PNG)

#### **RIGHT**

The RIGHT() function extracts a number of characters from a string (starting from right).

Example:

```markdown
SELECT RIGHT (first_name, 2) AS ExtractString FROM employee.employees;
```

Output:

![image output](image/output116.PNG)

#### **LOWER**

The LOWER() function converts a string to lower-case.

Example:

```markdown
SELECT LOWER('EMPLOYEE') AS lowercase;
```

Output:

![image output](image/output117.PNG)

#### **UPPER**

The UPPER() function converts a string to upper-case.

Example:

```markdown
SELECT UPPER('employee') AS uppercase;
```

Output:

![image output](image/output118.PNG)

#### **LTRIM**

The LTRIM() function removes leading spaces from a string.

Example:

```markdown
SELECT LTRIM('       Employee') AS lefttrim;
```

Output:

![image output](image/output119.PNG)

#### **RTRIM**

The RTRIM() function removes trailing spaces from a string.

Example:

```markdown
SELECT RTRIM('Employee     ')AS righttrim;
```

Output:

![image output](image/output120.PNG)

#### **QUOTENAME**

The QUOTENAME() function returns a Unicode string with delimiters added to make the string a valid SQL Server delimited identifier.

Example:

```markdown
SELECT QUOTENAME('Employee','()');
```

Output:

![image output](image/output121.PNG)

#### **REPLICATE**

The REPLICATE() function repeats a string a specified number of times.

Example:

```markdown
SELECT REPLICATE (first_name, 3) AS Replicate_name FROM employee.employees;
```

Output:

![image output](image/output122.PNG)

### **Date Functions**

**Returning the current date and time**

| **_Function_**                          | **_Descriptions_**                                                                                                                            |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [CURRENT_TIMESTAMP](#current-timestamp) | This function is used to get the current date and time values without including the time zone offset.                                         |
| [GETUTCDATE](#getutcdate)               | This function is used to get the current UTC date and time values as an integer.                                                              |
| [GETDATE](#getdate)                     | This function is used to get the system's current date and time on which the SQL Server is installed.                                         |
| [SYSDATETIME](#sysdatetime)             | This function is used to get the system's current date and time with more fractional second precision without including the time zone offset. |
| [SYSUTCDATETIME](#sysutcdatetime)       | This function is used to get the system's current date and time value based on the UTC timestamp as an integer.                               |
| [SYSDATETIMEOFFSET](#sysdatetimeoffset) | This function is used to get the system's current date and time with the time zone offset.                                                    |

**Returning the date and time Parts**

| **_Function_**              | **_Descriptions_**                                                                               |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| [DATENAME](#datename)       | This function is used to get a portion of the date in day, month, or year as a character string. |
| [DATEPART](#datepart)       | This function is used to get the portion of the date as an integer number.                       |
| [DAY](#day)                 | This function is used to get the day value from the input dates as an integer.                   |
| [MONTH](#month)             | This function is used to get the month value from the input dates as an integer.                 |
| [YEAR](#year)               | This function is used to get the year value from the input dates as an integer.                  |

**Returning a difference between two dates**

| **_Function_**              | **_Descriptions_**                                                                   |
|-----------------------------|--------------------------------------------------------------------------------------|
| [DATEDIFF](#datediff)       | This function is to get the difference in a date part of the two input dates values. |

**Modifying dates**

| **_Function_**                       | **_Descriptions_**                                                                                              |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [DATEADD](#dateadd)                  | This function is used to add an integer value to a date part of the input dates and returns the new date value. |
| [EOMONTH](#eomonth)                  | This function is used to get the last day of the month with the specified date and an optional offset.          |
| [SWITCHOFFSET](#switchoffset)        | This function is used to modify the timezone offset of a datetime offset value and preserves the UTC value.     |
| [TODATETIMEOFFSET](#todatetimeoffset)| This function is used to change the DATETIME2 value into a DATETIMEOFFSET value.                                |

**Constructing date and time from their parts**

| **_Function_**                                      | **_Descriptions_**                                                                    |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [DATEFROMPARTS](#datefromparts)                     | This function is used to get a date value from the specified day, month, or year.     |
| [DATETIME2FROMPARTS](#datetime2fromparts)           | This function is used to get a DATETIME2 value from the date and time arguments.      |
| [DATETIMEOFFSETFROMPARTS](#datetimeoffsetfromparts) | This function is used to get a DATETIMEOFFSET value from the date and time arguments. |
| [TIMEFROMPARTS](#timefromparts)                     | This function is used to get a time value from the time parts with precision.         |

**Validating date and time values**

| **_Function_**            | **_Descriptions_**                                                                                                    |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [ISDATE](#isdate)         | This function is used to check the entered dates follows the standard format of date, time, or datetime value or not. |

#### **CURRENT-TIMESTAMP()**

The CURRENT_TIMESTAMP function returns the current date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT CURRENT_TIMESTAMP AS currentDateAndTime;
```

Output:

![image output](image/output123.PNG)

#### **GETDATE()**

The GETDATE() function returns the current database system date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT GETDATE() AS currentDate;
```

Output:

![image output](image/output124.PNG)

#### **GETUTCDATE()**

The GETUTCDATE() function returns the current database system UTC date and time, in a 'YYYY-MM-DD hh:mm:ss.mmm' format.

Example:

```markdown
SELECT GETUTCDATE();
```

Output:

![image output](image/output125.PNG)

#### **SYSDATETIME**

The SYSDATETIME() function returns the date and time of the computer where the SQL Server is running.

Example:

```markdown
SELECT SYSDATETIME();
```

Output:

![image output](image/output126.PNG)

#### **SYSUTCDATETIME**

The SYSUTCDATETIME() function returns the system's current date and time based on the UTC timestamp as an integer.

Example:

```markdown
SELECT SYSUTCDATETIME() AS Date;  
```

Output:

![image output](image/output127.PNG)

#### **SYSDATETIMEOFFSET()**

The SYSDATETIMEOFFSET() function returns the system's current date and time with the timezone offset.

Example:

```markdown
SELECT SYSDATETIMEOFFSET() AS Date;  
```

Output:

![image output](image/output128.PNG)

#### **DATENAME()**

This function is used to get a portion of the date in day, month, or year as a character string.

Example:

```markdown
SELECT DATENAME(yy, '2017/08/25') AS DatePartString;
SELECT DATENAME(month, '2017/08/25') AS DatePartString;
```

Output:

![image output](image/output129.PNG)

#### **DATEPART()**

This function is used to get the portion of the date as an integer number.

Example:

```markdown
SELECT DATEPART(yy, '2017/08/25') AS DatePartString;
SELECT DATEPART(month, '2017/08/25') AS DatePartString;
```

Output:

![image output](image/output130.PNG)

#### **YEAR()**

This function is used to get the year value from the input dates as an integer.

Example:

```markdown
SELECT YEAR(hire_date) AS year FROM employee.employees;
```

Output:

![image output](image/output131.PNG)

#### **MONTH()**

This function is used to get the month value from the input dates as an integer.

Example:

```markdown
SELECT MONTH(hire_date) AS month FROM employee.employees;
```

Output:

![image output](image/output132.PNG)

#### **DAY()**

This function is used to get the day value from the input dates as an integer.  

Example:

```markdown
SELECT DAY(hire_date) AS day FROM employee.employees;
```

Output:

![image output](image/output133.PNG)

#### **DATEDIFF**

This function is to get the difference in a date part of the two input dates values.

Example:

```markdown
SELECT DATEDIFF(hour, '2017/08/25 07:00', '2017/08/30 12:45') AS HourDiff;
SELECT DATEDIFF(month, '2011/08/25', '2017/08/25') AS MonthDiff;
SELECT DATEDIFF(day, '2011/08/25', '2011/08/30') AS DayDiff;
```

Output:

![image output](image/output134.PNG)

#### **DATEADD()**

This function is used to add an integer value to a date part of the input dates and returns the new date value.

Example:

```markdown
SELECT DATEADD(year, 11, hire_date) AS YearAdd FROM employee.employees;
```

Output:

![image output](image/output135.PNG)

#### **EOMONTH**

This function is used to get the last day of the month with the specified date and an optional offset.   

Example:

```markdown
SELECT EOMONTH(hire_date) AS EndDateoftheMonth FROM employee.employees;
```

Output:

![image output](image/output136.PNG)

#### **SWITCHOFFSET**

This function is used to modify the timezone offset of a datetime offset value and preserves the UTC value.

Example:

```markdown
SELECT SWITCHOFFSET(hire_date,'-05:00') AS result FROM employee.employees;
```

Output:

![image output](image/output137.PNG)

#### **TODATETIMEOFFSET**

This function is used to change the DATETIME2 value into a DATETIMEOFFSET value. 

Example:

```markdown
SELECT TODATETIMEOFFSET(GETDATE(),'-05:00') AS result,TODATETIMEOFFSET(GETDATE(),180);
```

Output:

![image output](image/output138.PNG)

#### **DATEFROMPARTS**

This function is used to get a date value from the specified day, month, or year.

Example:

```markdown
SELECT DATEFROMPARTS(2023, 04, 04) AS Result1, DATEFROMPARTS(2023, NULL, 04) AS Result2;  
```

Output:

![image output](image/output139.PNG)

#### **DATETIME2FROMPARTS**

This function is used to get a DATETIME2 value from the date and time arguments.

Example:

```markdown
SELECT DATETIME2FROMPARTS ( 2023, 10, 31, 11, 59, 59, 0, 0 ) AS Result1,  DATETIME2FROMPARTS(2023, NULL, 31, 11, 59, 59, 0, 0) AS Result2;    
```

Output:

![image output](image/output140.PNG)

#### **DATETIMEOFFSETFROMPARTS**

This function is used to get a DATETIMEOFFSET value from the date and time arguments.

Example:

```markdown
SELECT DATETIMEOFFSETFROMPARTS(2023, 10, 11, 20, 35, 30, 4000, 10, 30, 4) AS Result1,  
DATETIMEOFFSETFROMPARTS(NULL, 10, 11, 20, 35, 30, 4000, 10, 30, 4) AS Result2;  
```

Output:

![image output](image/output141.PNG)

#### **TIMEFROMPARTS**

This function is used to get a time value from the time parts with precision.

Example:

```markdown
SELECT TIMEFROMPARTS(20, 55, 59, 55, 3) AS Result1,  TIMEFROMPARTS(10, NULL, 19, 5, 2) AS Result2;  
```

Output:

![image output](image/output142.PNG)

#### **ISDATE**

This function is used to check the entered dates follows the standard format of date, time, or datetime value or not.

Example:

```markdown
SELECT ISDATE('2020-25-01') AS Result1, ISDATE('2020-12-06') AS Result2;
```
Output:

![image output](image/output143.PNG)

### **Windows Function**

Window functions operate on a set of rows and return a single aggregated value for each row. The term Window describes the set of rows in the database on which the function will operate.

<br>

| **_Name_**                    | **_Description_**                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------|
| [DENSE_RANK](#dense-rank)     | Assign a rank value to each row within a partition of a result, with no gaps in rank values.                |
| [FIRST_VALUE](#first-value)   | Get the value of the first row in an ordered partition of a result set.                                     |
| [LAG](#lag)                   | Provide access to a row at a given physical offset that comes before the current row.                       |
| [LAST_VALUE](#last-value)     | Get the value of the last row in an ordered partition of a result set.                                      |
| [LEAD](#lead)                 | Provide access to a row at a given physical offset that follows the current row.                            |
| [NTILE](#ntile)               | Distribute rows of an ordered partition into a number of groups or buckets                                  |
| [PERCENT_RANK](#percent-rank) | Calculate the percent rank of a value in a set of values.                                                   |
| [RANK](#rank)                 | Assign a rank value to each row within a partition of a result set                                          |
| [ROW_NUMBER](#row-number)     | Assign a unique sequential integer to rows within a partition of a result set, the first row starts from 1. |


#### **DENSE-RANK**

Assign a rank value to each row within a partition of a result, with no gaps in rank values.

Example:

```markdown
SELECT first_name,last_name,
       DENSE_RANK() OVER (ORDER BY salary) AS Rank_No 
	   FROM employee.employees;
```

Output:

![image output](image/output144.PNG)

#### **FIRST-VALUE**

Get the value of the first row in an ordered partition of a result set.  

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
FIRST_VALUE(first_name) OVER (PARTITION BY job_id ORDER BY salary) AS FirstValue
FROM employee.employees
```

Output:

![image output](image/output49.PNG)

#### **LAG**

Lag function is used to access previous row data along with current row data

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
        LAG(Salary, 1, -1) OVER (ORDER BY Salary) AS Lag_1
FROM employee.employees
```

Output:

![image output](image/output50.PNG)

#### **LAST-VALUE**

The LAST_VALUE() function is a window function that returns the last value in an ordered partition of a result set.

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name, salary,
LAST_VALUE(first_name) OVER (ORDER BY salary ROWS BETWEEN UNBOUNDED PRECEDING AND UNBOUNDED FOLLOWING) AS LastValue
FROM employee.employees
```

Output:

![image output](image/output51.PNG)

#### **LEAD**

Lead function is used to access subsequent row data along with current row data

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
          LEAD(Salary, 2, -1) OVER (ORDER BY Salary) AS Lead
FROM employee.employees
```

Output:

![image output](image/output52.PNG)

#### **NTILE**

The SQL Server NTILE() is a window function that distributes rows of an ordered partition into a specified number of approximately equal groups, or buckets. It assigns each group a bucket number starting from one. For each row in a group, the NTILE() function assigns a bucket number representing the group to which the row belongs.

Syntax:

```markdown
NTILE (Number_of_Groups) OVER (ORDER BY Col1, Col2, ...)
```

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
          NTILE(5) OVER (ORDER BY salary) AS [Ntile]
FROM employee.employees
```

Output:

![image output](image/output53.PNG)

#### **PERCENT-RANK**

The PERCENT_RANK() function evaluates the relative standing of a value within a partition of a result set.

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
         PERCENT_RANK() OVER (ORDER BY salary) AS percent_rank
FROM employee.employees
```

Output:

![image output](image/output54.PNG)

#### **RANK**

The RANK() function is a window function that assigns a rank to each row within a partition of a result set.

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
         RANK() OVER (ORDER BY salary) AS rank
FROM employee.employees
```

Output:

![image output](image/output55.PNG)

#### **ROW-NUMBER**

Assign a unique sequential integer to rows within a partition of a result set, the first row starts from 1.

Example:

```markdown
SELECT employee_id, first_name+' '+last_name AS full_name,job_id, salary,
         ROW_NUMBER() OVER (PARTITION BY job_id ORDER BY job_id) AS rownumber
FROM employee.employees
```

Output:

![image output](image/output56.PNG)

### **System Function**

| **_Name_**                          | **_Description_**                                                                                                                        |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [CAST](#cast)                       | cast a value of one type to another.                                                                                                     |
| [CONVERT](#convert)                 | convert a value of one type to another.                                                                                                  |
| [CHOOSE](#choose)                   | return one of the two values based on the result of the first argument.                                                                  |
| [ISNULL](#isnull)                   | replace NULL with a specified value.                                                                                                     |
| [ISNUMERIC](#isnumeric)             | check if an expression is a valid numeric type.                                                                                          |
| [IIF](#iif)                         | add if-else logic to a query.                                                                                                            |
| [TRY_CAST](#try-cast)               | cast a value of one type to another and return NULL if the cast fails.                                                                   |
| [TRY_CONVERT](#try-convert)         | convert a value of one type to another and return the value to be translated into the specified type. It returns NULL if the cast fails. |
| [TRY_PARSE](#try-parse)             | convert a string to a date/time or a number and return NULL if the conversion fails.                                                     |

#### **CAST**

cast a value of one type to another. 

Example:

```markdown
SELECT 
    CAST('2019-03-14' AS DATETIME) result;
```

Output:

![image output](image/output57.PNG)

#### **CONVERT**

convert a value of one type to another.

Example:

```markdown
SELECT 
    CONVERT(DATETIME, '2019-03-14') result;
```

Output:

![image output](image/output58.PNG)

#### **CHOOSE**

return one of the two values based on the result of the first argument. 

Example:

```markdown
SELECT 
    CHOOSE(1, 'First', 'Second', 'Third') Result;
```

Output:

![image output](image/output59.PNG)

#### **ISNULL**

replace NULL with a specified value.

Example:

```markdown
SELECT 
    ISNULL(NULL,20) result;
```

Output:

![image output](image/output60.PNG)

#### **ISNUMERIC**

check if an expression is a valid numeric type.

Example:

```markdown
SELECT 
    ISNUMERIC('$10') result;
```

Output:

![image output](image/output61.PNG)

#### **IIF**

add if-else logic to a query.

Example:

```markdown
SELECT 
    IIF(10 < 20, 'True', 'False') Result ;
```

Output:

![image output](image/output62.PNG)

#### **TRY-CAST**

cast a value of one type to another and return NULL if the cast fails.

Example:

```markdown
SELECT 
    TRY_CAST('100.5' AS INT) Result;
```

Output:

![image output](image/output63.PNG)

#### **TRY-CONVERT**

convert a value of one type to another and return the value to be translated into the specified type. It returns NULL if the cast fails.

Example:

```markdown
SELECT 
    TRY_CONVERT( INT, '100.5') Result;
```

Output:

![image output](image/output64.PNG)

#### **TRY-PARSE**

convert a string to a date/time or a number and return NULL if the conversion fails.

Example:

```markdown
SELECT 
    CASE
        WHEN TRY_PARSE('12-08-2022' AS DATE) IS NULL
        THEN 'Cast failed'
        ELSE 'Cast succeeded'
    END AS result;
```

Output:

![image output](image/output65.PNG)

## REFERENCE

FOR INSTALLATION 

* SQL-server https://learn.microsoft.com/en-us/sql/database-engine/install-windows/install-sql-server?view=sql-server-ver16
* Docker SQL-Server https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver16&pivots=cs1-cmd


