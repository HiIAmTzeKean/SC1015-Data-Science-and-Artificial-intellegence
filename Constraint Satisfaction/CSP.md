# CSP

Requires the following to be defined:

1. State
    - variables that are to be filled with values from domain

2. Goal test
    - set of constraints that allow combination of values for variables
    - constraints can be defined explicitly or implicitly via function

3. Actions

4. Initial state

## Types of constraints

Unary: Where there is restriction of possible assignment value

Binary: Restriction of relationship between two variables

Global: Relationship between arbitrary number of variables

## Types of domains

Discrete finite: Set of some numbers

Discrete infinite: Set of all integers

Continuous: Real numbers from 0 to 1

## Types of assignments

Consistent/ legal: An assignment that does not violate any constraint

Complete: Every variable has a value assigned to it

Partial: Some, not all variables has a value assigned to it

## Solving CSP

### Backtracking

Use of **backtracking** to solve CSP. (uniformed approach)  
Before generating new successors, check constraint violation. If there is a violation, backtrack to test another assignment

![n queen backtracking](backtrack.gif)

Remove redundancy of expanding frontiers that have already violated constraints. But this is still a brute-force approach, and for huge number of n, the time complexity is still O(n^2).

References:

- <https://ktiml.mff.cuni.cz/~bartak/constraints/propagation.html>
