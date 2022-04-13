# How searching works

Exploration of state space by expanding nodes in the frontier.

Search strategies defines how nodes are being explored. Different search strategies are evaluated in similar dimensions shown below.

- Completeness
  - does search always find a solution

- Time complexity
  - time needed to get solution

- Space complexity
  - memory space used
  
- Optimality
  - if solution obtained is always the least cost

Each search expands the frontier of the nodes and number of frontiers for each node is the **branching** factor of the node. The higher the branching factor, the more likely the search time will be longer.