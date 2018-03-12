# FP & OOP

# [Polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science))

In programming languages and type theory, **polymorphism**  is the provision of a single interface to entities of different types.



- [Ad hoc polymorphism](https://en.wikipedia.org/wiki/Ad_hoc_polymorphism) - is a kind of polymorphism in which polymorphic functions can be applied to arguments of different types, because a polymorphic function can denote a number of distinct and potentially heterogeneous implementations depending on the type of argument(s) to which it is applied. 
  - **Ad hoc polymorphism** and **parametric polymorphism** were originally described in Fundamental Concepts in Programming Languages, a set of lecture notes written in 1967.
  
-	[Parametric polymorphism](https://en.wikipedia.org/wiki/Parametric_polymorphism) - allows a function or a data type to be written generically, so that it can handle values uniformly without depending on their type

- [Subtyping](https://en.wikipedia.org/wiki/Subtyping) - allows a function to be written to take an object of a certain type **T**, but also work correctly, if passed an object that belongs to a type **S** that is a subtype of **T** (according to the Liskov substitution principle).
  - In a 1985 paper, Peter Wegner and Luca Cardelli introduced the term inclusion polymorphism to model **subtypes** and **inheritance**.
- ...

### Static and dynamic polymorphism

Polymorphism can be distinguished by when the implementation is selected: statically (at compile time) or dynamically (at run time, typically via a virtual function). This is known respectively as **static dispatch** and **dynamic dispatch**, and the corresponding forms of polymorphism are accordingly called **static polymorphism** and **dynamic polymorphism**.

- [Multiple dispatch or multimethods](https://en.wikipedia.org/wiki/Multiple_dispatch) -  is a feature of some programming languages in which a function or method can be dynamically dispatched based on the run-time (dynamic) type or, in the more general case some other attribute, of more than one of its arguments.
- [Double dispatch](https://en.wikipedia.org/wiki/Double_dispatch) - is a special form of multiple dispatch, and a mechanism that dispatches a function call to different concrete functions depending on the runtime types of two objects involved in the call. 

# [Encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)) 

In programming languages, encapsulation is used to refer to one of two related but distinct notions, and sometimes to the combination thereof:
- A language mechanism for **restricting direct access** to some of the object's components.
- A language construct that facilitates the **bundling of data** with the methods (or other functions) operating on that data.
