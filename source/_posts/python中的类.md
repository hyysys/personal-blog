---
title: python中的类
date: 2023-02-07 11:42:50
tags: python
      study
      基础
categories: python基础   
cover: "../img/dt-05.jpg"  
---
# python中的类
## 创建类
python中使用class创建类
```python
class MyClass:
    x = 7
print(MyClass)
```
## 创建对象
有了类便可以创建对象
```python
p=MyClass()
print(p.x)
```
## __init__()函数
上面的例子是最简单形式的类和对象，在实际应用程序中并不真正有用。

要理解类的含义，我们必须先了解内置的 __init__() 函数。

所有类都有一个名为 __init__() 的函数，它始终在启动类时执行。

使用 __init__() 函数将值赋给对象属性，或者在创建对象时需要执行的其他操作：
创建名为 Person 的类，使用 __init__() 函数为 name 和 age 赋值：
```python
class Person:
    def __init__(self,name,age):
        self.name = name
        self.age = age
p1 = Person(bill,18)
print(p1.name)
print(p1.age)
```
**注释**:每次使用类创建新对象时，都会自动调用 __init__() 函数。
## 对象方法
对象也可以包含方法。对象中的方法是属于该对象的函数。
让我们在 Person 类中创建方法：
**实例**
插入一个打印问候语的函数，并在 p1 对象上执行它：
```python
class Person:
    def __init__(self,name,age):
        self.name = name
        self.age = age
    def myfun(self):
        print('hello,my name is ' + self.name,',I\'m ' + str(self.age))
P1 = Person('bill',19)
P1.myfun()
```
__提示：__ self 参数是对类的当前实例的引用，用于访问属于该类的变量。
## self参数
self 参数是对类的当前实例的引用，用于访问属于该类的变量。

它不必被命名为 self，您可以随意调用它，但它必须是类中任意函数的首个参数：

实例
使用单词 mysillyobject 和 abc 代替 self：
```python
class Person:
    def __init__(mysillyobject,name,age):
        mysillyobject.name = name
        mysillyobject.age = age
    def myfun(abc):
        print('hello,my name is ' + mysillyobject.name,',I\'m ' + str(mysillyobject.age))
P1 = Person('bill',19)
P1.myfun()
```
## 修改对象属性
您可以这样修改对象的属性：

实例
把 p1 的年龄设置为 40：
```python
class Person:
    def __init__(self,name,age):
        self.name = name
        self.age = age
p1 = Person(bill,18)
p1.age = 40
```
## 删除对象或对象属性
使用del
删除 p1 对象的 age 属性：
```python
del p1.age
```
删除p1对象：
```python
del p1
```
## pass语句
类定义不能为空，但是如果您处于某种原因写了无内容的类定义语句，请使用 pass 语句来避免错误。
```python
class Person:
    pass
```

