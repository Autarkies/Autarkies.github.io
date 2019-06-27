---
title: Results
nav: true
---

# Results
We have implemented the SAT tranlation into [DAut](https://github.com/arey0pushpa/dcnf-autarky), that finds the **A1**, **E1**, **A1 + E1** autarkies in the input (D)QBF. The `C++` implementaion is around 1800 lines of code. 
The software allows the user to choose an autarky system for the reduction and different *strictness levels* of the input file besides other parameters like choice of encoding `AMO constraints`. 
 
```
I. DQBF Track QBFEVAL:
   With improved SAT-encodings and running standard SAT-solvers, 
   we where able to compute the normalforms quite easily for all 334 instances 
   in the DQBF track of [QBFEVAL'18](http://www.qbflib.org/qbfeval18.php).
 
  We found 4 instances that have Autarkies.
```

A. ``SAT instances``
  1. [bloem\_eq1.dqdimacs](./files/bloem_eq1.dqdimacs), 0.011s
  2. [tentrup17\_ltl2dba\_theta\_environment\_1.dqdimacs](./files/tentrup17_ltl2dba_theta_environment_1.dqdimacs), 0.239s
  
  
B. ``Non-Trivial Autarkies``
  1. [bloem\_ex1.dqdimacs](./files/bloem_ex1.dqdimacs), 0.031s
  2. [bloem\_ex2.dqdimacs](./files/bloem_ex2.dqdimacs), 0.143s
  
```
II. Planted examples for DQCNF:
    We have tested our code against the state of the art DQBF solver 
    [HQS] (https://projects.informatik.uni-freiburg.de/
                  attachments/1009/hqs_2018-08-30.zip).
```
 A. ``A1-satisfible`` 
    <a href="./images/bloem_ex1.dqdimacs">cv</a>
  1. [planted_A1_50_50_200_40-3_40-4](./files/PlantedA1_DQCNF_50_50_200_40-3_40-4_2.dqdimacs), 0.52s
  2. [planted_A1_50_50_200_200-3_200-4](./files/PlantedA1_DQCNF_50_50_200_200-3_200-4_1.dqdimacs), 0.14s
  3. [Planted_A1_50_50_300_600-3_600-4](./files/PlantedA1_DQCNF_50_50_300_600-3_600-4_1.dqdimacs), 0.37s

 B. ``E1-satisfiable``
   - to be continued...

