---
description: Database
keywords: Database
title: About Database
---

## Database:

* [Mongodb](https://www.mongodb.com) [document database]
* [Redis](https://redis.io) [key-value]

  - http://redislabs.lookbookhq.com/c/wp-redis-labs-popula?x=DACO2h&mkt_tok=eyJpIjoiTXpjek9EQmtPRFUxTTJZMSIsInQiOiJZMEoyRms0TGpBanp6ZjlhYjRNbmU2eUxFVytvb3Z2NVpWR0dKYlFqNjhaTDJoZmd0SEplS2c1dHB1MEVTbk01SmRGZ2pIS0lCRHVTR1V3RElrcWo2NHR5WTJKcGY3VlRYbVVTcnd0OXliNWVMalVWaE1hN2pWWDhVeENZMHFCZSJ9&utm_campaign=why+your+mongodb+needs+redis&utm_medium=email+campaign+10-05-17&utm_source=white+paper

* [Logstash Kibana Elasticsearch](https://www.elastic.co) [full text search]
* [Postgresql](https://www.postgresql.org) [relationship database]
* [InfluxDB](https://influxdata.com/) [time series]
* [Cassandra](https://cassandra.apache.org/) [wide columns]

## Rules for setup database in production mod

* MUST setup authentication for DB
* MUST isolate DB servers within a private network (Update package via NAT Gateway)
* MUST backup data at least once in a day
* MUST set up replica set ( High Availability ) for DB
* RECOMMEND set up cluster ( Performance ) for DB
*

Links

- http://blog.cloud66.com/5-tips-for-managing-database-servers-in-production/

## Optimize a DB in general

* RULE 1: Profile first, optimize last

The basic rule of optimization is to nerver assume - ALWAYS verify, using actual data. The process of collecting performance metrics and determining performance issues is called profiling. We want to know whether database performance is responsible for a significant part of our page load time.

In mongodb we have some useful method to get database profiling

  - [cursor.explain](https://docs.mongodb.com/manual/reference/method/cursor.explain/#cursor-explain)

  - [cmdoption-profile](https://docs.mongodb.com/manual/reference/program/mongod/#cmdoption-profile)

* RULE 2: It's very important to profile using a relevant dataset. We should use data from production mod.

* RULE 3: Avoid looking at cached results.
