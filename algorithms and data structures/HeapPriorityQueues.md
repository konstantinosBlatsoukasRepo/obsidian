Heaps are coming in two flavors min heap and max heap

A heap is a bunary tree which the the parent node has always smaller value than the
childs.

```
                                       
              +--2----+                
              |       |                
              |       |                
              |       |                
             4      +-8--+             
       +-----|      |    |             
       |     |      |    |             
    +--9-+   7-+   10    9             
    |    |     |                       
   15   20     13
```

You can implemented with:

1. array
	1. parent index = (index -2) / 2)
	2. left child index = index*2  + 1
	3. right child index = index*2  + 2
2. tree (with pointers)


It can be applied to:
[[Dijkstra’s Shortest Path Algorithm]]