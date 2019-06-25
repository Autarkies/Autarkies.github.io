## Autarkies for SAT

Autarkies for SAT are partial assignments for boolean CNF, which either satisfy a clause or leave it untouched.

### A- and E-systems

Consider a DQCNF F and k ≥ 0:
1. An A k -autarky for F is an autarky such that all boolean functions assigned
depend essentially on at most k variables.
2. An E k -autarky is an autarky assigns at most k (existential) variables.

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
