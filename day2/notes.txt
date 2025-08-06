the length atrribiute of js is used to count the total no. of char in textbox

## DataBase
Data base is a collection of interrelated data which are stored in the form of a file.

## DBMS
Data base magangement system.It is a softfare using which we can manage a data stored in a database.

ex- `Oracle` `MySQL`

## RDBMS

Relational database management system . Here all the data are access thorugh tables . Tables are also termed as relation.Makes data fetching faster than dbms where searching was very slower for larger datas.

- Rows- tuples
- Columns - fields,keys

### - Primary key

It is a column which contains data which are **unique**.
Here we cannot have any **null** value

### - Unique
It can contain **null** values rest same as primary key

### - Foreign Key
If a primary key column of one table is present in another table thern in the second table it is counted as foriegn key.

- It is the foreign key and primary key which are used to relate two tables.


## JDBC[Java Database connectivity]

### Steps for JDBC connectivity

1. Create a table with blank fields.

2. Add appropriate driver for connecting with database.

3. Write appropriate SQL query in order to manipulate the data stored in the database.

## Steps for creating a table

Open Console

java.io contains DatainputStream
java.sql class is responsible for 

type 1---3
typ4 driver created using java

ojdbc
oracle.jdbc.driver.OracleDriver

oracle-jdbc-driver-oracledriver
for connection we need a interface----
connection class con= Drivermanager.getConnection

DriverMangaer is a class which is responsible for connecting with the dbms 
1521 is default port number for oracle
