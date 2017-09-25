### Database:

* [Mongodb] (https://www.mongodb.com) [document database]
* [Redis] (https://redis.io) [key-value]
* [Logstash Kibana Elasticsearch] (https://www.elastic.co) [full text search]
* [Postgresql] (https://www.postgresql.org) [relationship database]
* [InfluxDB](https://influxdata.com/) [time series]
* [Cassandra](https://cassandra.apache.org/) [wide columns]

### Rules for setup database in production mod

* MUST setup authentication for DB
* MUST isolate DB servers within a private network (Update package via NAT Gateway)
* MUST backup data at least once in a day
* MUST set up replica set ( High Availability ) for DB
* RECOMMEND set up cluster ( Performance ) for DB
*

Links

- http://blog.cloud66.com/5-tips-for-managing-database-servers-in-production/

### Optimize a DB in general

* RULE 1: Profile first, optimize last

The basic rule of optimization is to nerver assume - ALWAYS verify, using actual data. The process of collecting performance metrics and determining performance issues is called profiling. We want to know whether database performance is responsible for a significant part of our page load time.

In mongodb we have some useful method to get database profiling

  - [cursor.explain](https://docs.mongodb.com/manual/reference/method/cursor.explain/#cursor-explain)

  - [cmdoption-profile](https://docs.mongodb.com/manual/reference/program/mongod/#cmdoption-profile)

* RULE 2: It's very important to profile using a relevant dataset. We should use data from production mod.

* RULE 3: Avoid looking at cached results.

NOTE: This is the life cycle of a query in general.Here are the steps of a query:

- Transmission of query string to database backend
- Parsing of query string
- Planning of query to optimize retrieval of data (* can optimize)
- Retrieval of data from hardware
- Transmission of results to client

#### Tips
Suppose we found out some problematic queries on slow pages. There are some basic ways to optimize query performance:

* Indexing
* Increase RAM
Many database keep most recently used data in RAM. If you have created indexes for your queries and working dataset fits in RAM. Mongo serves all queries from memory.
* Return Only Necessary Data

* Caching (REDIS)
* Latency: Choosing the correct datacenter
Latency is the network transmission time from application to database. For application-to-database latency, it will be a round trip: to the database and from the database.

### How to design database for system

- What is difference between SQL and NOSQL database ?

[Introduction to NoSQL • Martin Fowler](https://www.youtube.com/watch?v=qI_g07C_Q5I)

[nosql](https://martinfowler.com/nosql.html)

[books nosql](https://martinfowler.com/books/nosql.html)

[NoSQL Databases: An Overview](https://www.thoughtworks.com/insights/blog/nosql-databases-overview) (*)

[Polyglot Persistence](https://martinfowler.com/bliki/PolyglotPersistence.html)


### SQL vs NoSQL

- Relational Model vs Aggregate Model

