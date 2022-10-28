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

## CRUD in MongoDB
MonogDB can be easily run in a terminal using the MongoDB Shell, `mongosh`. MongoDB allows us to store multiple databases inside of a single running instance.
> `show dbs` - show all the databases running in our instance and the space they are occupying.

There are 3 unique databases by default called the admin, local and config that are included by MongoDB to help configure our instance.

> `use <db_name>` - will select that database to work on. If the said DB does not exists then MongoDB will create a new DB and place us inside it.

> `db` - outputs the name of the current database that we are in.

### What is Querying?
Querying is the process by which we erquest the data from the database.

After we get inside a DB, we can read the data by using the find() that would fetch the objects that match our query.

> `db.collection_name.find()` - fetches the object that is the result of our query. We pass arguments in the form of objects
> 
> `it` - since all the data is not returned at once, we can use it that stands for iterate to view the rest of the data.

The find() uses an operator to find matches to our query. An operator is a special syntax that specifies some logical action that we want to perform when our command executes. Incase of find() it uses the equality operator, ie, $eq to match documents that include the specified field and value.

We can also explicitly include the equality operator by giving the parameter as 
```javascript
{
  <field>: {$eq}: value 
}
```
which is equivalent to 
```javascript
{
    <field>: <value>
}
```

We can also embed our documents within documents, ie, in a parent-child relationship. To access the child items of a document, we can have to use the standard dot notation but enclose them in quotes.

MongoDB provides us with other operators as well, like `$gt`, `$gte`, `$lte` and `$lt`, something like this;
```javascript
db.<collection>.find( { <field>: { $gt: <value> } } )
```

Suppose we want to sort our data that we fetch form our find(). To achieve that we use the `db.collection_name.find().sort()`, ie, we chain it to our find() and then we pass in some arguments in the form of json. The values that these arguments take are either 1 (ascending) or -1 (descending)

### Query Projections
Suppose the document that we are accessing is very large and detailed. So whenever we run a find() then the entire document will be returned by us thereby making our work more tedious. So to tackle that we can use `projections` of our dataset, ie, just view only the fields that we want and omit the rest. Kind of like a filter.

To make projections we pass in a second argument to our find(), an object where we can only give the name of fields on the document as keys with only 0 (hide) and 1 (show) values. The _id is automatically displayed, but we can hide it by passing 0 for it. Also we can only have inclusion and exclusion queries at once with _id. If we were to add 0 to some other fields and 1 to others, then mongosh will throw a `MongoServerError`. 


### Querying an Array
Suppose we have a book where each document has a field called genres which is an array. So if we want to filter only those books that have a certain genres in them then we will have to pass those genres as an array in the find() but that would be completely inaccurate because that would only fetch us those results where the genre field has only those genres and that too in that specific order. 

To counter that we have the ability to match individual elements that occur in the array from what we have learnt in previous lessons. But if suppose we want to match an array then in that case we can use `$all` operator that would look for the said keywords in all the fields regardless of their order. 

We can also query on an array by using multiple filters, ie, 
```javascript
db.<collection>.find({ <field>: { <operator>: <value>, <operator2>: <value2>, … } })
```
All we need to do is pass the operators as objects as the value to the field where we want to place a filter at.
