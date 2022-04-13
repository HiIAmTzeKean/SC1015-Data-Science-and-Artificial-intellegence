# Uninformed search

The search algo only uses information from the problem definition

## Breadth first search

Expand all nodes in the current level before expanding other nodes. Uses a FIFO queue to do search.  
Completeness: Yes, if solution exist, the solution can always be found  
Time complexity: b^d  
Space complexity: b^d, since each node must be kept in memory to return the solution  
Optimal: Yes if each step has equal cost  

## Uniform cost search

Similar to breadth search but considers the cost of each step and expands the nodes with the lowest cost.  
FIFO queue is swapped out for a Priority queue. Uses a cost function g(n) to evaluate priority  
Completeness: Yes, if solution exist, the solution can always be found  
Time complexity: # nodes with g(n) <= cost of optimal solution (number of nodes dequeued)  
Space complexity: # nodes with g(n) <= cost of optimal solution  
Optimal: Yes

## Depth first search

