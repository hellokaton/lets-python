# 安装Python3

## 在Windows安装

在 https://www.python.org/downloads/windows/ 下载最新的Python安装包，
下载所需(注意自己的系统是32位还是64位)，安装路径最好选择默认, 不然对于新手容易出现各种问题。

Windows 安装附加要点:

**设置环境变量**

1. 找到安装路径, 默认 `C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python36` 粘贴路径
2. 我的电脑 - 属性 - 高级 - 环境变量 - 系统变量中的PATH为(复制路径): `C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python36;`

**pip3 设置环境变量**

```bash
C:\Users\**你的用户名**\AppData\Local\Programs\Python\Python36\Scripts;
```

## 在MacOS安装

Mac操作系统自带了Python2，你可以在 https://www.python.org/downloads/mac-osx/ 下载Python3的安装包，
安装到默认位置即可。

## 检查安装是否ok

如果你没有Python2的环境输入 `python -V` 就可以了。

```bash
⬢  ~  python3 -V
Python 3.6.2
```

## links
   * [目录](<README.md>)
