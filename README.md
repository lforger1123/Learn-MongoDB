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

## Types of NoSQL Databases
There are 4 most common types of SQL DBs, each with their own characteristic adv and disadv.

- ### Key-Value:
  - This type of DB is the ebst when data is attributed to a unique key.
  - The data here can range from numbers to complex objects.
  - Amazon DynamoDB and Redis are popular in this category.

- ### Document
  - In some document oriented DBs data is stored in hierarchial structures.
  - These documents are very flexible as they can evolve to fit an applications needs.
  - MongoDB is a popular option in this category.

- ### Graph
  - It stores data in nodes like a graph structure and estabilishes relationships via edges.
  - The key adv is they are easy to setup, manage and query
  - Neo4j is a popular option in this category.

- ### Column Oriented
  - It is similar to Relational DB, however, it stores data as columns as opposed to rows.
  - This is done to proved faster read speeds by being able to quickly aggregate data of a specific column.
  - Amazon's Redshift is a popular choice in this category.

----------

# **Introduction to MongoDB**
MongoDB is a DBMS that allows users to store data using the document model. The data stored here is typically in the fashion of JSON, BSON and YAML.

## Advantages of MongoDB
- ### Flexibility and Scalability
  MongoDB is drastically flexible, suppose we want to change the data in a relational model, that change would impact thousands and millions of data entries, something which we don't see with mongoDB as it allows us to interact with each entity separately. So if any changes are to be accomodated our system is flexible enough to handle them. <br>
  Additionally applications may have a tendency to grow and in those cases mongoDB offers multiple easy to use options to accomodate scalability of the application.

- ### Developer Friendly
  Being a modern and popular DBMS, it has a variety of use cases not only in web, mobile or desktop applications but also in data analytics and visualisations. <br>
  Due to this it has a broad community of developers and a plethora of resources to learn and detailed documentation to facilitate the developers at any level.

- ### Diverse Cloud Tooling
  The strongest advantage of using MongoDB is availability of a wide array of cloud tools.
  - **MongoDB Atlas** is a multi-cloud DB service. It allows uses to create, manage and deploy MongoDB DBs with just a ew clicks. The main advantage is that these DBs are hosted in cloud and don't require developers to install MongoDB on their computers but use an online dashboard.
  - **MongoDB Realm** is another cloud offering that promotes fast development of applications that are integrated with mongodb. For instance if we were to build a mobile app then we could use Realm to create a DB on each phone and seamlessly synchronize it across all devices and databases. Also we could use it for authentication.


## Collections and Documents
As we know that MongoDB uses documents within collections to store data. To visualise it, we can think of it as; <br>
At the highest level we our MongoDB instance that contains all the data, then we have collections, ie, subsets of our data. For instance, in case of a camera store, our collections would be purchase data, inventory, customer info. Now each of these collections have their records, ie, data in the form of documents. 2 documents can have entirely different data.

## Why is JSON inefficent?
One of the main advantages of using document DB is the flexibiltiy it provides. In case of MongoDB this flexbility comes partly from JSON. The primary advanage of JSON is its readablity and flexibilty. Data is stored in an easily editable format that is comprehensibe to humans as well as our computers. But that comes at a price;
- JSON is inefficient form a computational perspective as the data is time consuming to parse.
- Due to its readability its not exactly storage efficient, as long text would require more space.
- JSON does not support all types of data like dates

## BSON - MongoDB's Storage Format
Binary Javascript Object Notation, is the format MongoDB uses to store data. It is categorically different from JSON on 3 keynotes;
- It is not human readable as it is binary.
- It is storage efficient as it is binary.
- It supports a large number of data formats as it is binary.

It looks like this:
> \x00\x00\x00\x02name\x00\a\x00\x00\x00Rodney\x00\x02occupation\x00\r\x00\x00\x00photographer\x00\x10year_of_experience\x00\a\x00\x00\x00\x00

MongoDB invented BSON to bridge the gap between flexibilty and readability of JSON and required performance for large databases. MongoDB stores data as BSON internally but allows the users to create and manipulate databse data as JSON. This allows for developers to experience the best of both worlds.
