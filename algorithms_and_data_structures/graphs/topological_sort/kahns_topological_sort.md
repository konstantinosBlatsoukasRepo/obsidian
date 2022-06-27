- works only for acyclic directed graphs

In-degree: total incoming edges to the vertex
Out-degree: total outgoing edges from the vertex


1. caclulate all In-degrees for each vertex
2. if a vertex with in_degree equal to zero, added to the queue
3. iterate over all vertexes that are in the queue
	- add to the queue the vertex with in-degree zero
	- add the vertex with zero in-degree in the queue
	- remove one in-degree rank from the adjecatn vertexes
4. return the solution (e.g. the array with the vertexes) 