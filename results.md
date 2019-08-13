---
title: Results
---

# Results
We have implemented the SAT tranlation into [DAut](https://github.com/arey0pushpa/dcnf-autarky), that finds the **A1**, **E1**, **A1 + E1** autarkies in the input (D)QBF. The `C++` implementaion is around 1800 lines of code. 
The software allows the user to choose an autarky system for the reduction and different *strictness levels* of the input file besides other parameters like choice of encoding `AMO constraints`. 
 
```
I. DQBF Track QBFEVAL'18:
   With improved SAT-encodings and running standard SAT-solvers, 
   we where able to compute the normalforms for all 334 instances 
   in the DQBF track of [QBFEVAL'18](http://www.qbflib.org/qbfeval18.php).
   All normalforms have been computed within a total time of 9000s. 
   (We remark that finding an autarky is quick, and most of the 
   time is spent on proving unsatisfiability.) 
   
   There are exactly 4 instances with non-trivial A1-autarkies.
   330 instances are E1+A1-lean (have no non-trivial E1- or A1-autarky). 

   From the remaining 4 instances, all are E1-lean, one is A1-satisfiable,
   one is E1+A1-satisfiable, and the remaining two instances are not E1+A1-satisfiable, 
   but allow A1-autarkies eliminating in both cases around 80% of variables 
   and clauses (while adding E1 does not change this). 

   Two of them are indeed A1-satisfiable.
```

A. ``A1-satisfiable instances``

  1. [bloem\_eq1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_eq1.dqdimacs) 
```
     Input formula:   
    	n(F) = 9    
    	c(F) = 16     
    	a(F) = 1        
    	e(F) = 8         
     E1_Autarky (F): Lean (No reduction)  
     A1_Autarky (F): Satisfiable   
     	Autarky: (2 -> -1, 3 -> true, 4 -> true, 5 -> false,   
                  6 -> false, 7 -> true, 8 -> true, 9 -> true)   
     
     E1 + A1_Autarky (F): Satisfiable  
     	Autarky: Same as above   
```
  2. [tentrup17\_ltl2dba\_theta\_environment\_1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/tentrup17_ltl2dba_theta_environment_1.dqdimacs)
```
     Input formula:  
    	n(F) = 249  
    	c(F) = 732  
    	a(F) = 3     
    	e(F) = 246     
    E1_Autarky (F): Lean (No reduction)  
    A1_Autarky (F): Non Trivial Autarky (Reduction but not SAT)  
    	Remaining evars count: 17  
    	Remaining clause count: 67  
    E1 + A1_Autarky (F): Satisfiable   
    	Autarky:  .... BIG ..... Leaving!   
```
  
B. ``Non-Trivial A1-Autarkies``
  1. [bloem\_ex1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_ex1.dqdimacs)  
```
     Input formula:  
    	n(F) = 23  
    	c(F) = 52  
    	a(F) = 3          
    	e(F) = 20         
     E1_Autarky (F): Lean (No reduction)  
     A1_Autarky (F): Non Trivial Autarky (Reduction but not SAT)  
    	Remaining evars count: 6  
    	Remaining clause count: 18  
     E1 + A1_Autarky (F): Non trivial Autarky   
      	Autarky: Same as above  
```
  
  2. [bloem\_ex2.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_ex2.dqdimacs)
```     
     Input formula:  
   	 n(F) = 60  
   	 c(F) = 139   
    	 a(F) = 10         
    	 e(F) = 50          
     E1_Autarky (F): Lean (No reduction)  
     A1_Autarky (F): Non Trivial Autarky (Reduction but not SAT)  
    	Remaining evars count: 33  
    	Remaining clause count: 99   
     E1 + A1_Autarky (F): Non trivial Autarky   
       Autarky: Same as above  
```
