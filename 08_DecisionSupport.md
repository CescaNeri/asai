## Constraint Programming

**Decision support system** is a framework supporting the decision-making activities of people and organizations.
It focuses on facilitating decision-making rather than fully automating it.

AI-based optimization can improve decision support in many areas:

* Planning and factory assembly
* Resource allocation
* Budgeting

 Such systems can handles combination of choices to take optimal decisions. However, the overall number of possible combinations can be huge, leading to excessive computational time.

 ```python
 S = {7, 10, 23, 13, 4, 16}

 N = 4, K > 50 -> yes
 N = 3, K > 50 -> no
 ```

These is a decision problem which is easy to solve for a machine (ordinamento).

 ```python
 S = {7, 10, 23, 13, 4, 16}

 N = 4, K = 50 -> yes
 N = 3, K = 50 -> no
 ```

 This decision problem is very difficult  for a machine as we cannot find the solution in a reasonable time.

 `P-NP` dilemma is a major open problem in computer science and solving this issue would be devastating, breaking down cryptosystems (HTTPS would not be secure anymore) but optimization would become easy.

 ### Knapsack Problem

 Given a set of items, each with a weight and a value, determine the number of each item to put in a knapsack so that the total weight does not exceed a given limit and the total value is maximal.

*How can we use AI to take optimal decisions?*

The first step is identifying the problem components and their interaction:

* Variables (model the decisions)
* Domains (model the choices)
* Constraints (define the requirements)
* Objective (Something to maximize or minimize)
* Parameters (Input values)