# CSP

Requires the following to be defined:

1. State
    - variables that are to be filled with values from domain

2. Goal test
    - set of constraints that allow combination of values for variables

3. Actions

4. Initial state

## Types of constraints

Unary: Where there is restriction of possible assignment value

Binary: Restriction of relationship between two variables

Global: Relationship between aribitray number of variables

## Types of domains

Discrete finite: Set of some numbers

Discrete infinite: Set of all integers

Continuous: Real number from 0 to 1

## Types of assignments

Consistent/ legal: An assignment that does not violate any constraint

Complete: Every variable has a value assigned to it

Partial: Some, not all variables has a value assigned to it

## Solving CSP

### Backtracking

Use of **backtracking** to solve CSP. (uniformed approach)  
Before generating new successors, check constraint violation. If there is a violation, backtrack to test another assignment

![n queen backtracking](backtrack.gif)

Remove redundancy of expanding frontiers that have already violated constraints. But this is still a brute-froce approach, and for huge number of n, the time complexity is still O(n^2).

### Heuristics for CSP

We can take into account of

- Which variable to assign next (Most contrainted variable/ Minimum remaining values heuristic)
- Order of value to assign to each variable (Least contraining value)
- Implications of current variable assignments for future assignments (constraint propagation)
- Changing assignments that have violated constraints to minimise the number of conflict (Min-conflicts heuristic)


References:
- https://ktiml.mff.cuni.cz/~bartak/constraints/propagation.html
