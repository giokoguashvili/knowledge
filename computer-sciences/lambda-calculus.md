# [Lambda Calculus](https://en.wikipedia.org/wiki/Lambda_calculus)

Lambda calculus is a formal system in mathematical logic for expressing computation based on function abstraction and application 
using variable binding and substitution. 
It is a universal model of computation that can be used to simulate any [Turing machine](https://en.wikipedia.org/wiki/Turing_machine).
It was introduced by mathematician [Alonzo Church](https://en.wikipedia.org/wiki/Alonzo_Church) in the 1930s.

### Lambda terms

The lambda calculus consists of a language of **lambda terms**, which is defined by a certain formal syntax, 
and a set of transformation rules, which allow manipulation of the lambda terms.

Syntax |	Name	| Description
--- | --- | ---
x	| Variable	| A character or string representing a parameter or mathematical/logical value
(λx.M)	| Abstraction	| Function definition (M is a lambda term). The variable x becomes bound in the expression.
(M N) |	Application	| Applying a function to an argument. M and N are lambda terms.

Like programming languages, the syntax of λ-terms can be defined with [BNF](https://en.wikipedia.org/wiki/Backus%E2%80%93Naur_form) (Backus–Naur form):
```fsharp
Exp = Var | Const | Exp Exp | λ Var. Exp
```

Operation	| Name	| Description
--- | --- | ---
(λx.M[x])→(λy.M[y]) | α-conversion | Renaming the bound (formal) variables in the expression. Used to avoid name collisions.
((λx.M) E)→(M[x:=E]) | β-reduction	| Substituting the bound variable by the argument expression in the body of the abstraction

# [Curry–Howard correspondence](https://en.wikipedia.org/wiki/Curry%E2%80%93Howard_correspondence)

1. In 1934 Curry observes that the types of the combinators could be seen as axiom-schemes for intuitionistic implicational logic.
2. In 1958 he observes that a certain kind of proof system, referred to as Hilbert-style deduction systems, coincides on some fragment to the typed fragment of a standard model of computation known as combinatory logic.
3. In 1969 Howard observes that another, more "high-level" proof system, referred to as natural deduction, can be directly interpreted in its intuitionistic version as a typed variant of the model of computation known as lambda calculus.

Math side	| Programming side	
--- | --- 
Natural Deduction - Gentzen (1935) | Typed Lambda Calculus - Church (1940)
Type Schemes - Hindle (1969) | ML Type System - Milner (1975)
System F - Girard (1972) | Polymorphic Lambda Calculus - Reynolds (1974)
Modal Logic - Lewis (1910) | Monads(state, exceptions) - Kleisli (19650, Moggi (1987)
Classical_Intuitionistic Embedding - Godel (1933) | Continuation Passing Style CPS - Reynolds (1972)

```javascript
var Identity = x => x
var True = x => y = x
var False = x => y => y
var If = p => x => y => p(x)(y)
var Or = p => q => p(p)(q)
var And = p => q => p(q)(p)

var Zero = f => x => x
var One = f => x => f(x)
var Two = f => x => f(f(x))

If(True)(One)(Two)

If(Or(False)(False))(One)(Two)
If(Or(False)(True))(One)(Two)

var Pair = x => y => z => z(x)(y)
var First = p => p(True)
var Second = p => p(False)

First(Pair(One)(Two))
Second(Pair(One)(Two))
```

# Type Theory

Mathematical structure    
    In mathematics, a structure on a set is an additional mathematical object that, in some manner, attaches (or relates) to that set to endow it with some additional meaning or significance.

Type theory
    In mathematics, logic, and computer science, a type theory is any of a class of formal systems, some of which can serve as alternatives to set theory as a foundation for all mathematics. In type theory, every "term" has a "type" and operations are restricted to terms of a certain type.

Set theory studies any type of set, and group theory studies a specific type of set called a group, which is defined by group axioms. The elements of a group must conform and abide by the group axioms, whereas in set theory a set can be just a collection of unrelated elements not defined by any type of structure.

Category theory is a toolset for describing the general abstract structures in mathematics. Paradigm. As opposed to set theory, category theory focuses not on elements x , y , ⋯ x,y, \cdots – called objects – but on the relations between these objects: the (homo)morphisms between them.

Abstract Algebra
   In algebra, which is a broad division of mathematics, abstract algebra (occasionally called modern algebra) is the study of algebraic structures. Algebraic structures include groups, rings, fields, modules, vector spaces, lattices, and algebras. 

Algebric Types 
    In computer programming, especially functional programming and type theory, an algebraic data type is a kind of composite type, i.e., a type formed by combining other types.
    Two common classes of algebraic types are product types (i.e., tuples and records) and sum types (i.e., tagged or disjoint unions or variant types).

Set theory is a branch of mathematical logic that studies sets, which informally are collections of objects.

    Groups  - is a set equipped with a binary operation which combines any two elements to form a third element in such a way that four conditions called group axioms are satisfied, namely closure, associativity, identity and invertibility,  
    Fields - is a set on which addition (+), subtraction (-), multiplication (*) and division (/) are defined, and behave as the corresponding operations on rational and real numbers do,
    Rings - two binary operations that generalize the arithmetic operations of addition (+) and multiplication (*),
    ...,
    ...

Dependent Types
    In computer science and logic, a dependent type is a type whose definition depends on a value. A "pair of integers" is a type. A "pair of integers where the second is greater than the first" is a dependent type because of the dependence on the value. 

Math Logic, Proof theory, 

Systematic Type Theory
Martin Lof Type Theory
   Algebric data types
   Dependent types
Category Theory
   Functors, Monoids, Monads
Intuitionistic logic
   Propositons as types
Hindley-Millner type inference



