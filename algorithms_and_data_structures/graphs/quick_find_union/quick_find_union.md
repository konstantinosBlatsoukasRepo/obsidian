Quick Find

```python

class QuickFind:

	def __init__(self, size):
		self.root = [i for i in range(size)]

	def find(self, i):
		return self.root[i]

	def union(self, x, y):
		root_x = root[x]
		root_y = root[y]
		if root_x != root_y
			for i in range(len(self.root)):
				if self.root[i] == root_y:
					root[i] = root_x

```


the union operation takes O(n), always


Quick Union

```python

class QuickUnion:

	def __init__(self, size):
		self.root = [i for i in range(size)]
		

	def find(self, i):
		if self.root[i] == i:
			return i
		return self.find(root[i])

	def union(self, x, y):
		root_x = self.find(x)
		root_y = self.find(y)
		if root_x != root_y:
			self.root[root_y] = root_x


```


extra optimizations on QuickUnion:

- Union by rank
- path compresion, on find operation