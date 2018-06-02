# Microservices

- [Distributed Transactions: The Icebergs of Microservices](http://www.grahamlea.com/2016/08/distributed-transactions-microservices-icebergs/)
- [Microservices, SOA, and APIs: Friends or enemies?](https://www.ibm.com/developerworks/websphere/library/techarticles/1601_clark-trs/1601_clark.html)
- [Why The Future Of Software And Apps Is Serverless](https://readwrite.com/2012/10/15/why-the-future-of-software-and-apps-is-serverless/)

### Videos:

- [Neal Ford - Building Microservice Architectures](https://www.youtube.com/watch?v=pjN7CaGPFB4)
- [Microservices and Rules Engines – a blast from the past - Udi Dahan](https://www.youtube.com/watch?v=Fuac__g928E)

### PDFs:

- [Your Coffee Shop Doesn’t Use Two-Phase Commit](https://martinfowler.com/ieeeSoftware/coffeeShop.pdf)

### Projects:

- [Workshop (with examples in NServiceBus)](https://github.com/Particular/Workshop)

### [Interservice communication](https://docs.microsoft.com/en-us/azure/architecture/microservices/interservice-communication)

- [What’s a service mesh? And why do I need one?](https://buoyant.io/2017/04/25/whats-a-service-mesh-and-why-do-i-need-one/)
- [Service Mesh vs API Gateway](https://medium.com/microservices-in-practice/service-mesh-vs-api-gateway-a6d814b9bf56)
- [How Containers Scale: Service Mesh vs. Traditional Architecture](https://dzone.com/articles/how-containers-scale-service-mesh-vs-traditional-a)
- [What is a Service Mesh and how Istio fits in](https://developer.ibm.com/code/2017/07/21/service-mesh-architecture-and-istio/)

### Event-driven architecture:

#### Comment by [mettjus] on video [GOTO 2017 • The Many Meanings of Event-Driven Architecture • Martin Fowler](https://www.youtube.com/watch?v=STKCRSUsyP0)
events/commands: the difference between Event and Command is really deeper than just naming. IMO it's the same difference that occurs between "choreography" and "orchestration". Moreover I would say the kind of queues used for the 2 types of "messaging" have different requirements: message-persistence/multiple-consumption in case of Events (eg. I don't know who and when will be interested in this event, an I would use something like Kafka for it), message-acknowledgment/single-consumption in case of Commands (eg. I am giving an instruction right now to a specific executor of that instruction (actually the executor I could not know but the nature of the action I know), and I would maybe use something like RabbitMQ)

- [Understanding When to use RabbitMQ or Apache Kafka](https://content.pivotal.io/blog/understanding-when-to-use-rabbitmq-or-apache-kafka)
- [Events, Flows and Long-Running Services: A Modern Approach to Workflow Automation](https://www.infoq.com/articles/events-workflow-automation)

### Books
- [Reactive Microservices Architecture - Design Principles for Distributed Systems](https://theswissbay.ch/pdf/_to_sort/O%27Reilly/reactive-microservices-architecture-orm.pdf)
