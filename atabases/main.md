# [Databases](https://db-engines.com/en/system/Amazon+Aurora%3BAmazon+DynamoDB%3BGoogle+Cloud+Spanner%3BMicrosoft+Azure+Cosmos+DB%3BMicrosoft+SQL+Server)


### [Types of databases](https://medium.com/swlh/4-types-of-nosql-databases-d88ad21f7d3b)

- SQL Databases
	- Relational (OLTP)
	- Analytical (OLAP)
- NoSQL Databases
	- Document databases
	- Key-value stores
	- Column-oriented databases
	- Graph databases
- NewSQL
	- In Memory
	- Key Value
	- Consistent Shrding (Distributed)
	- Schemaless

- Stream Processing
	- Spark
	- Flink
	- Samza
	- Hadoop
	- [Comparing Apache Spark, Storm, Flink and Samza stream processing engines - Part 1](https://blog.scottlogic.com/2018/07/06/comparing-streaming-frameworks-pt1.html)

- [Build modern apps with big data at a global scale](https://www.arbelatech.com/insights/white-papers/build-modern-apps-with-big-data-at-a-global-scale) - pdf

### Docs
- [Amazon Aurora](docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html)
- [Amazon DynamoDB](docs.aws.amazon.com/dynamodb)
- [Google Cloud Spanner](	cloud.google.com/spanner/docs)

### Posts
- [NoSQL Databases: An Overview](https://www.thoughtworks.com/insights/blog/nosql-databases-overview)
- [Graph Databases for Beginners: A Tour of Aggregate Stores](https://neo4j.com/blog/aggregate-stores-tour/)
- [RDBMSs vs. NoSQL Databases: Overview](http://maxivak.com/rdbms-vs-nosql-databases/)

### Databases

- Riak 
- Couchbase
- GridGain
- Redis
- Memchashed
- Aerospike
- Apache Ignite
- Kiara DB
- VoltDB
- TimescaleDB (up from PostgreSQL)
- InfluxSB
- 
- SQL Server
- MySQL
- PostgreSQL
- MongoDB
- Cassandra
- 
- Tarantool
- Redis (CouchBase/Aerospike)
- 
- ElasticSearch
- Kafka
- RabbitMQ




![Visual Guide to NoSQL Systems](http://maxivak.com/wp-content/uploads/2011/07/media_httpfarm5static_mevIk.png)

# NoSQL
### NoSQL Meanings
	Not Only SQL
	No SQL
	New SQL

- Key-Value
	- Raik, Redis, Memchaced, BerkelyDB, upscaledb, Couchbase
- Document Database:
	- MongoDB, CouchDB, Terrastore, OrientDB, RavenDB
- Column family stores:
	- Casandta, HBase, Hypertable, Amazon DynamoDB
- Graph Databases
	- Neo4j, Infinite Graph, OrientDB, FolckDB

### Q&A
- Stackoverflow
  - [Difference between Sharding and Replication](https://stackoverflow.com/a/11571916/5200896)
- Quora
  - [Why is MongoDB losing popularity?](https://www.quora.com/Why-is-MongoDB-losing-popularity)


```
Concurrency control
	2PL - 2 Phase Locking
	Deadlock detection
	Multi version concurrency control

Recovery
	Write ahead log
	Redo
	Undo

Distributed transactions
	2PC - 2 Phase Commit 
	Distributed recovery
```