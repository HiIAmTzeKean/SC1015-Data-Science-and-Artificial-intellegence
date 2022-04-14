# Uninformed search

The search algo only uses information from the problem definition

## Breadth first search

Expand all nodes in the current level before expanding other nodes. Uses a **FIFO** queue to do search.  
Completeness: Yes, if solution exist, the solution can always be found  
Time complexity: b^d  
Space complexity: b^d, since each node must be kept in memory to return the solution  
Optimal: Yes if each step has equal cost  

## Uniform cost search

Similar to breadth search but considers the cost of each step and expands the nodes with the lowest cost.  
FIFO queue is swapped out for a **Priority** queue. Uses a cost function g(n) to evaluate priority  
Completeness: Yes, if solution exist, the solution can always be found  
Time complexity: # nodes with g(n) <= cost of optimal solution (number of nodes dequeued)  
Space complexity: # nodes with g(n) <= cost of optimal solution  
Optimal: Yes

## Depth first search

Expands the nodes by seeking based on depth. Uses a **LIFO** stack and backtracks when no solution is obtained.
Completeness: if there are loops then solution may not be found, but can be solved with repeated state checking. if space is finite without loops, then solution can be found.  
Time complexity: b^d  
Space complexity: b*d, algo must store all possible nodes for backtrack, then if branching factor is 3 and algo always takes the left path, then for each level travelled down, the algo must store 2 additional nodes for backtracking  
Optimal: No

## Depth limited search

Similar to DFS, but applies a cut-off limit  
Completeness: if cut-off>=d  
Time complexity: b^d  
Space complexity: b*d  
Optimal: No

## Depth limited search

Similar to DFS, but increases the depth search incrementally. Similar concept to BFS on level checking, but algo looks deep on a selected level basis.  
Completeness: Yes, since solution can be found for some depth  
Time complexity: b^d  
Space complexity: b*d  
Optimal: Yes, since solution only encountered when d=solution depth
