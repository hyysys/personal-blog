---
title: python格式化
date: 2023-02-07 12:13:16
tags: python
      study
      基础
categories: pyhton基础
cover: "../img/yh-04.jpg"
---
# python输出格式化
## 利用%格式化

+ %s    字符串 (采用str()的显示)

+ %r    字符串 (采用repr()的显示)

+ %c    单个字符

+ %b    二进制整数

+ %d    十进制整数

+ %i    十进制整数

+ %o    八进制整数

+ %x    十六进制整数

+ %e    指数 (基底写为e)

+ %E    指数 (基底写为E)

+ %f    浮点数

+ %F    浮点数，与上相同

+ %g    指数(e)或浮点数 (根据显示长度)

+ %G    指数(E)或浮点数 (根据显示长度)

+ %%    字符"%"，显示百分号%

另外，比如我要固定字符的宽度，小数精度等，可以用如下的方式，对格式进行进一步的控制：
```python
%[(name)][flags][width].[precision] typecode

（1）(name)为命名：即参数的名称，可以没有这个，怎么使用呢？注意（name需要使用括号括起来哦！！！）

# 注意：这里的name，num括号不能掉
'Hey %(name)s, there is a %(num)f number!' % {"name": name, "num": number }
（2）flags可以有+,-,' '或0。+表示右对齐。-表示左对齐。' '为一个空格，表示在正数的左侧填充一个空格，从而与负数对齐。0表示左侧使用0填充。

（3）width表示显示宽度

（4）precision表示小数点后精度
```
## f 格式化输出
        print(f'..........')
