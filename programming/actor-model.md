# [Actor Model](https://en.wikipedia.org/wiki/Actor_model)

The actor model in computer science is a mathematical model of concurrent computation 
that treats "actors" as the universal primitives of concurrent computation. 
In response to a message that it receives, an actor can: 

1. make local decisions
2. create more actors
3. send more messages, and determine how to respond to the next message received

Actors may modify their own private state, but can only affect each other through messages (avoiding the need for any locks).

![1_kh_lpsu18rzhrliekhomuq](https://user-images.githubusercontent.com/8178412/36524009-bcb782ea-17bd-11e8-8856-d09708f33b02.png)

# Posts
- [Akka.NET: What is an Actor?](https://github.com/petabridge/akka-bootcamp)
- [What problems does the actor model solve?](http://getakka.net/articles/intro/what-are-actors.html)

# Videos
- [Hewitt, Meijer and Szyperski: The Actor Model (everything you wanted to know...)](https://www.youtube.com/watch?v=7erJ1DV_Tlo)
