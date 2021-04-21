---
layout: posts

alt_title: "Python Exception"

# optional sub-title below the page title
sub_title: "Life is short, I learn Python"

# optional intro text below titles, Markdown allowed
introduction: |
    Python异常处理机制

categories: Articles
tags: 
    - Python
    - Exception
---
# Python异常处理机制
| 异常名字              | 异常情况                                     |
| --------------------- | -------------------------------------------- |
| AssertitonError       | 断言语句失败                                 |
| AttributeError        | 不存在该属性或者方法                         |
| EOFError              | input读取到EOF，但是却没有接收任何数据       |
| FloatingPointError    | 浮点计算错误                                 |
| GeneratorError        | generator.close()方法被调用的时候            |
| ImportError           | 导入模块失败                                 |
| IndexError            | 索引超出列表长度                             |
| KeyError              | 字典缺少键值                                 |
| KeyboradError         | Ctrl+C                                       |
| MemoryError           | 内存溢出                                     |
| NameError             | 尝试访问不存在变量                           |
| NotImplementedError   | 存在接口未被实现                             |
| OSError               | 操作系统异常                                 |
| OverflowError         | 数值运算超出类型所指定的大小                 |
| ReferenceError        | 弱引用尝试引用一个被垃圾回收机制所回收的对象 |
| RuntimeError          | 一般的运行时错误                             |
| StopIteration         | 迭代器没有更多的值                           |
| SyntaxError           | Python语法错误                               |
| IndentationError      | 缩进错误                                     |
| TabError              | Tab和空格存在混用                            |
| SystemError           | 编译器系统错误                               |
| SystemExit            | 编译器进程关闭                               |
| TypeError             | 不同类型数据之间的无效操作                   |
| UnboundLocalError     | 访问一个未初始化的本地变量——NameError子类    |
| UnicodeError          | Unicode相关问题——ValueError子类              |
| UnicodeEncodeError    | Unicode编码出错                              |
| UnicodeDecodeError    | Unicode解码出错                              |
| UnicodeTranslateError | Unicode转换出错                              |
| ValueError            | 传入无效参数                                 |
| ZeroDivisionError     | 0做分母                                      |

草，终于到了正文部分！

# 异常捕获和处理

## Try - Except

```python
try:
    int('abc')
    f = open('I'm a file.txt)
    f.close()
except ValueError as reason:
    print(reason+'===================================')
except OSError as reason:
    print(‘文件没了QAQ’)
```

## Try - Finally

```python
try:
    int('abc')
    f = open('I'm a file.txt,'w')
    f.write('我可以了！')
except ValueError as reason:
    print(reason+'===================================')
except OSError as reason:
    print(‘文件没了QAQ’)
finally:
    f.close()
```

# 引起异常

## 编译器自动提交异常

## 手动异常Raise

```python
raise OSError('我是个手动异常！')
```



