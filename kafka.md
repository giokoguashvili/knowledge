# Kafka

### [Perfomance](https://www.confluent.io/kafka-vs-pulsar/)
- Aapache Kafka
- Aapache Pulsar
- RabbitMQ (AMQP)


### Blog Posts
- [Apache Kafka Design](http://kafka.apache.org/documentation.html#design) - kafka.apache.org
- [RabbitMQ vs Kafka Part 1 - Two Different Takes on Messaging](https://jack-vanlightly.com/blog/2017/12/4/rabbitmq-vs-kafka-part-1-messaging-topologies) - jack-vanlightly.com
- [Kafka in a Nutshell](https://sookocheff.com/post/kafka/kafka-in-a-nutshell/#:~:text=Kafka%20topics%20are%20divided%20into,from%20a%20topic%20in%20parallel.) - sookocheff.com
- [Avoiding Data Loss](https://docs.cloudera.com/HDPDocuments/HDP2/HDP-2.6.4/bk_kafka-component-guide/content/avoiding-data-loss.html) - docs.cloudera.com
- [When you can lose messages in Kafka](https://developer20.com/when-you-can-nose-messages-in-kafka/) - developer20.com
- [Apache Kafka Idempotent Producer - Avoiding message duplication](https://www.cloudkarafka.com/blog/apache-kafka-idempotent-producer-avoiding-message-duplication.html) - cloudkarafka.com
- [Kafka — Idempotent Producer And Consumer](https://medium.com/@shesh.soft/kafka-idempotent-producer-and-consumer-25c52402ceb9) - medium.com
- [Help, Kafka ate my data!](https://blog.softwaremill.com/help-kafka-ate-my-data-ae2e5d3e6576) - blog.softwaremill.com
- [Does Kafka really guarantee the order of messages?](https://blog.softwaremill.com/does-kafka-really-guarantee-the-order-of-messages-3ca849fd19d2) - blog.softwaremill.com
- [Apache Kafka Rebalance Protocol, or the magic behind your streams applications](https://medium.com/streamthoughts/apache-kafka-rebalance-protocol-or-the-magic-behind-your-streams-applications-e94baf68e4f2#:~:text=Kafka%20Connect%20uses%20the%20group,when%20configuration%20is%20submitted%2Fupdated.) - medium.com


### Client Docs
- [javadoc](https://kafka.apache.org/0100/javadoc/index.html?org/apache/kafka/clients/consumer/KafkaConsumer.html) - kafka.apache.org
- [Introduction to librdkafka - the Apache Kafka C/C++ client library](https://github.com/edenhill/librdkafka/blob/master/INTRODUCTION.md) - github.com

### UI Tools
- [Confluent Platform](https://docs.confluent.io/platform/current/kafka/kafka-basics.html)
- [KADEK Controle Center](https://www.xeotek.com/)
- [Kafka Magic](https://www.kafkamagic.com/)
- [Conductor](https://www.conduktor.io/)
- [Offset Explorer - Kafka Tool](https://www.kafkatool.com/)
- 
### [Confluent Tutorials](https://kafka-tutorials.confluent.io/)
- [Console Producer and Consumer Basics, no (de)serializers](https://kafka-tutorials.confluent.io/kafka-console-consumer-producer-basics/kafka.html)
- [How to read from a specific offset and partition with the Kafka Console Consumer](https://kafka-tutorials.confluent.io/kafka-console-consumer-read-specific-offsets-partitions/kafka.html)

### Videos
- [Youtube Playlist](https://www.youtube.com/watch?v=A_yUaPARv8U&list=PL2XGvKfYRbDsiHlCfLDh0pGdk-0Dykxfy)

### Q&A
- Stackoverflow
 - [Consuming from single kafka partition by multiple consumers](https://stackoverflow.com/questions/57952538/consuming-from-single-kafka-partition-by-multiple-consumers)
 - [How to implement Exactly-Once Kafka Consumer without manually assigning partitions](https://stackoverflow.com/questions/58029989/how-to-implement-exactly-once-kafka-consumer-without-manually-assigning-partitio)
 - [using assign instead of subscribe in kafka consumer side](https://stackoverflow.com/questions/52051849/using-assign-instead-of-subscribe-in-kafka-consumer-side)
 - [Need to understand kafka broker property “log.flush.interval.messages”](https://stackoverflow.com/questions/33970374/need-to-understand-kafka-broker-property-log-flush-interval-messages)
 - [Kafka - min.insync.replicas interpretation](https://stackoverflow.com/questions/62326946/kafka-min-insync-replicas-interpretation/)

### Settings
```
- replication-factor=3
- min.insync.replicas=1
- acks=-1
- unclean.leader.election.enable
- log.flush.interval

- replica.lag.time.max.ms
    We refer to nodes satisfying these two conditions as being "in sync" to avoid the vagueness of "alive" or "failed". 
    The leader keeps track of the set of "in sync" nodes. If a follower dies, 
    gets stuck, or falls behind, the leader will remove it from the list of in sync replicas. 
    The determination of stuck and lagging replicas is controlled by the replica.lag.time.max.ms configuration.


kafka-console-producer --topic Topic-3 --bootstrap-server broker:9092 --property parse.key=true --property key.separator=":"
```