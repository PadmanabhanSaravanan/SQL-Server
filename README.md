# SQL-Server

![image sql-server-logo](/image/sql-server_logo.png)<!--style="width:30%;" -->

## Introduction to SQLServer

* ## What is Database ?
* ## What is SQL Server ?
* ## Difference between MySql and MS Sql Server
* ## Installation of SQL Server
* ## SQL Server Sample Database

### What is Database ?

A database is an organized collection of data so that it can be easily accessed. To manage these databases, **Database Management Systems (DBMS)** are used.



**Database Management System**<!-- style="font-size:20px;" -->

Database management System is software which is used to store and retrieve the database.

**Types of DBMS**<!-- style="font-size:20px;" -->

In general, there are two common types of databases:

* Non-Relational

* Relational

**Non-Relational Database Management System (Non-RDBMS)**<!-- style="font-size:20px;" -->

In Non-RDBMS, data is stored in key-value pairs. For example:

![image Non-RDBMS](/image/Nosql.png)<!--style="width:50%;" -->

Here, customers' data are stored in key-value pairs.

Commonly used Non-RDBMS: MongoDB, Amazon DynamoDB, Redis, etc.

**Relational Database Management System**<!-- style="font-size:20px;" -->

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

**SQL Server Architecture** <!-- style="font-size:20px;" -->

![image sql-arch](/image/sql-arch.jpg)

SQL Server consists of two main components:

* Database Engine
* SQLOS

**Database Engine**<!-- style="font-size:20px;" -->

![image database engine](/image/database-engine.jpg)<!--style="width:50%;" -->

The core component of the SQL Server is the Database Engine. 

The Database Engine consists of a relational engine that processes queries and a storage engine that manages database files, pages, indexes, etc. The database objects such as stored procedures, views, and triggers are also created and executed by the Database Engine.

**SQLOS**<!-- style="font-size:20px;" -->(SQL Server Operating System)

SQLOS provides many operating system services such as memory and I/O management. Other services include exception handling and synchronization services.

### Difference between MySql and MS Sql Server

**MySQL** is an open source Relational Database Management System (RDBMS) based on Structured Query Language (SQL). It runs on platforms like Linux, UNIX and Windows.

**SQL Server** is owned and developed by Microsoft Corporation. The primary function of SQL Server is the storage and access of data as it is required by other applications, whether they are running on other computers that are connected to a network, or the computer on which the server is stored.

|                                          MS SQL Server                                          |                                                 MySQL                                                 |
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

For complete installation guide [click here](https://www.sqlservertutorial.net/install-sql-server/)




