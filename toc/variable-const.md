# 变量、常量

在Python中变量不需要声明，变量的赋值操作既是变量声明和定义的过程。每个变量在内存中创建，都包括变量的标识，名称和数据这些信息。

## 变量

### 变量的命名

> 首字母必须是字母或下划线，首字符以外的字符可以由字母，数字或下划线组成。

### 变量的赋值

**一次新的赋值操作，将创建一个新的变量**

```python
num = 25
print(num)
```

**多个变量赋值**

```python3
a = b = c = 22
```

您也可以为多个对象指定多个变量。例如：

```python3
a, b, c = 1, 2, "biezhi"
```

### 局部变量

局部变量是只能在函数或代码段内使用。函数或代码段一旦结束，局部变量的生命周期也将结束。
局部变量的作用范围只在局部变量被创建的函数内有效。

> python创建的变量就是一个对象。Python会管理变量的生命周期，Python对变量的回收采用的也是垃圾回收机制。

```python
def hello():
    local = 1
    print(local)
# 调用hello函数
hello()
```

### 全局变量

全局变量是能够被不同的函数，类或文件共享的变量，在函数之外定义的变量都可以称为全局变量。
全局变量可以被文件内部的任何函数和外部文件访问。

> `global`是保留字，`global`用于引用全局变量。

```bash
#!/usr/bin/python3

# 在文件的开头定义全局变量
_a = 1
_b = 2
def add():
    global _a
    _a = 3
    return "_a + _b =", _a + _b
def sub():
    global _b
    _b = 4
    return "_a - _b =", _a - _b
print add()
print sub()
# 错误的使用全局变量
_a = 1
_b = 2
def add():
    _a = 3
    return "_a + _b =", _a + _b
def sub():
    _b = 4
    return "_a - _b =", _a - _b
print add()
print sub()
```

## 常量

常量是指一旦初始化后就不能修改的固定值。c++中使用const保留字指定常量，而Python并没有定义常量的保留字。
但是python是一门功能强大的语言，可以自己定义一个常量类来实现常量的功能。

```bash
class _const:
    class ConstError(TypeError):
        pass

    def __setattr__(self, name, value):
        if self.__dict__.has_key(name):
            raise self.ConstError, "Can't rebind const instance attribute (%s)" % name

        self.__dict__[name] = value

import sys
sys.modules[__name__] = _const()
```

其大致含义为：

- 通过_const的__setattr__对象方法判断该对象是否存在属性name，若存在则抛出自定义异常ConstError，否则创建该属性。
- 将_const实例化的对象赋值sys.modules[__name__]，const模块被绑定成_const对象。__name__在首次载入const过程中为'const'，而sys.modules是模块名与已加载模块的dict。

如何使用const模块呢？

```bash
import const
const.magic = 23
```

若再次赋值const.magic，

```bash
const.magic = 88
```

则将抛出 `ConstError` 异常。

### 如何避免常量被删除？

实际项目中，常量并不希望被其他代码删除。在_const类中加入：

```bash
def __delattr__(self, name):
    if self.__dict__.has_key(name):
        raise self.ConstError, "Can't unbind const const instance attribute (%s)" % name

    raise AttributeError, "const instance has no attribute '%s'" % name
```

如此，删除已定义的常量（假设const.magic已经赋值）：

```bash
del const.magic
```

则将抛出`ConstError`异常。

## links
   * [目录](<../README.md>)