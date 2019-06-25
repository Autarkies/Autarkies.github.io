## Autarkies
Autarkies for SAT are partial assignments for boolean CNF, which either satisfy a clause or leave it untouched.
 
## DQCNF 
A DQCNF is a 4-tuple (A, E, F, D), where
 - A is the set of universal variables,
 - E is the set of existential variables, with A &#8745; E = &empty;,
 - F is a clause-set over A &cup; E (i.e., var(F) &sube; A &cup; E),
  - D is the dependency-map with dom(D) = E, mapping v &isin; E  &rarr; D(v) &sube; A, the variables on which v depends.

## A- and E-systems

Consider a DQCNF F and k ≥ 0:
1. An A k -autarky for F is an autarky such that all boolean functions assigned
depend essentially on at most k variables.
2. An E k -autarky is an autarky assigns at most k (existential) variables.

We consider three basic Autarky systems:
A_0 and A_1 allow the boolean functions to essentially depend on 0 resp. 1 universal variable
while E_1 only uses one existential variable.

## A_1: Translations of the autarky-problem via compilation

Basic Idea: restrict to some "interesting” selection **s(v)** &sube; BF<sup> D<sup> v, the selected (boolean) functions, and treat the elements of s(v) as the possible values of v. For each C &isin; F , compile all possibilities for admissible partial satisfying
assignments for C into some CNF-representation **P(C)**, admissible partial assignment.

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
