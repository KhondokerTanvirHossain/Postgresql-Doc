# ![alt text](https://www.aalpha.net/wp-content/uploads/2019/05/postgre-database-development-india.png)
Welcome to the [Postgresql](https://www.postgresql.org/) documentation! This documentation helps you understand PostgreSQL quickly.

[1 Getting Started](#getting-started)<br>
    [1.1 How to Install](#how-to-install)<br>
    [1.2 DROP TABLE author](#access-postgres-prompt)<br>
    [1.3 Quit Postgres Prompt](#quit-postgres-prompt)<br>
    [1.4 Create Database](#create-database) <br>
    [1.5 Access a Database with specific user](#access-a-database-with-specific-user)<br>
    [1.6 Connect and Access a Database](#connect-and-access-a-database)<br>
[2 Query](#query)<br>
    [2.1 Create Table](#create-table)<br>
    [2.2 Delete Table](#delete-table)<br>
    [2.3 Insert into Table](#insert-into-table)<br>
    [2.4 Update Table](#update-table)<br>
    [2.5 Delete from Table](#delete-from-table)<br>
    [2.6 Read from Table](#read-from-table)<br>




### Getting Started
##### How to Install
    $ sudo apt install postgresql postgresql-contrib

##### Access Postgres Prompt
    $ sudo -u postgres psql

##### Quit Postgres Prompt
    postgres=# \q

##### Create Database
    $ postgres createdb <db-name>

##### Access a Database
    $ psql -d <dbname>

##### Access a Database with specific user
    $ psql -d <dbname> -U <username>  -W <password>

##### Connect and Access a Database
    $ psql -h <hostname> -d <dbname> -U <username> -W <password>

### Query
##### Create Table
    CREATE TABLE [IF NOT EXISTS] <table_name> (
        <column1> datatype(length) column_contraint,
        <column2> datatype(length) column_contraint,
            .
            .
        <column3> datatype(length) column_contraint,
        table_constraints
    );

##### Delete Table
    DROP TABLE table_name;

##### Insert into Table
    INSERT INTO table_name(column1, column2, …)
    VALUES (value1, value2, …);

##### Update Table 
    UPDATE table_name
    SET column1 = value1,
        column2 = value2,
        ...
    WHERE <condition>;

##### Delete from Table
    DELETE FROM table_name 
    WHERE <condition>; 

##### Read from Table
    SELECT * FROM table_name
    WHERE <condition>;

    SELECT column1, colum2,.. FROM table_name
    WHERE <condition>;
