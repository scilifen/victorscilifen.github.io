---
layout: posts

alt_title: "Python Else & With"

# optional sub-title below the page title
sub_title: "Life is short, I learn Python"

# optional intro text below titles, Markdown allowed
introduction: |
    Python的else还有with

categories: Articles
tags: Python, While, With
---

## else在while和for里面

如果循环完了都没有一个真值出现，就执行else里的内容

如果循环里面有一个真值出现，那else里面的内容就一定不会被执行

如果try里面没有异常，那就执行else里的东西



## with:

```python
with open('i am a file') as f:
```

那么这个文件不用了就会自动关闭！

