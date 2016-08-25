### 初识python
- python 是一种编程语言，经过二十年的发展，它提供了非常完善的基础代码库，覆盖了  
网络，文件，GUI，数据库，文本等大量内容。除了这些内置库，还有大量优秀的第三方库。
- python的特点是优雅，明确，简单。它非常适合开发网站，后台。也能开发日常需要的小工具，如果系统管理员需要的脚本任务。
- python的缺点就是：
    - 速度慢，作为解释性语言，慢不可避免，但无关紧要。
    - 代码不能加密，也无关紧要，现在是开源的世界，现在靠卖软件授权的商业模式越来越少，靠网站和移动应用卖服务的模式越来越多。

### 安装python&运行
- python是跨平台的，目前安装的是3.5。在windows上安装要注意勾选 `Add Python 3.5 to PATH`，然后点击 `Install Now` 安装即可。
- 可以进行简单的 100+400 然后按 enter 的计算，退出输入 exit() ;
- 我们编写python代码时，会得到一个包含python代码的以`py`为扩展名的文本文件。而要运行这恶鬼文件就需要python解释器。  
python的解释器很多，使用最广泛的还是CPython，这个解释器是用C语言开发的，所以叫CPython，在命令行下运行`python`就是启动CPython解释器。

### 输入和输出
`input` 和 `print` 是最基本的输入和输出。我们把输入输出统称为Input/Output，或简写为IO。

    name = input('please enter your name')
    print('hello,', name)
    
    // 运行后出出现友好的提示文字，现要求输入你的名字，然后输出欢迎词，
    // 有了输入，用户才能告诉计算机程序所需的信息，有了输出，程序运行后才能告诉用户任务的结果。
    
### python语法采用缩进方式
```py
a = 100
if a >= 0:
    print(a)
else:
    print(-a)
```

- 另外，坚持使用4个空格的缩进，python程序对 **大小写敏感**

### 数据类型
- 0.00012 可以用1.2e-4表示。
- print('I\'m \"ok\"!') 输出 I'm "ok"!
- 如果字符串里面有很多字符都需要转义，就需要加很多\，为了简化，Python还允许用r''表示''内部的字符串默认不转义
- 换行可以 print('''line1 然后enter，开始。```前面可以加r.
- and or not True False (None 表示空值)

### 字符串和编码
- 最早计算机8个比特一个字节。所以一个字节能表示的最大整数就是255。
- 最早由127个字符被编码到计算机里，包括大小写字母，数字和一些符号，这个编码表被称为 `ASCII`。
- 中文至少需要两个字节，而且还不能和 `ASCII` 冲突，因此中国制定了  `GB2312`,用来把中文编进去。  
然而世界上有上百种语言，不可避免的会有冲突，在多语言混合的文本中，显示出来会有乱码。
- 因此 `Unicode` 应运而生，它把所有语言都统一到一套编码中。就不会有乱码问题了。
- 而 `UTF-8` 可以将 Unicode 编码转化为 ‘可变长编码’。也就是把一个 Unicode 字符根据不同的数字大小编码成1-6个字节。  
从而节约了空间。
- 计算机系统通用的字符编码工作方式：  
在计算机内存中，统一使用 Unicode 编码，当需要保存到硬盘或者需要传输的时候，就转换为UTF-8编码。

### python 的字符串
- Python 3 版本中，字符串是以Unicode编码的，即：Python字符串支持多语言。
- `ord()` 获取字符的编码的函数，`chr()` 把编码转化为对应字符的函数.
- 如果要在网络上传输，或保存到磁盘上，就需要把 `str` 变成以字节为单位的 `bytes`。  
以 Unicode 表示的 str 通过 `encode()` 方法可以编码为指定的 bytes，  
纯英文的 str 可以用 ascii 编码为 bytes, 中文的 str 可以用 utf-8 编码为 bytes.
- 反过来，如果我们从网络或磁盘上读取了字节流，那么读到的数据就是 `bytes`。要把 `bytes` 变成 `str`，就需要 `decode()` 方法。
- 计算 `str` 包含多少个字符，可以用 `len()` 函数
- python 源文件包含中文的时候，务必指定保存为UTF-8。通常文件开头加上
```js
#!/usr/bin/env python3
# -*- coding: utf-8 -*-
```
- 第一行注释是为了告诉Linux/OS X系统，这是一个Python可执行程序，Windows系统会忽略这个注释；
- 第二行注释是为了告诉Python解释器，按照UTF-8编码读取源代码，否则，你在源代码中写的中文输出可能会有乱码。
- 申明了UTF-8编码并不意味着你的.py文件就是UTF-8编码的，必须并且要确保文本编辑器正在使用UTF-8 without BOM编码
- 在 python 中，使用 % 实现格式化方式。
- 占位符， %d 整数；%f 浮点数；%s 字符串；%x 十六进制整数

### list 和 tuple
- python 内置的一种数据类型是列表： list。
    classmates = ['M', 'H', 'B']
- 可以使用 `len()` 函数获取列表的个数；
- 可以使用索引来访问list中的每一个位置的元素，从 0 开始。如： classmates[0], 可以使用 `-1` 做索引，直接获取最后一个元素。
- 一次类推，倒数第二个是 classmates[-2],如果越界了就会报错。
- 添加/删除元素是：
    - 末尾添加：classmates.append('Adam')
    - 指定位置添加：classmates.insert(1, 'Jack')
    - 末尾删除：classmates.pop()
    - 指定位置删除：classmates.pop(2)
    - 指定位置替换元素：classmates[1] = 'minooo'
- 另外一种有序列表叫tuple（元组）。这是不可变数组，一旦初始化就不可修改。
- 定义一个空的tuple，可以：t = ()
- 定义只有一个元素的tuple，可以：t=(1,),这是为了避免歧义

### if else 语句
```js
height = 1.8
weight = 84
 
a = int(height)
b = int(weight)
 
bmi = b/(a^2)
 
if bmi > 32:
    print('严重肥胖')
elif bmi >= 28:
    print('肥胖', bmi)
elif bmi >= 25:
    print('过重')
elif bmi >= 18.5:
    print('正常')
else:
    print('过轻')
```

### 循环
- `for...in...` 循环，依次把list或tuple中的每个元素迭代出来，看例子
```js
names = ['M', 'N', 'A']
for x in names:
    print(name)
```

- 如果要计算1-100的整数之和，从1写到100有点困难，幸好Python提供一个`range()`函数，可以生成整数数列，再通过`list()`函数可以转化为list
- 第二种循环是while循环，只要条件满足就不断循环。
```js
sum = 0
n = 1
while n < 100:
    sum = sum + n
    n = n + 2
print(sum)
```

### 使用dict 和  set
- dict 是键值对的集合，有点类似于js中的对象。避免key不存在的错误
    - 通过`in`判断
    ```js
    >>> 'Tom' in d
    False
    ```
    - 通过dict提供的get方法，如果key不存在可以返回None，或者自己指定value
    ```js
    >>> d.get('Tom')
    >>> d.get('Tom', -1)
    -1
    ```
- 要删除一个key，用pop(key)方法，对应的value也会从dice中删除。
```js
>>> d.pop('Bob')
75 (返回 'Bob' 对应的值)
```
- dict内部存放的顺序和key放入的顺序是没有关系的。
- 和list比较，dict有以下几个特点：
 - 查找和插入的速度极快，不会随着key的增加而变慢；
 - 需要占用大量内存。
- 而list相反
- set和dict类似，也是一组key的组合，但不存储value，set中没有重复的key
```js
>>> s = set([1,1,3,3,4])
>>> s
{1,3,4}
```
- 可以通过`add(key)`方法可以添加元素到set中，可以重复添加，但不会有效果。
- 可以通过`remove(key)`方法删除元素
- set 可以堪称数学意义上的无序和无重复元素的集合，因此，两个set可以做数学意义上的交集、并集等操作
```js
>>> s1 = set([1,2,3])
>>> s2 = set([2,3,4])
>>> s1 & s2
{2,3}
>>> s1 | s2
{1,2,3,4}
```
- 字符串是不可变对象，而变量仅仅是指向。