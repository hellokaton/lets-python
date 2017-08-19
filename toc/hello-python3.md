# Hello Python3

接下来我们编写程序界众所周知的第一个程序 `Hello World`。我们在Python自带的环境下运行：

```bash
⬢  ~  python3
Python 3.6.2 (default, Jul 17 2017, 16:44:45)
[GCC 4.2.1 Compatible Apple LLVM 8.1.0 (clang-802.0.42)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello Python3")
Hello Python3
>>>
```

你的终端将输出一行 `Hello Python3`。

## 编码

默认情况下，`Python3` 源文件以 `UTF-8` 编码，所有字符串都是 `unicode` 字符串。
当然你也可以为源码文件指定不同的编码：

```python
# -*- coding: gb2312 -*-
```

## 关键字

你可以在Python的交互式界面中查看有多少关键字

```bash
>>> import keyword
>>> keyword.kwlist
['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
>>> len(keyword.kwlist)
33
```

wow，33个还不少呢~

## 注释

在Python中注释是使用 `#` 来表示的。

**单行注释**

```python
# 输出一句Hello Python
print ("Hello, Python!") # 这也是一行注释
```

**多行注释**

```python
# this is first comment
# this is sencond comment
print ("Hello, Python!")
```

## 缩进

Python和Java语法上非常不同的一处在于它使用缩进表示代码块，而不是 `{}` （花括号）
像这样:

```python
if flag:
    print("flag is true")
else:
    print("flag is flase")
```

如果你的缩进数不一致会导致错误，像这样的代码是不可行的

```python
if flag:
    print("flag is true")
    print("this is big..")
else:
    print("flag is flase")
   print("haha~") # 缩进不一致，会导致运行错误
```

## 数据类型

python中数有四种类型：整数、长整数、浮点数和复数。

- 整数: 如1
- 长整数: 是比较大的整数
- 浮点数: 如 `1.23`、`3E-2`
- 复数: 如 `1 + 2j`、 `1.1 + 2.2j`

## links
   * [目录](<../README.md>)
