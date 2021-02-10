#### SQL ####
=============

**SQL** (Structured Query Language) is used to perform operations on the records 
stored in the database.  SQL is just a query language and not a database.  Oracle,
MySQL, MongoDB, PostGreSQL are some of the examples for Database.

##Why SQL?##

    * To create new databases, tables and views
    * To insert records in a database
    * To update records in a database
    * To delete records from a database
    * To retrieve data from a database

##SQL Commands##

SQL Commands are categorized into four categories as:

    1. DDL - Data Definition Language
    2. DQL - Data Query Language
    3. DML - Data Manipulation Language
    4. DCL - Data Control Language
    5. TCL - Transaction Control Language

##DDL##
-------

Data Definition Language actually consists of the SQL commands that can be used to
define the database schema.  DDL Commands:  Create, Drop, Alter, Truncate, Rename.

```sql

//query to create table
create table table_name(
    id int primary key,
    name varchar[25]
);

//query to delete table
drop table table_name;

```

##DQL##
-------

The purpose of DQL Command is to get some schema relation based on the query passed
to it.  DQL Command: Select.

```sql

//query to display all data in the table
Select * from table name;

```

##DML##

Data Manipulation Language deals with the manipulationof data present in the database
DML Commands:  Insert, Update, Delete.

```sql

//query to insert values into table
insert into table_name(id,name) values(101,'Mukesh');

//query to update values into table
update table table_name set name='Mukesh Kumar' where id=101;

```

##DCL##

Data Control Language deals with the commands that deals with the rights, permissions
and other controls of the database system.  DCL Commands: Grant, Revoke.

```sql

//query to grant and revoke create table permission to testing role
Grant create table to Testing
Revoke create table from Testing

```

##TCL##

TCL commands deals with the transaction within the database. TCL Commands: Commit,
Rollback, Savepoint.

```sql

\\query to save currentpoint of transaction and rollback to previous point
Savepoint sp1;
//some operations
rollback sp1;

```

##JOIN##

A join clause is used to combine two or more table, based on the given condition.
There are different types of joins in SQL.  They are Inner Join, Left Outer Join, 
Right Outer Join and Full Outer Join.

   * Inner Join returns only the matching rows of both the tables.
   * Left Outer Join returns the matching rows of both the tables and all the rows in
the left table.
   * Right Outer Join returns the matching rows of both the tables and all the rows
in the right table.
   * Full Join returns all rows in both the tables. 

```sql

//query to left join two tables
Select * from table_one LEFT JOIN table_two on table_one.id=table_two.id;

```