# [CAP](http://www.julianbrowne.com/article/viewer/brewers-cap-theorem)

1. Consistency    
   * Every read receives the most recent write or an error    
2. Availability    
   * Every request receives a (non-error) response – without guarantee that it contains the most recent write    
3. Partition tolerance
   * The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes

```
A distributed data store is a computer network where information is stored on more than one node, often in a replicated fashion.

[1] It is usually specifically used to refer to either a distributed database where users store information on a number of nodes, 
or a computer network in which users store information on a number of peer network nodes.

states that it is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees
```

# [Persistence Ignorance](http://deviq.com/persistence-ignorance/)
  * The principle of Persistence Ignorance (PI) holds that classes modeling the business domain in a software application should not be impacted by how they might be persisted. 

# [CQRS](https://martinfowler.com/bliki/CQRS.html)
```
CQRS is not a silver bullet
CQRS is not a top level architecture
CQRS is not new
CQRS is not shiny
CQRS will not make your jump shot any better
CQRS is not intrinsically linked to DDD
CQRS is not Event Sourcing
CQRS does not require a message bus
CQRS is not a guiding principle / CQS is
CQRS is not a good wife
CQRS is learnable in 5 minutes

CQRS is a small tactical pattern

CQRS can open many doors.
```

CQS - Command and Query Separation.
    https://en.wikipedia.org/wiki/Command%E2%80%93query_separation

CQRS - Command Query Responsibility Segregation. 


1. http://codebetter.com/gregyoung/2010/02/16/cqrs-task-based-uis-event-sourcing-agh/
    * CQRS is a very simple pattern that enables many opportunities for architecture that may otherwise not exist.
    * In other words the interesting stuff is not really the CQRS pattern itself but in the architectural decisions that can be made around it. 
http://codebetter.com/gregyoung/2009/08/13/command-query-separation/
http://cqrs.nu/Faq/command-query-responsibility-segregation

========================== CQS vs CQRS =====================================

http://www.axonframework.org/docs/2.3/single.html
https://www.codeproject.com/Articles/991648/CQRS-A-Cross-Examination-Of-How-It-Works
https://www.exceptionnotfound.net/real-world-cqrs-es-with-asp-net-and-redis-part-1-overview/

CQS vs CQRS - http://cqrs.nu/Faq/command-query-responsibility-segregation

* CQS puts commands and queries in different methods within a type.
* CQRS puts commands and queries on different objects.

Without CQS 
```
    // All methods (queries and commands) in one class
    public class CustomerService 
    {
        // Method performs action and returns data
        public Customer UpdatePositionAndReturnCustomer(int customerId, int positionId) { ... };
    }
```

CQS - spliting responsibilities over Methods

```
    // All methods (queries and commands) in one class
    public class CustomerService 
    {
        // Method performs action
        public void UpdatePosition(int customerId, int positionId) { ... }
        // Method returns data
        public Customer GetCustomer(int customerId) { ... }
    }
```

CQRS - spliting responsibilities over Classes

```
    // Only methods in which performs action
    public class CustomerWriteService 
    {
        // Method performs action
        public void UpdatePosition(int customerId, int positionId) { ... }
    }

    // Only methods which returns data
    public class CustomerReadService
    {
        // Method performs data
        public Customer GetCustomer(int customerId) { ... }
    }
```

========================= System Requirements ==================================

http://www.julianbrowne.com/article/viewer/systemic-requirements

======================== ACID and BASE =========================================
BASE - http://www.dataversity.net/acid-vs-base-the-shifting-ph-of-database-transaction-processing/
    * Basically Available
    * Soft state
    * Eventual consistency

ACID - https://en.wikipedia.org/wiki/ACID
    * Atomicity
        Atomicity requires that each transaction be "all or nothing"
    * Consistency
        The consistency property ensures that any transaction will bring the database from one valid state to another.
    * Isolation
        The isolation property ensures that the concurrent execution of transactions results 
        in a system state that would be obtained if transactions were executed sequentially, i.e., one after the other.
    * Durability
        The durability property ensures that once a transaction has been committed, it will remain so, even in the event of power loss, crashes, or errors.


================== All Links ==============================
+     http://codebetter.com/gregyoung/2010/02/16/cqrs-task-based-uis-event-sourcing-agh/
+     http://codebetter.com/gregyoung/2009/08/13/command-query-separation/
+     http://codebetter.com/gregyoung/2010/02/20/cqrs-and-cap-theorem/
+/-     http://www.julianbrowne.com/article/viewer/brewers-cap-theorem
+/-     https://en.wikipedia.org/wiki/ACID
-     http://www.julianbrowne.com/article/viewer/systemic-requirements
+     https://goodenoughsoftware.net/2012/03/02/cqrs/

+     http://codebetter.com/gregyoung/2012/09/09/cqrs-is-not-an-architecture-2/
-    http://enterprisecraftsmanship.com/2015/04/20/types-of-cqrs/
+     https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/cqrs
+/-    https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs
+/-     https://msdn.microsoft.com/library/ms978509.aspx

=============================================================

While CQRS touches on many pieces of software architecture, it is still not at the top of the food chain. 
CQRS if used is employed within a bounded context (DDD) or a business component (SOA) – a cohesive piece of the problem domain. 


====================== CRUD =================================
CRUD is data-oriented

+ https://msdn.microsoft.com/library/ms978509.aspx


======================= DDD ===================================

Terms: http://dddcommunity.org/resources/ddd_terms/


!!!!!!!!!!!!!! 
https://medium.com/technology-learning/event-sourcing-and-cqrs-a-look-at-kafka-e0c1b90d17d8
https://www.confluent.io/blog/event-sourcing-cqrs-stream-processing-apache-kafka-whats-connection/


======================== Saga ===================================

http://vasters.com/archive/Sagas.html
https://lostechies.com/jimmybogard/2013/03/21/saga-implementation-patterns-variations/
http://www.enterpriseintegrationpatterns.com/patterns/messaging/ProcessManager.html

Frameworks:
https://particular.net/nservicebus
https://geteventstore.com/
