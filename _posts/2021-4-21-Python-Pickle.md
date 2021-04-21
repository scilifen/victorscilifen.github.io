---
layout: posts

alt_title: "Python Pickle"

# optional sub-title below the page title
sub_title: "Life is short, I learn Python"

# optional intro text below titles, Markdown allowed
introduction: |
    一种储存python数据的好办法，实现python的数据结构简化，把字典，列表更好的整理。

categories: Articles
tags: 
    - Python
    - Pickle
---
## Pickle是一种储存python数据的好办法，实现python的数据结构简化，把字典，列表更好的整理。
```python
import pickle

pickle_file = open('pick_file', 'wb')
dict1 = {'1': 'hello', '2': 'goodbye'}
pickle.dump(dict1, pickle_file)

pickle_restore = open('pickle_restore', 'rb')
dict2 = pickle.load(pickle_restore)

```

这就是pickle的基本用法了，以后学到其他的会来更新。