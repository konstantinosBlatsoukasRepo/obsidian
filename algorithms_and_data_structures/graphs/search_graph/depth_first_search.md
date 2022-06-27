stack: lifo (return to previous state)


you can implement dfs or through :

1. a stack 
2. or a recursive calls


time complexity: O(V + E)
space complexity: O(V)


example:

```python
graph = {
    '5': ['3', '7'],
    '3': ['2', '4'],
    '7': ['8'],
    '2': [],
    '4': ['8'],
    '8': []
}

seen = set()
stack = ['5']

while stack:
    node_id = stack.pop()
    print(node_id)
    if node_id not in seen:
        seen.add(node_id)
        childs = graph[node_id]
        for child in childs:
            if child not in seen:
                stack.append(child)
```