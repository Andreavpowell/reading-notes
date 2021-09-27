# SQL vs NoSQL Database

## SQL

- SQL databases are primarily called as Relational Databases (RDBMS)
- table-based
- predefined schema
- vertically scalable by increasing the horse-power of the hardware
- uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful

## NoSQL

- NoSQL database are primarily called as non-relational or distributed database
- document based, key-value pairs, graph databases or wide-column stores
- dynamic schema for unstructured data
- horizontally scalable by increasing the databases servers in the pool of resources to reduce the load
- queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database

## Questions:

- What kind of data is a good fit for an SQL database?
  - SQL databases are good fit for the complex query intensive environment.
- Give a real world example.
- What kind of data is a good fit a NoSQL database?
  - NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
- Give a real world example.
- Which type of database is best for hierarchical data storage?
  - NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data.
- Which type of database is best for scalability?
  - In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.
- What does SQL stand for?
  - Structured Query Language
- What is a relational database?
  - Tables of data tied together. Relational Databases are called "Relational" because the whole database is based on Relational Algebra that Edgar Codd created. That algebra provides operations like projection and join.
- What type of structure does a relational database work with?
  - Tables
- What is a ‘schema’?
  - Normalized fields(columns) of data in a table
the way data is organized.
- What is a NoSQL database?
  - A DB not using SQL structure
- How does it work?
  - Data collections which contain documents and doesn't require schema.
- What is inside of a Mongo database?
  - Data inside documents
- Which is more flexible - SQL or MongoDB? and why.
  - MongoDB is more flexible. It allows for storage of different formats of data, allows for horizontal scaling, and is not required to be relational.
- What is the disadvantage of a NoSQL database?
  - Duplicate data may be requiem.

### Sources: [Database Differences Explained with few Example DB](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool), [SQL vs NoSQL Video](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

## Things I want to know more about:
- C#
- Different Databases

[Home](reading-notes.md)