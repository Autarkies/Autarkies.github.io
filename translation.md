---
title: Translation
nav: true
---

# Translation to SAT:

## Finding A1 via compilation:

   1. `Selected (boolean) functions`: restrict to some "interesting” selection **s(v)** ⊆ BF<sup> D<sup> v</sup> </sup>, and treat the elements of s(v) as the possible values of v.
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

