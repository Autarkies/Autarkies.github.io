---
title: Results
---

# Results
nav: true
We have implemented the SAT tranlation into [DAut](https://github.com/arey0pushpa/dcnf-autarky), that finds the **A1**, **E1**, **A1 + E1** autarkies in the input (D)QBF. The `C++` implementaion is around 1800 lines of code. 
The software allows the user to choose an autarky system for the reduction and different *strictness levels* of the input file besides other parameters like choice of encoding `AMO constraints`. 
 
```
I. DQBF Track QBFEVAL'18:
   With improved SAT-encodings and running standard SAT-solvers, 
   we where able to compute the normalforms quite easily for all 334 instances 
   in the DQBF track of [QBFEVAL'18](http://www.qbflib.org/qbfeval18.php).
 
   There are exactly 4 instances with non-trivial A1-autarkies.
   Two of them are indeed A1-satisfiable.
```

A. ``A1-satisfiable instances``
  1. [bloem\_eq1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_eq1.dqdimacs)
  2. [tentrup17\_ltl2dba\_theta\_environment\_1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/tentrup17_ltl2dba_theta_environment_1.dqdimacs)
  
  
B. ``Non-Trivial A1-Autarkies``
  1. [bloem\_ex1.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_ex1.dqdimacs)
  2. [bloem\_ex2.dqdimacs](https://github.com/arey0pushpa/dcnf-autarky/blob/master/dcnf/examples/bloem_ex2.dqdimacs)

Evaluation: 

1. bloem\_eq1.dqdimacs 
  Input formula: 
    n(F) = 9
    c(F) = 16
    a(F) = 1         [1]
    e(F) = 8         [2-9]
  E1\_Autarky (F): Lean (No reduction)
  A1\_Autarky (F): Satisfiable 
    Autarky: 2 -> -1 
             3 -> true 
						 4 -> true 
						 5 -> false
						 6 -> false
						 7 -> true
						 8 -> true
						 9 -> true
  E1 + A1\_Autarky (F): Satisfiable 
     Autarky: Same as above
  Our Runtime: 0.011s 
  HQS took [SAT]: 1.2s

2. tentrup17\_ltl2dba\_theta\_environment\_1.dqdimacs 
  Input formula: 
    n(F) = 249
    c(F) = 732
    a(F) = 3      [1-3]
    e(F) = 246    [4-249] 
  E1\_Autarky (F): Lean (No reduction)
  A1\_Autarky (F): Non Trivial Autarky (Reduction but not SAT)
    Remaining evars count: 17
			4 200 203 206 209 212 215 218 221 224 227 230 233 236 239 242 245 
    Remaining clause count: 67 
      0	1	2	537	538	539	540	548	549	550	551	559	560	561	562	570	571	
      572	573	581	582	583	584	592	593	594	595	603	604	605	606	614	615	
      616	617	625	626	627	628	636	637	638	639	647	648	649	650	658	659	
      660	661	669	670	671	672	680	681	682	683	691	692	693	694	702	703	
      704	705	 
  E1 + A1\_Autarky (F): Satisfiable 
     Autarky:  .... BIG ..... Leaving! 
  Our Runtime: 0.418s 
  HQS solver took (SAT): 1.77s
  
Iprover and idq performed better than HQS on these instances but for FMCAD I guess
run time data is not relevant.

# Non-Trivial Autarky 

1. bloem_ex1.dqdimacs
  Input formula:
    n(F) = 23
    c(F) = 52 
    a(F) = 3          [1,3,4]
    e(F) = 20         [2,5-23]
  E1_Autarky (F): Lean (No reduction)
  A1_Autarky (F): Non Trivial Autarky (Reduction but not SAT)
    Remaining evars count: 6
      7 8 9 14 15 16 
    Remaining clause count: 18 
			0	1	2	3	4	5	6	7	8	21	22	23	24	25	26	27	28	29	
  	E1 + A1_Autarky (F): Non trivial Autarky 
     Autarky: Same as above
  	Our Runtime: 0.036s 
  	HQS took [SAT]: 0.19s
  
2. bloem_ex2.dqdimacs
  Input formula:
    n(F) = 60
    c(F) = 139 
    a(F) = 10          [1,3,5-12]
    e(F) = 50          [2,4,13-60]
  E1_Autarky (F): Lean (No reduction)
  A1_Autarky (F): Non Trivial Autarky (Reduction but not SAT)
    Remaining evars count: 33
			15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 34 35 
      36 37 38 39 40 41 42 43 44 45 46 47 48 54 55 56 
    Remaining clause count: 99 
			0	1	2	3	4	5	6	7	8	9	10	11	12	13	14	15	16	17	18	
      19	20	21	22	23	24	25	26	27	28	29	30	31	32	
      33	34	35	36	37	38	39	40	41	42	43	44	57	58	
      59	60	61	62	63	64	65	66	67	68	69	70	71	72	
      73	74	75	76	77	78	79	80	81	82	83	84	85	86	
      87	88	89	90	91	92	93	94	95	96	97	98	99	100	
      101	117	118	119	120	121	122	123	124	125	
  	E1 + A1_Autarky (F): Non trivial Autarky 
     Autarky: Same as above
  	Our Runtime: 0.201s 
  	HQS took [SAT]: 1.13s
   
<!--  
```
II. Planted examples for DQCNF:
    We have tested our code against the state of the art DQBF solver 
    [HQS] (https://projects.informatik.uni-freiburg.de/
                  attachments/1009/hqs_2018-08-30.zip).
```
 A. ``A1-satisfible`` 
  1. [planted_A1_50_50_200_40-3_40-4](./files/PlantedA1_DQCNF_50_50_200_40-3_40-4_2.dqdimacs), 0.52s
  2. [planted_A1_50_50_200_200-3_200-4](./files/PlantedA1_DQCNF_50_50_200_200-3_200-4_1.dqdimacs), 0.14s
  3. [Planted_A1_50_50_300_600-3_600-4](./files/PlantedA1_DQCNF_50_50_300_600-3_600-4_1.dqdimacs), 0.37s

 B. ``E1-satisfiable``
   - to be continued...
-->
