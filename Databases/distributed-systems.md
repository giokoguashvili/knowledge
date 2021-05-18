# [Distributed Systems](https://gousios.org/courses/bigdata/dist-databases.html) - gousios.org

> A collection of independent computers that appear to its users as one computer. **- Andrew Tannenbaum**

### Three Characteristics

- The computers operate concurrently
- The computers fail idependently
- The computers do not share a global clock

### Properties
- Latency
- Throghophut
- Availability
- Consistency

### Fundamental problems in distributed systems
- Replica Consistency
- Durability
- Availability
- Latency

### Tools:

- **Storage:** Relation/Mongo, Cassandra, HDFS 
- **Computation:** Hadoop, Spark, Storm
- **Synchronization:** NTP, vector clocks
- **Consensus:** Paxos, Zookeeper
- **Messaging:** Kafka

### Technique

- [Partitioning](https://en.wikipedia.org/wiki/Partition_(database)#Partitioning_methods)
- [Replication](https://en.wikipedia.org/wiki/Replication_(computing))
- [Sharding](https://en.wikipedia.org/wiki/Shard_(database_architecture))
- [Consistent Hashing](https://www.toptal.com/big-data/consistent-hashing)
- **Distributed Transactions**
- [The Raft Consensus Algorithm](https://raft.github.io/)
- Clustering

# System Properties Comparison

- [Amazon Aurora vs. Amazon DynamoDB vs. Google Cloud Spanner vs. Microsoft Azure Cosmos DB vs. Microsoft SQL Server](https://db-engines.com/en/system/Amazon+Aurora%3BAmazon+DynamoDB%3BGoogle+Cloud+Spanner%3BMicrosoft+Azure+Cosmos+DB%3BMicrosoft+SQL+Server)
- [Amazon DynamoDB vs. Cassandra vs. CouchDB vs. Riak KV](https://db-engines.com/en/system/Amazon+DynamoDB%3BCassandra%3BCouchDB%3BRiak+KV)
- [Aerospike vs. Couchbase vs. Redis](https://db-engines.com/en/system/Aerospike%3BCouchbase%3BRedis)


# Glossary
### [Amazon's Dynamo](https://www.allthingsdistributed.com/2007/10/amazons_dynamo.html)
- Partitioning
  - Consistent Hashing
- Handling temporary failures
  - Sloppy Quorum 
  - Hinted handoff
- Conflicts
  - LWW - Last Write Win
  - Vector Clocks
  - [CRDT - Conflict-free replicated data type](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type)
    - [Delta CRDT](https://arxiv.org/pdf/1603.01529.pdf)
    - [A Conflict-Free Replicated JSON Datatype](https://arxiv.org/pdf/1608.03960.pdf)
- Membership and failure detection
  - Gossip-based membership protocol and failure detection.

- Consensus Algorithms
  - [Paxos](https://en.wikipedia.org/wiki/Paxos_(computer_science)) - wikipedia.org
  - [Raft](https://raft.github.io/) - raft.github.io
  - [Zab](https://cwiki.apache.org/confluence/display/ZOOKEEPER/Zab+vs.+Paxos)
- Service Discovery Systems
  - [Zookeeper](https://zookeeper.apache.org/doc/r3.6.2/zookeeperInternals.html)
  - [Consul](https://www.consul.io/docs/intro)
  
- Multi-Master Replication
- Replication Factor
- Bidirectonal Replicaiton
...


# Service reliability 

    Uptime            Downtime (Yearly)
    99.00000%      3d 15h 39m
    99.90000%      8h 45m 56s
    99.99000%      52m 35s
    99.99900%      5m 15s
    99.99990%      31s
    99.99999%      3s