# Informed search

Uninformed search inefficient due to the exponential time complexity and space used. Informed search uses problem specific knowledge to choose which nodes to first expand. This is done through an evaluation function that estimate desirability of node.

## Evaluation function

Path-cost function g(n) used by UCS takes into cost to move to a certain node, but does not indicate cost towards goal.  
Heuristic function h(n) used to estimate the cost from goal to node. (Note h(n) is admissible if the function never over-estimates)

## Best first searching

Use the notion of choosing the best node to expand such that the search is always moving towards the goal

### Greedy search

Expand node that is the estimated to be closest to the goal. Strategy is to expand all frontiers and evaluate based on heuristic function (BFS idea), store the results into priority queue. Always pick closest node based on the heuristics.  
Complete: No, there could be loops causing it to be like a DFS  
Time: b^d, DFS approach  
Space: b^d, BFS approach to storing nodes  
Optimal: No  

![Greedy](Greedy%20Search.jpg)

### A* Search

Uses UCS idea with greedy search. 
Takes g(n) cost function from UCS and h(n) from greedy search. Such that f(n)=g(n)+h(h), using the whole life of the path to estimate desirability.  
g(n) is the backward cost (cumulative cost from start node)  
h(n) is forward cost (estimate cost from current node to goal)  
___
Note  
The worse case performance of A* is when the heuristic performance returns 0 all the time, causing it to function like UCS  
___

Complete: Yes  
Time: b^d  
Space: b^d  
Optimal: Yes  

![astar](A%20Star.jpg)

References:

- <https://en.wikipedia.org/wiki/A*_search_algorithm#Bounded_relaxation>
