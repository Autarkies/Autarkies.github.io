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
