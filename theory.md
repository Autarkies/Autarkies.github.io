---
title: Theory
nav: true
---
<div class="page">
  <h1 class="page-title">Looking for an Autarky?</h1>
  <!--<span>Sorry, but the page you were trying to view does not exist.</span>-->
<pre><code>---------------------
 Autarkies for SAT are partial assignments for boolean CNF, 
 which either satisfy a clause or leave it untouched.
--------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||

</code></pre>
</div>


## DQCNF 
A `DQCNF` is a 4-tuple `(A, E, F, D)`, where
 - `A` is the set of `universal variables`,
 - `E` is the set of `existential variables`, with A &#8745; E = &empty;,
 - `F` is a `clause-set` over A &cup; E (i.e., var(F) &sube; A &cup; E),
  - `D` is the `dependency-map` with dom(D) = E, mapping v &isin; E  &rarr; D(v) &sube; A, the variables on which v depends.

## A- and E-systems
Consider a DQCNF F and k ≥ 0:
  1. An **Ak- autarky** for F is an autarky such that all boolean functions assigned depend essentially on at most k variables. 
  2. An **Ek- autarky** is an autarky assigns at most k (existential) variables.

```
  A0 and A1 allow the boolean functions to essentially 
  depend on 0 resp. 1 universal variable.

  E1 only uses one existential variable.
```
We have considered three Autarky Systems **A1**, **E1**, **A1 + E1**.
