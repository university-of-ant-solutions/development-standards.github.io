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
