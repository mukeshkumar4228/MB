SQL 
=============

**SQL** (Structured Query Language) is used to perform operations on the records 
stored in the database.  SQL is just a query language and not a database.  Oracle,
MySQL, MongoDB, PostGreSQL are some of the examples for Database.

Why SQL?
--------

    * To create new databases, tables and views
    * To insert records in a database
    * To update records in a database
    * To delete records from a database
    * To retrieve data from a database

SQL Commands
------------

SQL Commands are categorized into four categories as:

    1. DDL - Data Definition Language
    2. DQL - Data Query Language
    3. DML - Data Manipulation Language
    4. DCL - Data Control Language
    5. TCL - Transaction Control Language

DDL
-------

Data Definition Language actually consists of the SQL commands that can be used to
define the database schema.  DDL Commands:  Create, Drop, Alter, Truncate, Rename.

```sql

create table table_name(
    id int primary key,
    name varchar[25]
);

drop table table_name;

```

DQL
-------

The purpose of DQL Command is to get some schema relation based on the query passed
to it.  DQL Command: Select.

```sql

Select * from table name;

```

DML
-----

Data Manipulation Language deals with the manipulationof data present in the database
DML Commands:  Insert, Update, Delete.

```sql

insert into table_name(id,name) values(101,'Mukesh');

update table table_name set name='Mukesh Kumar' where id=101;

```

DCL
-----

Data Control Language deals with the commands that deals with the rights, permissions
and other controls of the database system.  DCL Commands: Grant, Revoke.

```sql

Grant create table to Testing
Revoke create table from Testing

```

TCL
-----

TCL commands deals with the transaction within the database. TCL Commands: Commit,
Rollback, Savepoint.

```sql

Savepoint sp1;
//some operations
rollback sp1;

```

JOIN
-------

A join clause is used to combine two or more table, based on the given condition.
There are different types of joins in SQL.  They are Inner Join, Left Outer Join, 
Right Outer Join and Full Outer Join.

   * Inner Join returns only the matching rows of both the tables.
   * Left Outer Join returns the matching rows of both the tables and all the rows in
the left table.
   * Right Outer Join returns the matching rows of both the tables and all the rows
in the right table.
   * Full Join returns all rows in both the tables. 

table_one                

| ID |   Name  |         
|----|---------|         
| 01 |  Mukesh |         
| 02 |  Kumar  |         
| 03 |  Raj    |         

table_two

| ID |  Phone Number |
|----|---------------|
| 01 |   9876543210  |
| 02 |   7894561230  |
| 04 |   9632587410  |

```sql

Select * from table_one LEFT JOIN table_two on table_one.id=table_two.id;

```
Output 

| ID |  Name  |  Phone Number |
|----|--------|---------------|
| 01 | Mukesh |  9876543210   |
| 02 | Kumar  |  7894561230   |
| 03 | Raj    |  null         |


AGGREGATE Funtion
------------------

An aggregate function is a function where values in multiple rows are grouped together
based on certain criteria to form a single value.  Avg, Sum, Count, Min, Max are some
of the aggregate functions used in SQL.

| ID | Price |
|----|-------|
| 11 | 200   |
| 12 | 300   |
| 13 | 100   | 

```sql

Select AVG(age) from table_name;

```
**Output**

200
