```python

import re

s_nums = 'one1two22three333four'

print(re.split('\d+', s_nums))
# ['one', 'two', 'three', 'four']

```