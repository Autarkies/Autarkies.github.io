## Autarkies
Autarkies for SAT are partial assignments for boolean CNF, which either satisfy a clause or leave it untouched.

## A- and E-systems

Consider a DQCNF F and k ≥ 0:
1. An A<sub>k</sub> -autarky for F is an autarky such that all boolean functions assigned
depend essentially on at most k variables.
2. An E<sub>k</sub> -autarky is an autarky assigns at most k (existential) variables.

We consider three basic Autarky systems:
A<sub>0</sub> and A<sub>1</sub> allow the boolean functions to essentially depend on 0 resp. 1 universal variable
while E<sub>1</sub> only uses one existential variable.

##  A<sub>1</sub>: Translations of the autarky-problem via compilation

Basic Idea: 
 -  Selected (boolean) functions: restrict to some "interesting” selection **s(v)** &sube; BF<sup> D<sup> v</sup> </sup>, and treat the elements of s(v) as the possible values of v. 
 - Admissible partial assignment: For each C &isin; F , compile all possibilities for admissible partial satisfying
assignments for C into some CNF-representation **P(C)**.

The complete translation

1. The translation t chooses for each v &isin; E and f &isin; 
s(v) a distinct new bf-variable t(v,f) &isin; VA

&#8743; t(v, f) &#8744; t(v,f').

2. In order to make each P(C) a clause, we choose distinct
   new pa-variables t(φ) &isin; VA, for φ &isin; C∈F S(C) ("true" iff φ is activated). 
   
 t(φ) &#8660;  &#8743; t(v, φ(v))

3. We choose furthermore distinct new clause-selector-variables t(C) &isin; VA

which yields for each C &isin; F the clauses

t(C) &#8744; &#8744; t(φ)  (4.3)
    φ∈S(C)

&#8743; &#8743; t(C) &#8744; t(v,f) (4.4)

4. The existence of a non-trivial autarky is now expressed either via the clause

  &#8744; t(C)


```markdown
Consider the DQCNF 
F := ({3,4}, {1,2})

A DQDIMACS code is:
p cnf 4 2
a 3 4 0
e 2 0
d 1 3 0
-1 2 0
2 -3 -4 0


[Link](url) and ![Image](src)
```

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
