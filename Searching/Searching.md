# How searching works

Exploration of state space by expanding nodes in the frontier.

Each search expands the frontier of the nodes and number of frontiers for each node is the **branching** factor of the node. The higher the branching factor, the more likely the search time will be longer.

Each problem comes with

1. Graph to search goal node
2. Search strategy defined by search technique
3. Fringe to store frontier on expansion (can be stack, queue etc)

## Evaluation of search

- Completeness
  - does search always find a solution if there exist one?

- Time complexity
  - time needed to get solution

- Space complexity
  - memory space used
  
- Optimality
  - if solution obtained is always the least cost?
