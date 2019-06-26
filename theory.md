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

### A- and E-systems
Consider a DQCNF F and k ≥ 0:
  1. An Ak -autarky for F is an autarky such that all boolean functions assigned depend essentially on at most k variables. 
  2. An Ek -autarky is an autarky assigns at most k (existential) variables.

  - A0 and A1 allow the boolean functions to essentially depend on 0 resp. 1 universal variable.

  - E1 only uses one existential variable.

We have considered three Autarky Systems A1, E1, A1 + E1.
