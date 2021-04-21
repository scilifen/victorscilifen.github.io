---
layout: posts

alt_title: "Python Formatted Output"

# optional sub-title below the page title
sub_title: "Life is short, I learn Python"

# optional intro text below titles, Markdown allowed
introduction: |
    Python的格式化输出

categories: Articles
tags: 
    - Python
    - 格式化输出

---

# 格式化输出
主要是针对print函数进行的，花式print

```python
print('C:\\three\\two\\one\\now\n')
print("\"life is short,let\'s learn python!\"\n")
print(r'c\three\teo\one')

# m.n m指显示的最小总长度，n指的是小数点后的位数（四舍五入）
# - 用于左对齐
# + 用于显示正数正号
# # 用于在8进制数前显示0，在16进制数前显示0x
# 0 显示的数字用0替代空格
# enumerate -> (index,value)
# a=[1,2,3,4]
# b=[5,6,7,8]
# list(zip(a,b))->[(1,5),(2,6),(3,7),(4,8)]
```

|      |                             |
| ---- | --------------------------- |
| %c   | 格式化字符 ASCII码          |
| %s   | 格式化字符串 没什么用       |
| %d   | 格式化整数                  |
| %o   | 格式化无符号8进制数         |
| %x   | 格式化无符号16进制数        |
| %X   | 格式化无符号16进制数 大写   |
| %f   | 格式化定点数 可指定小数位数 |
| %e   | 用科学计数法格式化          |
| %E   | 用科学计数法格式化 大写     |
| %g   | 根据值的大小来自动选择%f %e |
| %G   | 根据值的大小来自动选择%f %E |

