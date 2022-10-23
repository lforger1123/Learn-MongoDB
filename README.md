# Introduction to Databases

In software engineering *databases* are systems that store, access and modify collections fo information. The most common types of databases are: <br>
- Relational
- Non-relational

## Database Management Systems (DBMS)
We store all of our data in a databsem but to itneract with hat databse we need some sort of software that can help us work with it. That software is called DAtabse Management System, that gives us the option to either programmatically or by GUI interact.

In other words if Database is a bucket that soters all our data then DBMS is an encapsulation of that Database. Each DB has its own DBMS that works differently than the rest. Usually DB and DBMS are used interchangeably and for good reason too. Since one DBMS corresponds to a certain DB only.

Each DBMS allows DB to store different kinds of data, varying from numbers, strings to audio, video file ( though they are stored in binary ). It is because of this ability to store a huge array of data DBMSs have a plethora of use cases.


## Relational Database
One of the most common ones are the RElatinoal Databases or commonly known as SQL Databases. They structure data in a tabular form. Meaning that they store data using rows and columns in a table.

- THey are unique as they are based on presenting the data int erms of relationships. To accomplish this they sue associations like, one-to-one, one-to-many, many-to-many.

- Another notable feature of SQL DBs is that they require something called schema, ie, the blueprint of our DB structure, This means that we have to first define the structure and estabilish the relationships before even inserting our data.

- Relational DBs are managed by RDBMS, In these DBs we manage the data using SQL. Notable RDBMS are: PostgreSQL and MySQL.

- The unique disadvantage of SQL DBMS is, 
    - at enterprise level, the datasets are massive hence setting up Relational DB are costly.
    - Maintenance and Scaling of these DBs prove to be expensive over time.
    - Since they use rows and columns, they consume a great deal of physical space which leads to slower performance and higher cost.


## Non-Relational Database
Another most popular DB is the Non-Relational Database, commonly known as NoSQL DB. Any DB that does not follow the relational model fall udner the NoSQL. These types of databases have their own framework for organizing data. We use these for storing unstructured data that doesn't nearly fit into rows and columns

- The unstructured nature of NoSQL DBs allow the design of flexible schemas ie, the ones that don't need to be created beforehand. This allows  DB to be adaptable to changing needs of an application.

- They are well suited for scalability and are relatively inexpensive maintenance as comapred to SQL DBs.

- Unlike RDBs most NoSQL DBs use their custom quey language isntead of a standard query language (SQL).

- The unique disadvantage of NoSQL DBMS is,
    - Since they are unstructrued, data us harder to maintain and keep a track of.
    - Additionally since all NoSQL DBs use custom queries, they all require a learning curve.


## Why NoSQL?
Over the time as datasets become larger and more and more complex, develoeprs began looking for more flexible and scalable DB solutions.
