Doesn't throws an error if the key doesn't exists.
Instaed, insert the key and the value is inserted in the collection that we have defined in the constructor, for examle, bellow the value is inserted in a list

```python
from collections import defaultdict

a = defaultdict(list)
a["a"].append("b")
a["a"].append("c")

print(a)

{'a': ['b', 'c']}
```