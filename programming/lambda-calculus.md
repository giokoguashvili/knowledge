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

Operation	| Name	| Description
--- | --- | ---
(λx.M[x])→(λy.M[y]) | α-conversion | Renaming the bound (formal) variables in the expression. Used to avoid name collisions.
((λx.M) E)→(M[x:=E]) | β-reduction	| Substituting the bound variable by the argument expression in the body of the abstraction

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
