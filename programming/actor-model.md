# [Actor Model](https://en.wikipedia.org/wiki/Actor_model)

The actor model in computer science is a mathematical model of concurrent computation 
that treats "actors" as the universal primitives of concurrent computation. 
In response to a message that it receives, an actor can: make local decisions, create more actors, send more messages, and determine how to respond to the next message received. Actors may modify their own private state, but can only affect each other through messages (avoiding the need for any locks).

As computational entities, actors have these characteristics, this is similar to the everything is an object philosophy used by some object-oriented programming languages:

- They communicate with asynchronous messaging instead of method calls
- They manage their own state
- When responding to a message, they can:
  - Create other (child) actors
  - Send messages to other actors
  - Stop (child) actors or themselves
  
![1_kh_lpsu18rzhrliekhomuq](https://user-images.githubusercontent.com/8178412/36524009-bcb782ea-17bd-11e8-8856-d09708f33b02.png)

# [Terminology and Concepts](http://getakka.net/articles/concepts/terminology.html)

- Concurrency vs. Parallelism
- Asynchronous vs. Synchronous
- Non-blocking vs. Blocking
- Deadlock vs. Starvation vs. Live-lock
- Race Condition
- Non-blocking Guarantees (Progress Conditions)
  - Wait-freedom
  - Lock-freedom
  - Obstruction-freedom
  
### Concurrency
![concurrency](https://user-images.githubusercontent.com/8178412/36524619-077aa3f0-17c0-11e8-9f89-9297eb75dc6d.png)
### Parallelism
![parallelism](https://user-images.githubusercontent.com/8178412/36524620-07993e46-17c0-11e8-9002-d65da3e7a1fb.png)

# History
According to Carl Hewitt, unlike previous models of computation, the actor model was inspired by physics, including general relativity and quantum mechanics. It was also influenced by the programming languages Lisp, Simula and early versions of Smalltalk


# Posts
- [Akka.NET: What is an Actor?](https://github.com/petabridge/akka-bootcamp)
- [What problems does the actor model solve?](http://getakka.net/articles/intro/what-are-actors.html)

# Videos
- [Hewitt, Meijer and Szyperski: The Actor Model (everything you wanted to know...)](https://www.youtube.com/watch?v=7erJ1DV_Tlo)

# FAQ
- [What is the difference between Actor model and Microservices?](https://softwareengineering.stackexchange.com/a/338899/273636)
