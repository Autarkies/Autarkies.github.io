---
title: Translation
nav: true
---

Autarkies for SAT are partial assignments for boolean CNF, which either satisfy a clause or leave it untouched.

### A- and E-systems
Consider a DQCNF F and k ≥ 0:
  1. An Ak -autarky for F is an autarky such that all boolean functions assigned depend essentially on at most k variables. 
  2. An Ek -autarky is an autarky assigns at most k (existential) variables.

  - A0 and A1 allow the boolean functions to essentially depend on 0 resp. 1 universal variable.

  - E1 only uses one existential variable.

We have considered three Autarky Systems A1, E1, A1 + E1.

### Translation of finding A1 via compilation:

   1. `Selected (boolean) functions`: restrict to some "interesting” selection **s(v)** ⊆ BF D v , and treat the elements of s(v) as the possible values of v.
   2. `Admissible partial assignment`: For each C ∈ F , compile all possibilities for admissible partial satisfying assignments for C into some CNF-representation **P(C)**.

{% highlight ruby %}
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
{% endhighlight %}

