---
layout: posts

alt_title: "Python OOP"

# optional sub-title below the page title
sub_title: "Life is short, I learn Python"

# optional intro text below titles, Markdown allowed
introduction: |
    Python面向对象编程

categories: Articles
tags: 
    - Python
    - OOP
---

# Python OOP

## 类对象

Class 类名一般首字母大写

定义属性

定义方法

```python
class Turtle:
    shell = True
    weight  = 100
    
    def bite(self):
        print('Aha!')
```

## 对象

对象实例化：

```python
tt = Turtle()
```

### 继承

```python
class MyList(list):
    # 意思是继承list类
```

注意:

继承之后的子类如果有与父类同样的模块，那么就完成了重写。

#### 重写

当我需要继承父类的部分方法时：

1. 复制粘贴代码
2. 调用父类.方法
3. super().方法()

### 多态

在不同类里，同一个方法名字实现不同的功能。

好扯的多态，这感觉更像是我只是在调用刚好名字相同的方法而已。你们的归属不同，方法的功能不同其实很简单就能理解。

但是在Java里面，多态更接近面对对象编程的思想一些。

### Self参数

在类对象的方法定义中，常常会传入一个默认参数self

```python
class Ball:
    def setName(self,name):
        self.name = name
        
    def kick(self):
        print('I am %s',% self.name)
```

可以这么认为，self就是这个对象实例化之后的本身，我可以新建属性向里面传入来给这个类里面其他的方法调用。有点那个类中公共区域的感觉。

### __init_ __构造方法

```python
class Person:
    __inti__ (self,name):
        self.name = name
```

当我每次创建这个对象的时候，都需要传入一个name。

### 公有和私有

加两个下滑线就变成了有趣的私有变量。

_类名__变量强行访问

## BIF

issubclass

isinstance

hasattr

getattr

setattr

delattr

property(set,get,del,doc)

# 小甲鱼作业：

```python
import random as r


class Animal:
    def __init__(self):
        self.x = r.randint(0, 10)
        self.y = r.randint(0, 10)

    def move(self):
        self.x = self.x + r.choice([1, -1])
        self.y = self.y + r.choice([1, -1])
        check(self)


class Turtle(Animal):
    def __init__(self):
        super(Turtle, self).__init__()
        self.power = 100

    def move(self):
        choice = r.choice([0, 1])
        if choice == 0:
            self.x = self.x + r.choice([1, -1, 2, -2])
        elif choice == 1:
            self.y = self.y + r.choice([1, -1, 2, -2])
        self.power = self.power - 1
        check(self)

    def eat(self):
        self.power += 10
        if self.power > 100:
            self.power = 100


def check(obj):
    if obj.x > 10:
        obj.x = 20 - obj.x
    elif obj.x < 0:
        obj.x = 0 - obj.x
    elif obj.y > 10:
        obj.y = 20 - obj.y
    elif obj.y < 0:
        obj.y = 0 - obj.y


def game():
    turtle = Turtle()
    fish = []
    fish_count = 10
    for each in range(10):
        new_fish = Animal()
        fish.append(new_fish)

    while True:
        if turtle.power == 0:
            print('Lose!')
            break
        elif fish_count == 0:
            print('Win!')
            break
        for each in fish[:]:
            if each.x == turtle.x and each.y == turtle.y:
                fish_count -= 1
                turtle.eat()
            else:
                each.move()
            turtle.move()


def run(num):
    for i in range(num):
        game()


run(20)

```

