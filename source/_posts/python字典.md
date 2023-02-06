---
title: python字典
date: 2023-02-06 17:30:58
tags: python
      study
      基础
categories: python基础
cover: "./img/gf-11.jpg"
---

# python字典基础知识

## 字典简介

字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值 key:value 对用冒号 : 分割，每个键值对之间用逗号 , 分割，整个字典包括在花括号 {} 中 ,格式如下所示：

```python
d = {key1 : value1, key2 : value2 }
```

注意：dict 作为 Python 的关键字和内置函数，变量名不建议命名为 dict。
键一般是唯一的，如果重复最后的一个键值对会替换前面的，值不需要唯一。
值可以取任何数据类型，但键必须是不可变的，如字符串，数字或元组。
一个简单的字典实例：

```python
tinydict = {'Alice': '2341', 'Beth': '9102', 'Cecil': '3258'}
tinydict1 = { 'abc': 456 }
tinydict2 = { 'abc': 123, 98.6: 37 }
```

## 访问字典里的值

```python
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
x = thisdict["model"]
print(x)
```

## 更改字典中的值

```
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict["year"] = 2019
```

## 遍历字典

您可以使用 for 循环遍历字典。

循环遍历字典时，返回值是字典的键，但也有返回值的方法。

实例
逐个打印字典中的所有键名：

```
for x in thisdict:
  print(x)
```

实例
通过使用 items() 函数遍历键和值：

```
for x, y in thisdict.items():
  print(x, y)
```

## 添加项目

通过使用新的索引键并为其赋值，可以将项目添加到字典中：

```
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict.pop("model")
print(thisdict)
```

## 删除项目

pop() 方法删除具有指定键名的项：

```
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
thisdict.pop("model")
print(thisdict)
```

del 关键字删除具有指定键名的项目(也可以完全删除整个字典)：

``` 
thisdict =	{
  "brand": "Porsche",
  "model": "911",
  "year": 1963
}
del thisdict["model"]
print(thisdict)
```

## dict()构造函数

也可以使用 dict() 构造函数创建新的字典：

``` 
thisdict = dict(brand="Porsche", model="911", year=1963)
# 请注意，关键字不是字符串字面量
# 请注意，使用了等号而不是冒号来赋值
print(thisdict)
```