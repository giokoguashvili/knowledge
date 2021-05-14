# [Replication](https://en.wikipedia.org/wiki/Replication_(computing))
```
NewSQL
    In Memory
    Key Value
    Consistent Shrding (Distributed)
    Schemaless

Databases
    Riak 
    Couchbase
    GridGain
    Redis
    Memchashed
    Aerospike
    Apache Ignite
    Kiara DB
    VoltDB
    TimescaleDB (up from PostgreSQL)
    InfluxSB

    SQL Server
    MySQL
    PostgreSQL
    MongoDB
    Cassandra

    Tarantool
    Redis (CouchBase/Aerospike)
 
    ElasticSearch
    Kafka
    RabbitMQ


Kafka vs RabbitMQ
Akka.NET Messaging Delivery and Persistance
Event Soursong with Kafka

Latency
Throghophut
Availability
Consistency

Replication     - used for HA or read scaling
 ⁃ Sync/Async/Semi
    Sync  = local + remote commit
    Async = local commit
    Semi  = local commit + remote ack
 ⁃ Logical/Physical
    Logical
        SBR     - Statment Based Replication
        RBR/DBR - Row/Document Based Replication
        Mixed
 ⁃ Pull/Push
 ⁃ Master-Slave
   Master-Master
   Multi-Master
   Masterless
   Primary Owner

Active Replication  - which is performed by processing the same request at every replica
Passive Replication - which involves processing every request on a single replica and transferring the result to the other replicas

Sharding    - write scalling
Partitioning
Clustering

Snapshoting
    COW - Copy On Write

RPS - Request Per Second 
TPS - Transaction Per Seccond
WAL - Write Ahead Logging
AOF - Append Only File

Transaction
ACID
BASE
MVCC2PT

Sharding
    Hash function
    Routing
        Client Side
        Proxy
        Coordinator
    Select
        Map/Reduce

Service reliability 

    Uptime            Downtime (Yearly)
    99.00000%      3d 15h 39m
    99.90000%      8h 45m 56s
    99.99000%      52m 35s
    99.99900%      5m 15s
    99.99990%      31s
    99.99999%      3s


PostgreSQL
    VACUUM
    Bloat
```