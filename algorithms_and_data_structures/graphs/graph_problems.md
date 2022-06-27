- find if path exists, in bi-directional graph
	- can be solved with [[depth_first_search]] and [[breadth_first_search]]

- all paths from source to target (DAG, __D__ irected __A__ cyclic __G__ raph)
	- can be solved with [[depth_first_search]] and [[breadth_first_search]]

- find cycle in digraph (GRAY-BLACK!!)

- __shortest path__ in unweighted graph 
	- can be solved using [[breadth_first_search]]

- __single source shortest path__ (weighted, directed): find the shortest path from a given vertex to any other vertex

	[[dijkstra’s_shortest_path_algorithm]] Works only with positive weights

-  find the minumum total edge cost in a "weighted undirected graph"
	- [[prims_algorithm]]
	- [[kruskals_algorithm]]
	
- [[kahns_topological_sort]] works only for acyclic directed graphs
