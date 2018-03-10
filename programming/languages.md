# [Histrory of Languages](https://en.wikipedia.org/wiki/History_of_programming_languages)
Some notable languages that were developed in this period include:
- [Comparison of programming languages](https://ru.wikipedia.org/wiki/%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5_%D1%8F%D0%B7%D1%8B%D0%BA%D0%BE%D0%B2_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F)

### First programming languages
In the 1940s, the first recognizably modern electrically powered computers were created. The limited speed and memory capacity forced programmers to write hand tuned assembly language programs. It was eventually realized that programming in assembly language required a great deal of intellectual effort.

  - **1951 – Regional Assembly Language.**
  - 1952 – Autocode.
  - 1954 – IPL (forerunner to LISP)
  - 1955 – FLOW-MATIC (led to COBOL)
  - **1957 – FORTRAN (First compiler)**
  - 1957 – COMTRAN (precursor to COBOL)
  - **1958 – LISP.**
  - **1958 – ALGOL 58.**
  - **1959 – COBOL**           
  - 1959 – RPG
  - 1962 – APL
  - **1962 – Simula**
    invented in the late 1960s by Nygaard and Dahl as a superset of Algol 60, was the first language designed to support object-oriented programming.
  - 1962 – SNOBOL
  - 1963 – CPL (forerunner to C)
  - 1964 – Speakeasy (computational environment)
  - 1964 – BASIC
  - 1964 – PL/I
  - 1966 – JOSS
  - 1967 – BCPL (forerunner to C)
  
### Establishing fundamental paradigms  
The period from the late 1960s to the late 1970s brought a major flowering of programming languages. Most of the major language paradigms now in use were invented in this period:

- 1968 – Logo
- 1969 – B (forerunner to C)
- **1970 – Pascal**
- 1970 – Forth
- **1972 – C**
- **1972 – Smalltalk**
- **1972 – Prolog**
- **1973 – ML**
- **1975 – Scheme**
- **1978 – SQL** (a query language, later extended)

### 1980s: consolidation, modules, performance
- **1980 – C++** (as C with classes, renamed in 1983)
- 1983 – Ada
- **1984 – Common Lisp**
- 1984 – MATLAB
- 1984 - dBase III, dBase III Plus
- 1985 – Eiffel
- **1986 – Objective-C**         
- 1986 – LabVIEW (Visual Programming Language)
- **1986 – Erlang**
- 1987 – Perl
- 1988 – Tcl
- 1988 – Wolfram Language (as part of Mathematica, only got a separate name in June 2013)
- 1989 – FL (Backus)   

### 1990s: the Internet age
- **1990 – Haskell**
- **1991 – Python**
- **1991 – Visual Basic**
- 1993 – Lua
- **1993 – R**
- 1994 – CLOS (part of ANSI Common Lisp)
- **1995 – Ruby**
- 1995 – Ada 95                                                    
- **1995 – Java**
- **1995 – Delphi (Object Pascal)**
- **1995 – JavaScript**
- **1995 – PHP**
- 1997 – Rebol

### Current trends
Programming language evolution continues, in both industry and research. Some of the recent trends have included:

- **2000 – ActionScript**
- **2001 – C#**
- 2001 – D
- 2002 – Scratch
- **2003 – Groovy**
- **2003 – Scala**
- **2005 – F#**
- **2006 – PowerShell**
- **2007 – Clojure**
- **2009 – Go**
- **2010 – Rust**
- **2011 – Dart**
- **2011 – Kotlin**
- 2011 – Red
- **2011 - Elixir**
- 2012 – Julia
- **2014 – Swift**
- 2016 – Ring


# [Programming Paradigms](https://en.wikipedia.org/wiki/Programming_paradigm)

A programming paradigm is a complex of concepts, principles and abstractions which define a fundamental style of programming.
Note that it is not necessary for a language to use one and only one paradigm. Languages which are designed to support several paradigms are called multi-paradigm.

- Array
- Concatenative
- Concurrent
- **[Declarative](https://en.wikipedia.org/wiki/Declarative_programming)**
- Esoteric
- Function-level
- **[Functional](https://en.wikipedia.org/wiki/Functional_programming)**
- **Generic**
- **[Imperative](https://en.wikipedia.org/wiki/Imperative_programming)**
- [Logic](https://en.wikipedia.org/wiki/Logic_programming)
- **Message passing**
- Metaprogramming
- Non-strict
- **[Object-oriented](https://en.wikipedia.org/wiki/Object-oriented_programming)**
- **[Procedural](https://en.wikipedia.org/wiki/Procedural_programming)**
- Prototype-based
- **Reflective**
- Scalar
- Stack-oriented
- Strict
- **[Structured](https://en.wikipedia.org/wiki/Structured_programming)**
- Tabular
- Tacit
- Value-level
- Visual

## [Type System](https://en.wikipedia.org/wiki/Type_system)

- https://habrahabr.ru/post/161205/

- Typed
  - Static
    - Strong
      - Implicit
      - Explicit
    - Weakly
      - Implicit
      - Explicit
  - Dynamic
    - Strong
      - Implicit
      - Explicit
    - Weakly
      - Implicit
      - Explicit
- Untyped
  - Assembler
  - Forth
  - Brainfuck



# [Polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)#Row_polymorphism)

- [Ad hoc polymorphism](https://en.wikipedia.org/wiki/Ad_hoc_polymorphism) - is a kind of polymorphism in which polymorphic functions can be applied to arguments of different types, because a polymorphic function can denote a number of distinct and potentially heterogeneous implementations depending on the type of argument(s) to which it is applied. 

-	Parametric polymorphism - allows a function or a data type to be written generically, so that it can handle values uniformly without depending on their type

- Subtyping - allows a function to be written to take an object of a certain type **T**, but also work correctly, if passed an object that belongs to a type **S** that is a subtype of **T** (according to the Liskov substitution principle).
- ...

### Static and dynamic polymorphism

Polymorphism can be distinguished by when the implementation is selected: statically (at compile time) or dynamically (at run time, typically via a virtual function). This is known respectively as static dispatch and dynamic dispatch, and the corresponding forms of polymorphism are accordingly called static polymorphism and dynamic polymorphism.

# [History of ML](https://courses.cs.washington.edu/courses/cse341/04wi/lectures/02-ml-intro.html)
ML is clean and powerful, and has many traits that language designers consider hallmarks of a good high-level language
![02-ml-history](https://user-images.githubusercontent.com/8178412/36527608-ce78c5e4-17cb-11e8-9866-15fee4c5466e.png)

# FAQ
- http://progopedia.ru/

# Diagrams

### Computer Language Family Tree
![computerlanguageschart](https://user-images.githubusercontent.com/8178412/36428425-4922e43c-1669-11e8-8023-50ef0d0a74b7.png)

### Paradigms
![paradigmsdiagrameng108](https://user-images.githubusercontent.com/8178412/36428741-2ced3064-166a-11e8-8c33-a3ec14a73770.jpg)
