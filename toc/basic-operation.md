# 基础运算

我们前面只学会了如何输出一句 `Hello World`，当然开启了旅程的第一步，我们还有很多需要学习的~
本章节主要说明Python的运算符。举个简单的例子 `4 +5 = 9`。 `4` 和 `5` 被称为操作数，`"+"` 称为运算符。
Python语言支持以下类型的运算符:

- 算术运算符
- 比较（关系）运算符
- 赋值运算符
- 逻辑运算符
- 位运算符
- 成员运算符
- 身份运算符
- 运算符优先级

## 算术运算符

以下假设变量a为10，变量b为21：

| 运算符  | 描述 |  实例 |
|---|---|---|
| + | 加 - 两个对象相加 | a + b 输出结果 31 |
| - | 减 - 得到负数或是一个数减去另一个数 | a - b 输出结果 -11 |
| * | 乘 - 两个数相乘或是返回一个被重复若干次的字符串 | a * b 输出结果 210 |
| / | 除 - x 除以 y | b / a 输出结果 2.1 |
| % | 取模 - 返回除法的余数 | b % a 输出结果 1 |
| ** | 幂 - 返回x的y次幂 | a**b 为10的21次方 |
| // | 取整除 - 返回商的整数部分 | 9//2 输出结果 4 , 9.0//2.0 输出结果 4.0 |

下面是一个运算符操作的例子：

```python3
#!/usr/bin/python3

a = 21
b = 10
c = 0

c = a + b
print ("1 - c 的值为：", c)

c = a - b
print ("2 - c 的值为：", c)

c = a * b
print ("3 - c 的值为：", c)

c = a / b
print ("4 - c 的值为：", c)

c = a % b
print ("5 - c 的值为：", c)

# 修改变量 a 、b 、c
a = 2
b = 3
c = a**b
print ("6 - c 的值为：", c)

a = 10
b = 5
c = a//b
print ("7 - c 的值为：", c)
```

上面的例子将输出

```bash
1 - c 的值为： 31
2 - c 的值为： 11
3 - c 的值为： 210
4 - c 的值为： 2.1
5 - c 的值为： 1
6 - c 的值为： 8
7 - c 的值为： 2
```

## 比较运算符

以下假设变量a为10，变量b为20：

| 运算符  | 描述 |  实例 |
|---|---|---|
| == | 等于 - 比较对象是否相等 | (a == b) 返回 False |
| != | 不等于 - 比较两个对象是否不相等 | (a != b) 返回 True |
| > | 大于 - 返回x是否大于y | (a > b) 返回 False |
| < | 小于 - 返回x是否小于y。所有比较运算符返回1表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。 | (a < b) 返回 True |
| >= | 大于等于 - 返回x是否大于等于y | (a >= b) 返回 False |
| <= | 小于等于 - 返回x是否小于等于y | (a <= b) 返回 True |

下面是一个比较运算符的例子

```python3
#!/usr/bin/python3

a = 21
b = 10
c = 0

if ( a == b ):
   print ("1 - a 等于 b")
else:
   print ("1 - a 不等于 b")

if ( a != b ):
   print ("2 - a 不等于 b")
else:
   print ("2 - a 等于 b")

if ( a < b ):
   print ("3 - a 小于 b")
else:
   print ("3 - a 大于等于 b")

if ( a > b ):
   print ("4 - a 大于 b")
else:
   print ("4 - a 小于等于 b")

# 修改变量 a 和 b 的值
a = 5;
b = 20;
if ( a <= b ):
   print ("5 - a 小于等于 b")
else:
   print ("5 - a 大于  b")

if ( b >= a ):
   print ("6 - b 大于等于 a")
else:
   print ("6 - b 小于 a")
```

以上实例输出结果：

```bash
1 - a 不等于 b
2 - a 不等于 b
3 - a 大于等于 b
4 - a 大于 b
5 - a 小于等于 b
6 - b 大于等于 a
```

## 逻辑运算符

Python语言支持逻辑运算符，以下假设变量 a 为 10, b为 20:

| 运算符 | 逻辑表达式	| 描述 |  实例 |
|---|---|---|---|
| and | x and y | 布尔"与" - 如果 x 为 False，x and y 返回 False，否则它返回 y 的计算值 | (a and b) 返回 20 |
| or | x or y | 布尔"或" - 如果 x 是 True，它返回 x 的值，否则它返回 y 的计算值 | (a or b) 返回 10 |
| not | not x | 布尔"非" - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True | not(a and b) 返回 False |

例子

```python3
#!/usr/bin/python3

a = 10
b = 20

if ( a and b ):
   print ("1 - 变量 a 和 b 都为 true")
else:
   print ("1 - 变量 a 和 b 有一个不为 true")

if ( a or b ):
   print ("2 - 变量 a 和 b 都为 true，或其中一个变量为 true")
else:
   print ("2 - 变量 a 和 b 都不为 true")

# 修改变量 a 的值
a = 0
if ( a and b ):
   print ("3 - 变量 a 和 b 都为 true")
else:
   print ("3 - 变量 a 和 b 有一个不为 true")

if ( a or b ):
   print ("4 - 变量 a 和 b 都为 true，或其中一个变量为 true")
else:
   print ("4 - 变量 a 和 b 都不为 true")

if not( a and b ):
   print ("5 - 变量 a 和 b 都为 false，或其中一个变量为 false")
else:
   print ("5 - 变量 a 和 b 都为 true")
```

输出结果

```bash
1 - 变量 a 和 b 都为 true
2 - 变量 a 和 b 都为 true，或其中一个变量为 true
3 - 变量 a 和 b 有一个不为 true
4 - 变量 a 和 b 都为 true，或其中一个变量为 true
5 - 变量 a 和 b 都为 false，或其中一个变量为 false
```

## links
   * [目录](<../README.md>)