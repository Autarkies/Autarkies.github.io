---
title: Results
nav: true
---

# Results
We have implemented the SAT tranlation into [DAut](https://github.com/arey0pushpa/dcnf-autarky), that finds the **A1**, **E1**, **A1 + E1** autarkies in the input (D)QBF. The `C++` implementaion is around 1800 lines of code. 
The software allows the user to choose an autarky system for the reduction and different strictness levels of the input file besides other parameters like choice of encoding `AMO constarints`. 
 
With improved SAT-encodings and running standard SAT-solvers, we where able to compute the normalforms quite easily for all over 334 instances in the DQBF track of [QBFEVAL'18](http://www.qbflib.org/qbfeval18.php)
.

We found 4 instances that have Autarkies:

1. SAT instances 
  - bloem\_eq1.dqdimacs, 0.011s
  - tentrup17\_ltl2dba\_theta\_environment\_1.dqdimacs, 0.239s
  
  
2. Non-Trivial Autarkies
  - bloem\_ex1.dqdimacs, 0.031s
  - bloem\_ex2.dqdimacs, 0.143s
  
