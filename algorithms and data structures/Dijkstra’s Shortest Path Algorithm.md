
## the algorithm

1. Let distance of start node to staret node = 0
2. Let all otehr distances from the start to be infinity
3. Repeat
	1. Visit the node with the smallest distance from the start node
	2. for the current node, get the unvisited neighbours
	3. for the current node, compute the distance each node from the start node
	4. if the computed distance is smaller update the shortest distance
	5. update the previous nodes, for the updated distrances
	6. add node to visited nodes
7. till all nodes visited 


[youtube](https://www.youtube.com/watch?v=pVfj6mxhdMw)

[implementation with priority queue](https://www.youtube.com/watch?v=pSqmAO-m7Lk)