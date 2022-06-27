the algorithm works for:

- undirected graphs
- weighted
- use min heap, for storing edges

1. select a vertex arbitrary and place them in a visited set
2. select as next vertex, 
	1.  the vertex that forms an edge with a minimum weight
	2. it is adjecent to the visited set
	3. it hasn't been visited
4. repeat the process until all edges are visited