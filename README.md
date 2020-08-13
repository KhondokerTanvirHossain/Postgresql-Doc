# ![alt text](https://www.aalpha.net/wp-content/uploads/2019/05/postgre-database-development-india.png)
Welcome to the [Postgresql](https://www.postgresql.org/) documentation! This documentation helps you understand PostgreSQL quickly.

[1 Getting Started](#getting-started)<br />
&nbsp;&nbsp;[1.1 How to Install](#how-to-install)<br>
&nbsp;&nbsp;[1.2 DROP TABLE author](#access-postgres-prompt)<br>
&nbsp;&nbsp;[1.3 Quit Postgres Prompt](#quit-postgres-prompt)<br>
&nbsp;&nbsp;[1.4 Create Database](#create-database) <br>
&nbsp;&nbsp;[1.5 Access a Database with specific user](#access-a-database-with-specific-user)<br>
&nbsp;&nbsp;[1.6 Connect and Access a Database](#connect-and-access-a-database)<br>
[2 Query](#query)<br>
&nbsp;&nbsp;[2.1 Create Table](#create-table)<br>
&nbsp;&nbsp;[2.2 Delete Table](#delete-table)<br>
&nbsp;&nbsp;[2.3 Insert into Table](#insert-into-table)<br>
&nbsp;&nbsp;[2.4 Update Table](#update-table)<br>
&nbsp;&nbsp;[2.5 Delete from Table](#delete-from-table)<br>
&nbsp;&nbsp;[2.6 Read from Table](#read-from-table)<br>
[3 Clause and Condition](#clause-and-condition)<br>
&nbsp;&nbsp;[3.1 WHERE](#where)<br>
&nbsp;&nbsp;[3.1 IN](#in)<br>
&nbsp;&nbsp;[3.1 IS NULL](#is--is-not-null)<br>
&nbsp;&nbsp;[3.1 CASE](#case)<br>



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

### Clause and Condition
##### WHERE
    SELECT select_list
    FROM table_name
    WHERE <condition>;
    WHERE <conditNOT ion>;
##### IN
    SELECT select_list
    FROM table_name
    WHERE value IN (SELECT column_name FROM table_name);

##### IS / IS NOT NULL
    SELECT select_list
    FROM table_name
    WHERE value IS NULL;
    /WHERE value IS NOT NULL;

##### CASE
    CASE 
      WHEN condition_1  THEN result_1
      WHEN condition_2  THEN result_2
      [WHEN ...]
      [ELSE else_result]
    END

### Join
##### INNER JOIN
    SELECT
        column1,
        column2,
        .
        .
        FROM table_A
    INNER JOIN table_B ON pka = fka;

##### OUTER JOIN
    SELECT
        column1,
        column2,
        .
        .
        FROM table_A
    LEFT/RIGHT/FULL OUTER JOIN table_B ON pka = fka;

##### CROSS JOIN
    SELECT
        column1,
        column2,
        .
        .
        FROM table_A
    CROSS JOIN table_B ON pka = fka;



