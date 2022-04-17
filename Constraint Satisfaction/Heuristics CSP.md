# Heuristics for CSP

We can take into account of

- Which variable to assign next (Most constrained variable/ Minimum remaining values heuristic)
- Order of value to assign to each variable (Least constraining value)
- Implications of current variable assignments for future assignments (constraint propagation)
- Changing assignments that have violated constraints to minimise the number of conflict (Min-conflicts heuristic)

## Constraint propagation

![Constraint propagation](constraint%20propagation.gif)

Here we see how future moves can be affected by the current variables that are assigned.  
This heuristic can also be applied to other algorithm's such as map colouring etc.

## Most constraint variable

Minimum remaining values.  
To assign variables that is involved in the largest number of constraints on unassigned variables (AKA variable with the least legal values). Idea behind is to reduce branching factor on future choices.

## Least constraining value

Assigning variables with values that leaves for maximum flexibility for future assignments

## Min-Conflict heuristic

For some given initial assignment, we select a variable with in the scope of violated constraint and assign it a value that violates least number of constraint.

![min conflict](min%20conflict.png)

Here we see that the queen on the last column can be shifted such that it is placed in a position with the least violation of conflicts.

___

References:

- <https://slidetodoc.com/presentation_image_h/a0ba4815e2d7c0551b8571331de22fa0/image-14.jpg>
