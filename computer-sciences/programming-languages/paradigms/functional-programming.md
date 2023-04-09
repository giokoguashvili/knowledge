# Functional Programming

Main Concepts:

- Immutability <br/>
This refers to the concept that once an object or variable is created, it cannot be modified. This is a key concept in functional programming and allows for more predictable behavior

- First-Class Functions <br/>
This refers to the idea that functions are treated as first-class citizens in a programming language, meaning they can be assigned to variables, passed as arguments to other functions, and returned as values from functions

- Higher-Order Functions <br/>
These are functions that either take other functions as arguments or return functions as values. This is another key concept in functional programming

- Purity <br/>
A pure function is a function that has no side effects and always returns the same output for a given input. This makes the function predictable and easier to reason about.

- Side Effects <br/>
Side effects are any changes made to the outside world by a function, such as modifying a variable or sending data over a network. Side effects can make it harder to reason about a program and lead to bugs

- Recursion <br/>
This is the process of calling a function from within itself. Recursion is often used in functional programming to solve problems that can be broken down into smaller sub-problems.

- Tail Recurtion <br/>
Tail recursion is a specific type of recursion where the recursive call is the last operation performed in a function. In other words, the recursive call is in the tail position

- Lazy Evaluation <br/>
This is a technique where values are only computed when they are needed. This can save memory and improve performance in some cases

- Function Composition <br/>
This is the process of combining two or more functions into a new function that performs both operations in sequence

- Function Pipelines <br/>
This is a technique where a series of functions are composed into a pipeline, where the output of one function is used as the input of the next function

- Function Currying <br/>
This is the process of taking a function that takes multiple arguments and converting it into a series of functions that take one argument each. This can be useful for creating more reusable and composable functions

- Function Closure <br/>
This is a technique where a function can access variables from its outer scope even after the outer function has finished executing

- Pattern Matching <br/>
This is a technique for matching data structures against a pattern and extracting information from the data based on the pattern

- High-Order Polymorphism (Generics) <br/>
This is a technique for creating functions and data types that can work with a wide range of input types

- Dependent Types <br/>
These are types that depend on values, allowing for more precise type checking and verification

- Type Inference <br/>
This is a technique where a programming language can automatically deduce the types of variables and functions without requiring the programmer to explicitly specify them

- ADT - Algebraic Data Types <br/>
These are data types that can be composed of other data types using algebraic operations like sum and product

- Category Theory <br/>
This is a branch of mathematics that provides a framework for abstracting common concepts in programming, such as functions and composition
    - Monads <br/>
    Monads are a way of encapsulating effects in a functional programming language and sequencing computations in a predictable and composable way
    - Optics <br/>
    Optics is a set of abstractions for working with complex data structures, including lenses, prisms, traversals, and isomorphisms
        - Lenses
        - Prisms
        - Traversals
        - Isomorphisms