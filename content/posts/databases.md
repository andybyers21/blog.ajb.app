+++
title = "SQL vs NoSQL, Relational Database Management Systems"
date = "2020-12-01"
description = "Exploring the differences between SQL and NoSQL databases and discovering the technology and use cases of each."
hideReadMore = "true"
+++

## SQL vs NoSQL

#### **RDBMS** - Relational Database Management System (i.e. SQL databases).
#### **NoSQL** - Non-Relational Database Management System.

- SQL databases are relational, NoSQL are non-relational.
- SQL databases use structured query language and have a predefined schema.
  NoSQL databases have dynamic schemas for unstructured data.
- SQL databases are vertically scalable, NoSQL databases are horizontally
  scalable.
- SQL databases are table based, while NoSQL databases are document, key-value,
  graph or wide-column stores.
- SQL databases are better for multi-row transactions, NoSQL are better for
  unstructured data like documents or JSON.

---

## RDBMS

RDBMS have been an established standard in the industry for nearly 40 years
using _the programming language SQL_. RDBMS are table based and follow a highly
organized and structured approach to data management (think Excel). And apply
strict category parameters to allow users to organise, access and manage their
data within those parameters. SQL databases are vertically scalable, which means
that you can increase the load on a single server by increasing things like CPU,
RAM or SSD.

### Advantages

- They are highly stable and reliable.
- They adhere to an industry recognized standard (with [[Tech-Stacks]] like
  LAMP)
- Because they've been around for so long, support options are abundant.
- ACID compliance. If a database system is "ACID compliant," it satisfies a set
  of priorities that measure the atomicity, consistency, isolation, and
  durability of database systems. The more ACID-compliant a database is, the
  more it serves to guarantee the validity of database transactions, reduce
  anomalies, safeguard data integrity, and create stable database systems.
  Generally, SQL-based RDBMSs achieve a high level of ACID compliance.

### Disadvantages

- Scalability challenges,
- These databases also present challenges when it comes to sharding. _Sharding
  is the process of dividing a large database into smaller parts for easier
  management._
- Less efficient with NoSQL formats: Most RDBMSs are now compatible with NoSQL
  data formats, but they don't work with them as efficiently as non-relational
  databases.

### Use Cases

- Ideal for consistent data systems, your information will remain in the
  structure you originally create.
- If you don't need a dynamic information system for massive amounts of data—and
  you're not dealing with numerous data types an RDBMS offers great speed and
  stability.

If you're dealing with a conservative database that you don't expect to change a
lot in the years ahead, the sharding and scaling challenges related to RDBMS
solutions may never apply to you. On the other hand, if you plan to scale up and
grow in the years ahead, a non-relational database system (NoSQL-based) could be
a better match for your needs.

### Popular RDBMS/SQL Databases

#### MySQL

_Open Source_, frequent security and features updates. (Paid versions exist for
enterprise). Mature, pre-defined structure and set schemas. High compatibility.
Good for use cases that require multi-row transactions like accounting or
inventory management.

#### PostgreSQL

**PostgreSQL is a hybrid SQL/NoSQL database system that finds a middle-ground
between these two options** - _Open Source_, highly compatible, Highly ACID
Compliant, Massive Scalability. _Object Oriented Database Management_, excellent
when your data doesn't mesh well with a perfectly relational model. PostgreSQL
is highly trusted and supported (it's been around since the early 1990s). It
works well with extra-large databases and for performing complicated queries.

---

## NoSQL

NoSQL databases are built to handle large amounts of unstructured data such as
email, text, surveys, social media etc. Data schemes are only loosely defined
and easy to modify or add to where required. (Similar to the file system on your
PC). _NoSQL databases give up the distinction of ACID compliance to gain speed
and flexibility when dealing with unstructured data._ NoSQL databases are
horizontally scalable, this means that you handle more traffic by sharding, or
adding more servers in your NoSQL database.

### Advantages

- Excellent for handling "big data" analytics. They remove bottlenecks of
  needing to categorize data and apply structures before analysing it.
- _Easy to scale, they are designed to be fragmented_ (across data-centres for
  example)
- No limits on data types that can be stored.
- You can store unstructured information and expose it to powerful business
  intelligence systems to analyse it.
- You can store unstructured data that you may want to structure later.
- Less up front data prep.
- Non-relational databases work with formats like JSON for web-based
  applications that let websites update "live" without needing to refresh the
  page.

### Disadvantages

- As NoSQL is relatively new there may be less opportunities to find support.
- Less tools available.
- There may be compatibility with older RDBMS systems.

### Use Cases

- NoSQL databases the preferred choice for large or ever-changing data sets.

### Popular NoSQL Databases

#### MongoDB

_Open Source_, Dynamic Schema, Highly Scalable, Manageable and high speed.
MongoDB is a good choice for businesses that have rapid growth or databases with
no clear schema definitions or if you find yourself denormalizing data schemas.
Or if your data requirements and schemas are constantly evolving - as is often
the case with mobile apps, real-time analytics us and content management systems,
etc. Perfect for building an application on top of an operational database and
you need a really fast response time.

#### Cassandra

_Open Source_, originally created by Facebook but ownership has been transferred
to Apache. Active everywhere, users can write and read from all Cassandra nodes.
Highly scalable. Cassandra benefits from a "masterless design." That means all
of its nodes are identical, which creates operational simplicity, making it easy
to scale up to a larger database architecture. _Support for SQL_. Offers
excellent data protection. Note, Cassandra is **not** optimized for updating and
deleting data.

Cassandra is most popular for use with IoT (internet of things) technology
because it offers fast, real-time insights and excels at writing time-based log
activities, error logging, and sensor data. If you need fast read and write
processing, Cassandra could be your database. Cassandra is also good for those
who want to work with SQL-like data types on a NoSQL database.

#### BigTable

_Google owned paid service_. Sub 10ms latency guaranteed. Replication. Easy to
integrate, highly scalable. Highly compatible with Google services. Fully
managed with Integrations which reduces workload requirements. It also
integrates instantly with many platforms, which streamlines the ETL processes
required to load data.

Machine learning: BigTable features a storage engine for use with machine
learning applications. BigTable can also be used for fin-tech, IoT, and
advertising technology

#### Apache HBase

_Open Source_, modeled after Google's BigTable. Created to work with large data
sets. Excellent at scaling across a cluster. HBase organizes rows into
"regions." The regions determine how the table will be divided across more than
one node that make up a cluster. If one of the regions is too big, HBase
automatically breaks it up to evenly distribute the load across more than one
server. Works with both unstructured and semi-structured data. The Apache HBase
website advises to use HBase "when you need random, realtime read/write access
to your big data." The database is designed to host massive tables of
information that include billions of rows and millions of columns.

---

## How to Chose the Right Database

There are many differing factors that come into play when choosing a database
for your project but 3 big factors may be:

- Atomicity. If atomicity is a top priority for you, stick to a relational
  database.
- Scalability (and sharding).
- Speed. If speed is more important than ACID compliance, a non-relational
  database, such as a document database, is a better bet.
