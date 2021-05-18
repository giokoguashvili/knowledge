# [Replication](https://en.wikipedia.org/wiki/Replication_(computing))


## Reason
- To keep data geographically close to your users (and thus reduce access latency) 
- To allow the system to continue working even if some of its parts have failed (and thus increase availability) 
- To scale out the number of machines that can serve read queries (and thus increase read throughput)

## Replication Architectures
- Single-leader
    - Master-Slave
- Multi-leader 
    - Multi-Master
- Leaderless
    - Master-Master
    - Masterless
    - Primary Owner

- Sync/Async/Semi
    - Synchronously  - local + remote commit
    - Asynchronously - local commit
    - Semi  - local commit + remote ack

- Logical/Physical
    - Logical
        - SBR           - Statment Based Replication
        - WAL Shipping  - Write-Ahead Log  Shipping
        - RBR/DBR       - Row/Document Based Replication
        - Mixed
- Pull/Push

## Multi-Leader Replication Topologies
- Circular topology
- Star topology
- All-to-all topology

## Types
- Active Replication - which is performed by processing the same request at every replica
- Passive Replication - which involves processing every request on a single replica and transferring the result to the other replicas


```
Kafka vs RabbitMQ
Akka.NET Messaging Delivery and Persistance
Event Soursong with Kafka

Snapshoting
    COW - Copy On Write

RPS - Request Per Second 
TPS - Transaction Per Seccond
QPS - Query rate Per Second 
WAL - Write Ahead Logging
AOF - Append Only File

SC  - strong consistency
HA  - high throughput
HT  - high availability
```

## Problems with Replication Lag 
- Read-after-write consistency 
> Users should always see data that they submitted themselves
- Monotonic Reads 
> After users have seen the data at one point in time, they shouldn’t later see the data from some earlier point in time
- Consistent Prefix Reads
> Users should see the data in a state that makes causal sense: for example, seeing a question and its reply in the correct order

## Papers
- [Chain Replication for Supporting High Throughput and Availability](https://www.cs.cornell.edu/home/rvr/papers/OSDI04.pdf)

## Q&A
- [Difference between Stream Replication and logical replication](https://stackoverflow.com/questions/33621906/difference-between-stream-replication-and-logical-replication) - stackoverflow.com

