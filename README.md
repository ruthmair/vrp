# Vehicle Routing Problems

## Objective and Prerequisites

Vehicle routing problems (VRPs) are combinatorial optimization problems that arise in the area of logistics [1].
In most variants, a set of customers needs to be visited and served (delivering or picking some goods) by a given fleet of vehicles. We want to find
* a visiting sequence of customers for each vehicle
* with minimal total routing costs, such that
* each customer is visited exactly once,
* the vehicle capacity is never exceeded,
* and potentially other constraints are satisfied, e.g., time windows at the customers.

These notebooks demonstrate several ways to model vehicle routing problems as mixed-integer linear programs (MILP), 
without use of sophisticated column generation or cutting plane methods as needed in state-of-the-art approaches [2,3].
Therefore, the presented models have limited performance compared to the state-of-the-art, independent of the used solver. 
The formulations presented here should be a starting point to understand the modeling difficulties related to VRPs and to evaluate the performance for your problem instances.
Currently, only the Capacitated Vehicle Routing Problem (CVRP) and the Vehicle Routing Problem with Time Windows (VRPTW) are considered but the mentioned modeling techniques might also be used for additional variants and side constraints.

These modeling examples are at an intermediate level, where we assume that you know Python and that you have some knowledge of how to build mathematical optimization models.

[1] Toth, P., & Vigo, D. (Eds.). (2014). Vehicle routing: problems, methods, and applications. Society for industrial and applied mathematics.

[2] Baldacci, R., Bartolini, E., Mingozzi, A., & Roberti, R. (2010). An exact solution framework for a broad class of vehicle routing problems. Computational Management Science, 7(3), 229.

[3] Pessoa, A., Sadykov, R., Uchoa, E., & Vanderbeck, F. (2020). A generic exact solver for vehicle routing and related problems. Mathematical Programming, 183, 483-523.

## Gurobi License

In order to run this Jupyter Notebook properly, you must have a Gurobi license. If you do not have one, you can request an 
[evaluation license](https://www.gurobi.com/downloads/request-an-evaluation-license/) 
as a *commercial user*, or a 
[free license](https://www.gurobi.com/academia/academic-program-and-licenses/) as an *academic user*.

Copyright © 2023 Gurobi Optimization, LLC