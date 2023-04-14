[toc]





# 一、python基础

author：李政震

==起点低、当下净、回头脏、平常道==



## 1 基本概念

**简单、明确、优雅**



**python：**

* 解释型语言
* 动态语言
* 动态类型语言
* 强类型语言
* 面向对象程序设计



1989	有想法

1991	第一个python诞生



**计算机技术的演进**：

* 1946-1981	计算机系统结构时代（35年）	计算能力问题
* 1981-2008	网络和视窗时代（27年）	        交互问题
* 2008		    （安卓诞生）	
* 2008-2016	复杂信息系统时代（8年）	       数据问题
* 2016		    （人机大战  柯洁）		                人类的问题
* 2016-		    人工智能时代



**python语言的特点：**
	语法简洁		  生态高产
	C代码量的10%	13万第三方库
	强制的可读性	快速增长的计算生态
	较少的底层语法元素	避免重复造轮子
	多种编程方式	开房共享
	支持中文字符	跨操作系统平台



**如何看待python：**
	人生苦短，我学python

​	==Life is short, you need Python==

​	

机器语言：	二进制，二进制代码指令	cpu
汇编语言：	二进制代码直接对应助记符	cpu型号有关，程序不通用，需要汇编器转换
高级语言：	更接近自然语言		与CPU型号无关，编译后运行
超级语言：粘性整合已有程序，具备庞大计算生态





python解释器：   **python.exe**

```txt
想法 ==编写==》 python代码 ==》python解释器 ==翻译==》0101二进制 ==提交==》执行
```



> 类库
>
> * Numpy  （Numeic Python）
>
>   > 处理数值计算的python库
>   >
>   > 数学基础库
>
> * SciPy   （Science Python）
>
>   > 面向科学计算的python库
>
> * Pandas   （Python Data Analysis Library）
>
>   > 面向python的数据分析库
>
> * Matplotlib   
>
> * Seaborn
>
> * scikit-learn



python3.x所有字符的编码是Unicode

python2.x字符时需要在字符前面显式加上标识符u

>  ```python
>  from __future__ import                  # 导入未来包，解决python2.x不兼容
>  ```







## 2 软件安装

### 2.1 python

官方网址：[Welcome to Python.org](https://www.python.org/)

![image-20221220153607962](D:\Typora\picture\image-20221220153607962.png)

![image-20221220153733291](D:\Typora\picture\image-20221220153733291.png)

![image-20221220153757747](D:\Typora\picture\image-20221220153757747.png)

![image-20221220153829882](D:\Typora\picture\image-20221220153829882.png)

![image-20221220153909698](D:\Typora\picture\image-20221220153909698.png)

![image-20221220153924098](D:\Typora\picture\image-20221220153924098.png)

验证：cmd   

```txt
$ python
```

```txt
$ python --version
```



### 2.2 Anaconda

```linux
conda install 类库名
```





### 2.3 PyCharm

安装插件：

translation（第一个翻译）

Chinese（第二个中文版）



快捷键：

`ctrl`+`alt`+`S`	打开设置

`ctrl`+`D`	复制当前行

`shift`+`alt`+ ↑↓   移动当前行

`ctrl`+`shift`+`F10`   运行

`shift`+`F6`  重命名

`shift`+`alt`+鼠标左键拖动		滑选



**Anaconda导入PyCharm：**

![image-20230410165935567](D:\Typora\picture\image-20230410165935567.png)



### 2.4 Jupyter notbook

文学化编程（Literate Programming）

安装Anaconda时，Jupyter就被默认安装了

```windows
conda install jupyter notebook
```

有两种单元格：代码单元格、文本单元格

每个单元格都有两种模式：编辑模式、命令模式

> `Esc`	切换模式
>
> `A`		向上建立一个单元格
>
> `B`		向下建立一个单元格
>
> `DD`	  删除当前单元格
>
> `Shift` + `Enter`    运行
>
> `Shift` + `M`      合并单元格
>
> `ll`       显示行号
>
> `m m`     转成Markdown
>
> `y y `     转成代码模式



> View —— Toggle Line Number（切换到行号）   显示代码框中的行号



#### 2.4.1 魔法函数

```python
%lsmagic
```

> 列出所有魔法函数。list、ls

```python
%matplotlib lnline
```

> 告诉IPython，我们的绘图模式是内嵌模式，即绘图直接显示在当前的网页上
>
> plt.show()  可以省略

```python
%matplotlib qt
```

> 代码构造的图形是通过独立窗口显示

```python
%timeit
```

> 为某行代码的执行能力提供计时服务
>
> 在评估机器学习算法的性能、评估运行时间时特别有用

> ```python
> %timeit area = (40 * np.random.rand(20)) ** 2
> %timeit -n10 out = sess.run(a)
> ```

```python
%timeit?       # 查看某个魔法函数的具体用法
```

```python
%%writefile 保存的文件名.py   # 保存文件
```

```python
%run    # 运行.py格式的python代码
```

```python
%load   # 用外部脚本替换当前单元格
```



#### 2.4.2 shell命令

```shell
!ls    # 显示当前文件列表
```

```python
!pwd   # 显示当前目录
```





### 2.5 Markdown

- 轻量级的可使用普通文本编辑器编写的标记语言
- 约翰 · 格鲁伯 于 2004 年创建

```markdown
# 一级标题
###### 六级标题

**粗体**
*倾斜*
~~删除线~~
**粗体_粗体斜体_**

> 引用内容

- 无序列表1
- 无序列表2

1. 有序列表1
2. 有序列表2
```







## 3 基础语法

### 3.1 缩进

1个tab键

4个空格

```python
for i in range(10):
    pass
```



### 3.2 注释

```python
# 单行注释
```

```python
'''
多行注释
'''
```

>  单行注释：单行代码；一小段代码
>
>  多行注释：整个python代码文件；类；方法



### 3.3 内置函数

> Build in Function   简称BIF

IPython、IDLE

```python
Python 3.11.0 (main, Oct 24 2022, 18:26:48) [MSC v.1933 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.

>>> dir(__builtins__)

['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BaseExceptionGroup', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EncodingWarning', 'EnvironmentError', 'Exception', 'ExceptionGroup', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'aiter', 'all', 'anext', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip'
 
 >>> help(zip)     # help(内置函数名)    查看帮助文档
```

> Tab   自动补全





### 3.4 数据类型

在代码中，被写下来的固定的值，称为字面量

| 类型               | 描述                                  | 说明 |
| ------------------ | ------------------------------------- | ---- |
| 数值（ Number）    | 整数（int)  浮点数 float 复数 complex |      |
| 布尔（Boolean）    | True  False                           |      |
| 字符串（String）   | 描述文本                              |      |
| 列表（List）       | 有序 可变                             |      |
| 元组（Tuple）      | 有序 不可变                           |      |
| 字典（Dictionary） | 无序 键值对                           |      |
| 集合（Set）        | 无序 不重复                           |      |

> 二进制	
>
> 八进制	0
>
> 十进制
>
> 十六进制

> 浮点数：按照科学计数法表示时，一个浮点数的小数点位置是可变的

> 科学计数法：
>
> 1.23e9   1.23E-9





### 3.3 变量

变量的名称  = 变量的值

```txt
 命名规则： 大小写字母 数字 下划线 汉字
（大小写敏感 首字符不能是数字、不能与保留字相同）
```

变量可以具有短名称（如 x 和 y）或更具描述性的名称（年龄、车名total_volume）。 Python 变量的规则：

- 变量名称必须以字母或下划线字符开头
- 变量名称不能以数字开头
- 变量名称只能包含字母数字字符和下划线（A-z、0-9 和 _）
- 变量名称区分大小写（age、age 和 AGE 是三个不同的变量）
- 变量名称不能是任何 [Python 关键字](https://www.w3schools.com/python/python_ref_keywords.asp)。



### 3.4 标识符

英文	中文	数字	下划线（_）

1. 不推荐使用中文；不能以数字开头
2. 大小写敏感
3. 不能使用关键字



规范：

1. 见名知意
2. 下划线命名法
3. 英文字母全小写



保留字：（33个）
	and	elif	import	raise	global
	as	else	in	return	nonlocal
	assert	except	is	try	True
	break	finally	lambda	while	False
	class	for	not	with	None
	continue	from	or	yield		
	def	if	pass	del	



### 3.5 运算符

#### 3.5.1 算术运算符

```python
# 算术运算符
正（+）负（-）
加（+）减（-）乘（*）除（/）
整除（//）取余（%）幂（**）
```

#### 3.5.2 关系运算符

```python
# 关系运算符（比较运算符）
等于（==）不等于（!=）
大于（>）小于（<）
大于等于（>=）
小于等于（<=）
```

#### 3.5.3 身份运算符

```python
# 身份运算符
is         # 判断两个标识符是不是引用自一个对象
is not     # 判断两个标识符是不是引用自不同对象
```

> 用于比较两个对象的内存地址是否一致（是否是对同一个对象的引用）
>
> ```python
> '对象' is None   # python中针对None的比较建议用is
> 
> ```

> [is]:用于判断两个变量引用对象是否是同一个
> [==]: 用于判断引用变量的值是否相等

#### 3.5.4 自反赋值运算符

```python
# 自反赋值运算符
+=		# 加法赋值运算符
-=		# 减法赋值运算符
*=		# 乘法赋值运算符
/=		# 除法赋值运算符
%=		# 取模赋值运算符
**=		# 幂赋值运算符
//=		# 取整除赋值运算符
```

#### 3.5.5 位运算符

```python
# 位运算符
&		# 按位与	 	 111
|		# 按位或	 	 101
^		# 按位异或	 	101
~		# 按位取反		10 01
<<		# 左移动	
>>		# 右移动
```

#### 3.5.6 逻辑运算符

```python
# 逻辑运算符
and		# 与运算
or		# 或运算
not		# 非运算
```

#### 3.5.7 成员运算符

```python
# 成员运算符
in		# 如果在指定序列中找到值，True
not in	# 如果在指定序列中没有找到值，True
```

#### 3.5.8 三目运算符

```python
# 三目运算符
表达式1 if 判断条件 else 表达式2
```



### 3.6 数据输入

```python
input("请告诉我你是谁？")
```



### 3.7 ASCII码表

* 0-9	48-57
* A-Z    65-90
* a-z     97-122







## 4 数据类型

![image-20221220233302667](D:\Typora\picture\image-20221220233302667.png)

### 4.0 基础知识

```python
type("小政")   # String
```

> type(变量)   查看变量存储的数据类型

```python
int(X)		# 将x转换为一个整数
float(x)    # 将x转换为一个浮点数
str(x)   	# 将对象x转换为一个字符串

long(x)
complex(real[,imag])
repr(x)   	# 字符串表达式
eval(str)   # 评估函数
tuple(s)   	# 元组
list(s)   	# 列表

chr(x)   	# 整数->字符
unichr(x)  	# 整数->unicode字符
ord(x)      # 字符->整数

hex(x)   	# 16
oct(x)   	# 8
```

> 任何类型都可以转字符串
>
> 浮点数转整数会丢失精度



####  4.0.1 五种类型比较

* 列表：一批数据，可修改，可重复
* 元组：一批数据，不可修改，可重复
* 字符串：一串字符串
* 集合：一批数据，去重
* 字典：一批数据，根据key检索value

![五种类型比较](D:\Typora\picture\image-20221222000148063.png)



### 4.1 数值型



### 4.2 布尔型

True      False   （首字母大写）

 1非空    0空





### 4.3 字符串

**==只可以存储字符串、长度任意、支持下标索引、允许重复字符串存在、不可以修改、支持for循环==**

#### 4.3.1 字符串定义

```python
name = 'lizhengzhen'
name = "lizhengzhen"
name = """li   zheng   zhen"""
```

#### 4.3.2 格式化输出

```python
print("姓名：",name)
print("姓名：" + name)
print("姓名：%s，年龄：%d，分数：%f"%(name,age,score))
print(f"姓名{name}")
```

> m.n
>
> m：控制宽度      %5d： (空格)(空格)(空格)11
>
> n： 控制精度       %.2f    11.345   11.35    （四舍五入）

> %s   字符串
>
> %d   有符号的十进制整数
>
> %f    浮点数

> 【转义字符】
>
> `\t`    制表符：一个tab键，四个空格
>
> `\n`    换行
>
> ```python
> print(r'\\\python\\\')    # \\\python\\\
> ```

> 【结束符】
>
> ```python
> print('输入的内容',end='\n')
> ```

##### 4.3.2.1 .format()

```python
print("姓名：{}，年龄：{}，分数：{}".format(name,age,score))
print("姓名：{1}，年龄：{0}，分数：{2}".format(age,name,score))
```

> 可以传入下标

> {:value}      设置显示宽度
>
> ```python
> "开始——{:5}".format("运动")   # '开始——运动   '    有三个空格
> "开始——{:1}".format("运动")   # '开始——运动'    
> ```
>
> {:<value}      左对齐
>
> ```python
> "开始——{:<6}".format("运动")   # '开始——运动    '   有四个空格  
> ```
>
> {:>value}      右对齐
>
> ```python
> "开始——{:>6}".format("运动")   # '开始——    运动'   有四个空格  
> ```
>
> {:^value}      居中
>
> ```python
> "开始——{:^6}".format("运动")   # '开始——  运动  '   两边各两个空格
> ```
>
> {:*^value}      居中（ * 填充）
>
> ```python
> "开始——{:*^6}".format("运动")   # '开始——**运动**'   *填充  
> ```
>
> {:,}      设置千分位符号
>
> ```python
> "数字{:,}".format(123456789)   # '数字123,456,789'   
> ```
>
> {:+.valuef}      设置显示精度 （+ 用来输出符号，可省略）（ . 表示精度）（ f 进行精度限制）
>
> ```python
> "数字{:.2f}".format(123.456789)   # '数字123.46'
> "{:.5}".format("hello world") # "hello"
> ```
>
> {:str}		指定显示类型
>
> ```python
> # 整数
> b	二进制
> e	Unicode字符
> d	十进制
> o	八进制
> x	小写十六进制
> X	大写十六进制
> # 浮点数
> e	小写字母e的指数形式
> E	大写字符E的指数形式
> f	标准浮点类型
> %	百分比类型
> ```

#### 4.3.3 切片

<font color='red' size=6 ><b>up to but not including</b></font>            [左闭右开)

```txt
序列[开始位置下标:结束位置下标:步⻓]
```

> 字符串下标从0开始
>
> 步长默认是1，正负均可

> 【例子】
>
> 我	爱	你	中	国
>
> 0	   1	  2      3     4
>
> -5      -4     -3    -2    -1

#### 4.3.4 常用方法

```python
dir(str)   # 查看字符串对象有哪些可用的对象
help(str.split)  # 查看split的用法
```

| 函数                          | 功能                                 | 备注       |
| ----------------------------- | ------------------------------------ | ---------- |
| upper()                       | 变大写                               | AAA        |
| lower()                       | 变小写                               | aaa        |
| title()                       | 标题化                               | Aa Bb Cc   |
| capitalize()                  | 首字母大写                           | Aa bb cc   |
| swapcase()                    | 大变小，小变大                       | aA BB CC   |
|                               |                                      |            |
| isdecimal()                   | 是否全是数字                         |            |
| isalpha()                     | 是否全是字母                         |            |
| isalnum()                     | 是否只含数字和字母                   |            |
| isupper()                     | 是否全大写                           |            |
| istitle()                     | 是否首字母大写                       |            |
| isspace()                     | 是否是空白符（空格、换行、制表符）   |            |
| isprintable()                 | 是否为可打印字符                     |            |
| isidentifier()                | 是否符合命名规则                     |            |
|                               |                                      |            |
| center(width,”填充字符”)      | 居中，空格填充width宽                |            |
| ljust(width,”填充字符”)       | 左对齐                               |            |
| rjust(widht,”填充字符”)       | 右对齐                               |            |
|                               |                                      |            |
| startwith(sub[,start,[,end]]) | 是否是sub开头                        |            |
| endwith(sub[,start,[,end]])   | 是否是sub结尾                        |            |
| find(sub[,start,[,end]])      | 返回sub第一次出现的下标              | 没有返回-1 |
| rfind(sub[,start,[,end]])     | 从右往左找                           | 没有返回-1 |
| index(sub[,start,[,end]])     | 返回sub第一次出现的下标              | 没有报错   |
| rindex(sub[,start,[,end]])    | 从右往左找                           | 没有报错   |
|                               |                                      |            |
| replace(old,new[,count])      | 替换。                               |            |
| pratition(sep)                | 切开。切成三部分                     | 返回元组   |
| split(sub,count)              | 切开。按照指定字符分割字符串         |            |
| strip()                       | 去边。移除两边（空格、换行、制表符） |            |
| lstrip()                      | 删左边空白字符                       |            |
| rstrip()                      | 删右边空白字符                       |            |
| join()                        | 合并。可迭代数据用字符串连接起来     |            |
| count(sub[,start,[,end]])     | 计数。统计sub在字符串中的个数        |            |

> ```python
> s = ['xiao','zheng']
> print(''.join(s))     # xiaozheng
> ```
>
> 可迭代数据：字符串、列表、元组、字典、集合  （且每个元素都必须是字符串）

#### 4.3.5 常量

| 常量            | 说明           | 说明 |
| --------------- | -------------- | ---- |
| ascii_lowercase | a~z            | 集合 |
| ascii_uppercase | A~Z            | 集合 |
| ascii_letters   | 所有大小写字母 | 集合 |
| digits          | 0~9            | 集合 |
| hexdigits       | 十六进制       | 集合 |
| octdigits       | 八进制         | 集合 |
| punctuation     | 特殊字符       | 集合 |
| printable       | 所有字符集合   | 集合 |
| whitespace      |                | 集合 |

> ```python
> import string
> 
> print(string.ascii_letters)
> ```

> 字符串对象是不可变的，所以一旦某个字符串被赋值，该字符就被视为一个常量。
>
> ```python
> s = 123456
> s[0] = 'H'   # 报错
> ```







### 4.4 列表 

**==有序、任意数量元素、允许重复元素、可修改==**

#### 4.4.1 创建

```python
ls = []   # 空列表
ls = list()  # 空列表 
```

```python
ls = ['xiao','zheng',2001]    # 可以存储混合类型
```

```python
ls = [[1,2,3],
      [4,5,6]]
```

> 1. 列表索引从0开始
> 2. 元素个数没有限制
> 3. 可以存储整数、小数、字符串、列表、元组等任何数据类型的数据，并且同一个数据列表中元素的类型可以不同

#### 4.4.2 增加

```python
# 增
ls.append("666")   				# 尾插   （一整个插入）
ls.extend(['0','1','2'])   		# 尾插   （一个一个插）
ls.insert(4,'3')   				# 指定下标插
```

> id(ls)    发现在经过多种方法操作后，列表对象ls的内存地址始终如一    （原地操作）
>
> id()     # 获取对象的内存地址

#### 4.4.3 删除

```python
# 删
ls.remove('3')   	# 删除第一个与指定值相同的元素  （删除）
ls.pop()   			# 弹出最后一个  （删除）   【默认-1】
ls.pop(2)   		# 弹出索引为2的 （删除）
ls.clear()   		# 清空列表  （清空）
del ls[0]  			# 删除下标  （指定删除）
del ls[1:3]  		# 删除切片  （指定删除）
```

#### 4.4.4 更改

```python
# 改 
ls.copy()  			# 复制
ls[0] = 'xiao'
```

#### 4.4.5 查找

```python
# 查
print(ls[0])   		# xiao
print(ls[::-1])  	# [2001,'zheng','xiao']    	# 支持切片

ls.index(2)  	    # 返回2第一次出现的下标，没有则报错
ls.count(2)         # 统计2在列表中出现的次数

ls.sort()   		# 按字典排序  （伤筋动骨）
ls.reverse()		# 按字典逆序  （伤筋动骨）
```

> dir(list)           # 列举出list的内置方法

#### 4.4.6 拓展

```python
# 拓展
len([1,2,3])    	# 求列表长度			# 3
[1,2,3]+[4,5,6]   	# 支持加法			 # [1,2,3,4,5,6]
['xiao']*2   	    # 支持乘法 			 # ['xiao','xiao']
3 in [1,2,3]        # True
for i in [1,2,3]: print(i)  # 遍历      # 1 2 3
    

sorted(ls要排序的列表, reverse=F升序/T降序)   # 排序   （不会影响原列表顺序）

# 炸开效果
ls = list('xiaozheng')   # ['x', 'i', 'a', 'o', 'z', 'h', 'e', 'n', 'g']

```

#### 4.4.7 函数

| 函数                               | 功能                                 | 说明                  |
| ---------------------------------- | ------------------------------------ | --------------------- |
| list（seq）                        | 元组转为列表                         |                       |
| all（iterable）                    | 都是真，True                         |                       |
| any（iterable）                    | 一个真，True                         |                       |
| len（s）                           | 求个数                               |                       |
| max（iterable）                    | 最大元素                             |                       |
| min（iterable）                    | 最小元素                             |                       |
| sorted（iterable）                 | 排序                                 |                       |
| sum（iterable[，start]）           | 求和                                 |                       |
| cmp（ls1, ls2）                    | 比较两个元素                         |                       |
|                                    |                                      |                       |
| **zip(ls1, ls2)**                  | **将多列表元素组合成一个元组**       | **拉链**              |
| **enumerate(sequence, [start=0])** | **枚举**                             | **枚举**              |
|                                    |                                      |                       |
| append（x）                        | 追加到末尾                           |                       |
| extend（x）                        | 添加到末尾                           |                       |
| insert（i，x）                     | 指定下标i插入x                       |                       |
| remove（x）                        | 删除第一个x                          | 没有则报错            |
| pop（[i]）                         | 弹出第i个元素并返回它,默认弹最后一个 | 会修改原列表          |
| index（x）                         | 返回第一个x的下标                    | 没有则报错            |
| count（x）                         | 返回x的次数                          |                       |
| sort（cmp，key，reverse=False）    | 排序                                 | Flase：升序True：降序 |
| reverse（）                        | 逆置                                 |                       |

> 【sort 和 sorted】
>
> ```python
> ls = [1, 9, 6, 4, 7, 5, 2, 3]
> ls.sort()
> print(ls)		# [1, 2, 3, 4, 5, 6, 7, 9]  原列表更改
> 
> ls = [1, 9, 6, 4, 7, 5, 2, 3]
> ls2 = sorted(ls)
> print(ls)   # [1, 9, 6, 4, 7, 5, 2, 3]  原列表不更改
> print(ls2)  # [1, 2, 3, 4, 5, 6, 7, 9] 
> ```

> **【拉链】**
>
> ```python
> fruits = ['apple','banana','pear','orange','kiwi']
> list(zip(fruits,range(len(fruits))))
> --------------------------------------------------
> [('apple', 0), ('banana', 1), ('pear', 2), ('orange', 3), ('kiwi', 4)]
> ```
>
> > 若是两个列表长度不一样，zip()会根据较短列表的长度，实施最大限度的缝合

> **【 枚举】**
>
> ```python
> fruits = ['apple','banana','pear','orange','kiwi']
> list(enumerate(fruits,start=1))
> --------------------------------------------------
> [(1, 'apple'), (2, 'banana'), (3, 'pear'), (4, 'orange'), (5, 'kiwi')]
> ```
>
> > start：下标起始位置





### 4.5 元组

**==有序、任意数量元素、允许重复元素、不可修改、支持for循环==**

<font color='red' size='6px'>**元组中的元素一旦创建，便不能修改。**</font>

> 有点像常量版本的列表，故此，有人将其称为 “带上枷锁的列表”

> 当我们需要在程序内封装数据，又不希望封装的数据被篡改，那么元组就非常合适了。



#### 4.5.1 创建

```python
tup = ()   		# 空元组
tup = tuple()   # 空元组
```

```python
t = (100,)  	# 创建只包含一个元素的元组
t = ('xiao','zheng',2001)
t = 'a','b','c','d'   # 定义一个没有括号的元组
```

```python
# 互换
t = tuple([1,2,3])    # 列表转成元组
t = tuple('123')      # 字符串转成元组
```



#### 4.5.2 增加

```python
# 增
t = ('小政',2023,4.10)
t = t[:1] + ('xiaozheng',) + t[1:]
```

> “狸猫换太子”
>
> 此时，python解释器会生成一个新元组（即开辟了新的内存空间），然后将原来的变量名指向这个连接好的新元组，旧的同名元组被销毁



#### 4.5.3 查找

```python
# 查
print(t[0])   		# 下标查
print(t[1:])   		# 支持切片
ls.index('666')	 	# 返回666第一次出现的下标，没有则报错
```

> 元组的切片操作会临时产生一个新的元组，他不会改变原先的元组



#### 4.5.4 拓展

```python
# 拓展
len((1,2,3))    # 3
(1,2,3)+(4,5,6)   # (1,2,3,4,5,6)
('xiao')*2    # ('xiao','xiao')
3 in (1,2,3)  # True
for i in (1,2,3): print(i)    # 1 2 3
    
max(t)   # 求最大
min(t)   # 求最小
```





### 4.6 字典

**==支持for循环==**



#### 4.6.1 创建

```python
d = {}   		# 空字典
d = dict()   	# 空字典
```

```python
d = {'name':"小政",'age':'22'}

d = {'a':1 , 
     '2023':[4,10], 
     100:('hello','world')
     }

d = dict('name'='小政','age'='22')

d = dict(zip(['name','age'],['小政',22]))
```

```python
d.fromkeys(seq,value)   # 列表  值          #  d.fromkeys(list,10)
```

```python
# 转换
d = dict([(),()])
d = dict([[],[]])
d = dict(((),()))
d = dict(([],[]))
```



#### 4.6.2 增加

```python
# 增
d1.update(d2)   # 字典合并。d2的键值对添加到d1
d.update({'xiaozheng':21})

d[key] = value   # 添加键值对
d.copy()   # 复制
```



#### 4.6.3 删除

```python
# 删
del d   # 删除字典
del d[key]   # 删除指定元素
d.pop(key)   # 删除指定元素
d.popitem()  # 删除最后一个元素，并且以元组形式返回。     # ('age',22)
d.clear()    # 清空字典
```



#### 4.6.4 更改

```python
# 改 
d[key] = value
```



#### 4.6.5 查找

```python
# 查
d['name']    # '小政'
d.get(key)   # 获取指定键对应的值。键不存在不报错。
d.setdefault(key,value)   # 获取指定键对应的值。键不存在添加值。

d.values()   # 获取所有键对应的值。列表形式。
d.keys()     # 获取所有键。列表形式。
d.items()    # 遍历字典。[(键,值),(键,值),(键,值)]
```



#### 4.6.6 拓展

```python
# 拓展
len(d)   # 键的个数

# 当键为整数时
max(d)  # 键的最大值
min(d)  # 键的最小值
```



### 4.7 集合

**==无序、任意数量元素、不允许重复元素、可修改、支持for循环==**

#### 4.7.1 创建

```python
s = set()   # 空集合
```

```python
s = {'xiao','zheng'}
s = {1,2,3,4,5}
s = set('abcdef')   # {'a','b','c','d','e','f'}
```

```python
# 过滤效果
ls = [1,2,3,3,4,5]
s = set(ls)
```

> 集合中的元素**只能**包括 **数值、字符串、元组** 等不可变元素
>
> **不能**包括 **列表、字典、集合**



#### 4.7.2 增加

```python
# 增
s.add(100)    			# 添加元素 （会去重）
s.update([100,200])   	# 添加序列
```



#### 4.7.3 删除

```python
# 删
s.remove('3')   	# 删除3，不存在则报错
s.pop()   			# 随机取出一个元素，原集合改变
s.discard(3)  		# 删除3，不存在不报错
s.clear()   		# 清空
del s				# 删除集合
```



#### 4.7.4 拓展

```python
# 拓展
len(s)   # 集合元素个数
'xiao' in set_name
'xiao' not in set_name
```



#### 4.7.5 集合间运算

```python
# 差集运算
S-T

# 交集运算
S&T

# 补集运算
S^T

# 并集计算
S|T
```

![集合间运算](D:\Typora\picture\image-20221221193550502.png)









## 5 流程控制

### 5.1 顺序结构

```txt
自上而下，逐行执行。
```



### 5.2 选择结构

#### 5.2.1 if

```python
if 表达式:
    语句块
```

#### 5.2.2 if-else

```python
if 表达式:
    语句块1
else:
    语句块2
```

#### 5.2.3 if-elif-else

```python
if 表达式1:
    语句块1
elif 表达式2:
    语句块2
[elif 表达式m:
    语句块m]
else:
    语句块
```

#### 5.2.4 if 嵌套

```python
if 表达式1:
    语句块
    if 表达式2:
        语句块
    else:
        语句块
else:
    语句块
```

#### 5.2.5 三元操作符

```python
a = x if 某条件成立 else y
```



### 5.3 循环结构

#### 5.3.1 for循环

```python
for 循环变量 in 序列:
    语句块
```

> range() ：内置函数。该函数可以创建一个整数列表，一般用在for循环中
>
> range(start, stop[, step])

> **拓展**
>
> ```python
> for index,key in enumerate(seq):
>  print('seq[{0}] = {1}'.format(index,key))
> ```

#### 5.3.2 while循环

```python
while 表达式:
    语句块
```

#### 5.3.3 含else

```python
for 循环变量 in 序列:
    语句块1
else:
    语句块2
```

```python
while 表达式:
    语句块1
else:
    语句块2
```

> else在**穷尽列表**或**条件变为False**导致循环终止时被执行。
>
> 但循环被break终止，else子句不执行。

#### 5.3.4  break和continue语句

```python
break      # 跳出循环体
continue   # 结束本次循环，开始下次循环
```

#### 5.3.5 pass语句

```python
for i in range(5):
    pass   # 空语句
```



### 5.4 推导式

“精简”版的for循环，称为推导式（comprehensions，又称解析式）

> 能够非常简洁的按照某种规则，以一个数据序列为基础，推导出另一个新的数据序列 

#### 5.4.1 列表推导式

列表推导式总共以下有两种形式：

1. [exp1 for x in data if condition]
2. [exp1 if condition else exp2 for x in data]

此处if…else主要起赋值作用。

```python
[生成表达式 for 变量 in 序列或迭代对象]
```

> ```python
> # 过滤原始序列中不符合条件的元素
> ls = [1,'4','a',0.5,"xiaozheng"]
> result = [ e**2 for e in ls if type(e) == int ]
> ```

> ```python
> # 使用列表推导式实现嵌套列表的平铺
> ls = [1,'4','a',0.5,"xiaozheng"]
> result = [ e**2 for e in ls if type(e) == int ]
> ```

```python
# 列表推导式
ls = [i for i in range(10)]
ls = [i for i in range(0,10,2)]
ls = [i for i in range(10) if i % 2 == 0]
ls = [(i,j) for i in range(1,3) for i in range(3)]
```

#### 5.4.2 字典推导式

```python
# 字典推导式
d = {i: i**2 for i in range(1,5)}
d = {list1[i]: list2[i] for i in range(len(list1))}
c = {key: value for key, value in counts.items() if value >= 200}
```

> ```python
> # 例子
> d = {'a':10,'b':20,'A':30,'c':40}
> {key.lower():d.get(key.lower(),0)+d.get(key.upper(),0) for key in d.keys()}
> -----------------------------------------------------
> {'a': 40, 'b': 20, 'c': 40}
> ```

#### 5.4.3 集合推导式

```python
# 集合推导式
s = {i ** 2 for i in list1}
```



## 6 模块

### 6.1 导入模块

```python
[from 模块名] import [模块| 类 | 变量 | 函数 | * ] [as 别名]
```

> 写在开头部分

> 使用 from 好处：
>
> * 减少了对象的查询次数
> * 提高了访问速度
> * 减少了用户的代码输入量

### 6.2 自定义模块

```python
# 文件名1.py

__all__ = ['test1']

def test1(a,b):
    print(a+b)
    
def test2(a,b):
    print(a-b)
 
if __name__ = '__main__'
    test1(3,2)             # 把不想被第三方模块执行的代码‘保护起来’
    
# 文件名2.py
import 文件名1
from 文件名1 import *    

文件名1.test(10,20)
```

### 6.3 模块的搜索路径

```python
import sys
sys.path
home_dir = '/home/用户名/package'
sys.path

%run calculate.py
```





## 7 包

### 7.1 创建包

就是一个文件夹，只是里面必须有`__init__.py`

> 存在的意义就是告知Python解释器，当前文件夹被标记为一个包

```python
# __init__.py			# 文件夹T
__all__ = ['test1']   # 一次性批量导入（2）
```

```python
# test1.py			# 文件夹T
def test1(a,b):
    print(a+b)
```

```python
# test2.py			# 文件夹T
def test2(a,b):
    print(a-b)
```

```python
# test.py
import T.test1 as t1
import T.test2 as t2
t1.test1(10,20)    # （2）


from T.test1 import test1
test1(10,20)
```

### 7.2 导入包

```python
#导入包
import 包名.模块名
from 包名 import *

包名.模块名.目标
```

### 7.3 安装第三方包

```linux
pip install 包名称
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple 包名称
```





## 8 函数

>  函数：组织好的、可重复使用的、用来实现特定功能的代码块

使用函数的好处：

+ 将功能封装在函数内，可供随时随地地重复利用

+ 提高代码的复用性，减少重复代码，提高开发效率

  

### 8.1 函数的定义

```python
def 函数名([参数列表]):
    ''' 函数文档注释 '''
    函数体
    [return [返回值]]
```

> 即使没参数，小括号也不能省。否则报错**invalid syntax**

> 形参列表：用于指明改参数可以接收多少个参数。多个参数，“,”分隔

```python
def 函数名(形参,形参=n):
    语句块
```

> 指定默认值的形参必须放在所有形参的最后

### 8.2 函数返回多个值

> 返回一个值 ，也可以返回多个值    
>
> ```python
> def demo():
> 	return 1,'xiao',True
> 
> x,y,z = demo()   # 1,'xiao',True
> ```
>
> 函数体在遇到return后就结束了，所以写在return后的代码不会执行
>
> 默认返回None

> 对于元组而言，逗号甚至比那对括号更具有身份象征意义。在Python语法上，为了书写方便，去掉包裹元素的圆括号而仅保留逗号也能定义一个元组。根据这样的规定，上面代码返回实际上是一个元组。
>
> 说是返回一个元组，实际上，返回的是元组的引用（即它在内存中的编号）

### 8.3 函数文档的构建

> 在函数的定义中，常利用多行注释给函数写文档，称为函数文档。

> 为Python代码写文档：
>
> 1. 增强程序的可读性和可用性
> 2. 是非常重要的
> 3. 是程序员的专业化素养

```python
def xiaozheng():
    '''
    这是一个函数
    :return: None
    '''
```

```python
# help()   查看函数文档
help(xiaozheng)
-------------------------------------------------
Help on function xiaozheng in module __main__:

xiaozheng()
    这是一个函数
    :return: None
```

```python
# 函数名.__doc__   查看函数文档
print(xiaozheng.__doc__)
-------------------------------------------------
    这是一个函数
    :return: None
```

> 在Ipython中：
>
> * `函数名?` ：可以输出函数的签名及帮助文档
> * `函数名??` ：可以查看该函数的源代码



### 8.4 函数的调用

```txt
[变量] = 函数名([实参])
```

> 定了多少个形参，就要传多少个实参，且顺序一致



### 8.5 参数传递

参数传递方式有两种：

* 值传递：适用于实参类型为不可变类型（字符串，数字，元组）
* 引用传递：适用于实参类型为可变类型（列表，字典）

> 严格说是：传递不可变对象 和 传递可变对象

在python中，类型属于对象，变量是没有类型的。

#### 8.5.1 关键字传参

```python
# 关键字传参
def demo(name,age,gender):
    print(f'姓名：{name}，年龄：{age}，性别：{gender}')

demo('xiaozheng','22','男')
demo(name="xiaozheng",gender='男',age='22')     # 顺序可以改变
```

```python
# 命名关键字参数
def demo(name,*,age,sex):    # *后面的被视为关键字
    pass

demo('小政',age=22,sex='男')   # 传不够会报错
```

#### 8.5.2 默认参数

```python
# 缺省参数
def demo(name,age,gender='男'):      # 默认值参数放最后
    print(f'姓名：{name}，年龄：{age}，性别：{gender}')

demo('xiaozheng','22','男')
demo('xiaozheng','22')      # 默认值参数可以省
```

> **函数名.__defaults\_\_**
>
> ```python
> demo.__defaults__       # 查看某个函数中参数的默认值
> ```

> * 在定义默认参数时，务必要让这个默认参数是 **不可变对象** （比如数值型、字符串型、不可变集合、None、元组）

#### 8.5.3 不定长参数

```python
# 不定长参数（位置传递）
def demo(*args):       # 一个星号     【字符串、列表、元组】
    print(args)

# 所有参数都被args收集，根据位置合并为一个元组。
demo('xiaozheng','22','男')        # ('xiaozheng', '22', '男')

# 列表传入
ls = ['xiaozheng','22','男']       # ('xiaozheng', '22', '男')
demo(*ls)

# 元组传入
t = ('xiaozheng','22','男')        # ('xiaozheng', '22', '男')
demo(*t)
```

```python
# 不定长参数（关键字传递）
def demo(**kwargs):       # 两个星号   【键值对、字典】
    print(kwargs)
    
# 参数是“键=值”形式，都被kwargs接收，组成字典
demo(name="xiaozheng",gender='男',age='22')       # {'name': 'xiaozheng', 'gender': '男', 'age': '22'}

# 字典传入
d = {'name': "xiaozheng", 'gender': '男', 'age': '22'}   # {'name': 'xiaozheng', 'gender': '男', 'age': '22'}
demo(**d)
```

#### 8.5.4 参数序列的打包与解包

```python
num = 1, 2, 3, 4, 5    # 打包
a, b, c, d, e = num    # 解包
print(a, b, c, d, e)   # 1 2 3 4 5
```

```python
def demo(a, b, c, d, e):
    print(a, b, c, d, e)

ls = [1, 2, 3, 4, 5]
demo(*ls)    # 前面加*可以解包
```

```python
def demo(a, b, c, d, e):
    print(a, b, c, d, e)

dic = {'a':1, 'b': 2, 'c':3, 'd':4, 'e':5}
demo(**dic)    # 前面加**可以对字典解包
```

### 8.6 传值与传引用

* 传值（pass-by-value）

  > 形参和实参存在于不同的地址空间，它们是不同的对象，除了参数赋值那一刻短暂的“邂逅”，之后他们独来独往，互不干扰

* 传引用(pass-by-reference)

  > 在引用传递过程中，被调用函数的形参就是实参变量的地址

```txt
Python中所有的函数参数传递，统统都是基于传递对象的引用进行的

因为在Python中，一切皆对象。

而传对象，实质上传的是对象的内存地址，而地址即引用。
```

* 如果参数传递的是可变对象，传递的就是地址，形参的地址就是实参的地址
* 如果参数传递的是不可变对象，为了维护他的“不可变”属性，函数内部不得不“重构”一个实参副本。此时实参的副本（即形参）和主调用函数提供的实参在内存中分处于不同的位置，因此对函数形参的修改，并不会对实参造成任何影响，在结果上看起来和传值一样。





### 8.7 函数的嵌套

```python
def one():
    print('---开始1----')
    print('one')
    print('---结束1----')
def two():
    print('---开始2----')
    one()
    print('---结束2----')

two()
```

### 8.8 函数的递归

```python
def test(num):
    if num == 1:
        result = 1
    else:
        result = test(num - 1) * num
    return result

print(test(5))
```



### 8.9 变量的作用域

#### 8.9.1 局部变量

* 在函数内定义的变量称为局部变量

* 它只在函数内部有效，当函数被调用完毕后，该变量就不存在了。

#### 8.9.2 全局变量

* 在函数外定义的变量称为全局变量

* 它在整个代码中都有效，无论在函数内使用，还是在函数外使用

#### 8.9.3 global

```python
# 在函数内修改全局变量
s = "小政加油"
def demo():
    global s
    s = '小政好帅'
    print(s)
    
demo()   # 小政好帅
```

#### 9.2.4 nonlocal

```python
# 在函数作用域中修改嵌套作用域中的变量
def one():
    count = 1
    def two():
        nonlocal count
        count = 2
    two()
    print(count)

one()   # 2
```



### 8.10 函数式编程的高阶函数

#### 8.10.1 lambda表达式

**==匿名函数==**

```python
lambda 参数: 语句块
```

> 没有函数名，且代码只能写成一行。

**匿名函数有名**

> ```python
> s = lambda a,b :a+b
> s(2,4)    # 6
> ```



#### 8.10.2 filter() 函数

**==过滤器==**

```python
filter(function,sequence)
```

> 序列或支持迭代的容器迭代器sequence中的每个元素都进行function的筛选，返回True的元素

> 返回一个迭代器对象，该对象并不能直接使用，需要使用内置函数list()将其转换成列表，然后再正常输出

> 例子
>
> ```python
> def fun(variable):
>  letters = ['a','e','i','o','u']
>  if(variable in letters):
>      return True
>  else:
>      return False
>  
> sequence = ['a','b','c','d','e','f','g','h','j']
> filtered = filter(fun,sequence)
> list(filtered)          # ['a', 'e']
> ```
>
> ```python
> # 还可以用lambda表达式来描述
> ls = [2,4,6,1,18,9,27,12]
> data = filter(lambda x : x%3==0,ls)
> list(data)   # [6, 18, 9, 27, 12]
> ```





#### 8.10.3 map() 函数

```python
map(function,sequence)
```

> 遍历序列sequence，对序列每个元素都进行函数function操作，返回新序列
>
> function：映射函数
>
> sequence：一个或多个可迭代的序列

> Python中的for循环效率不高，而通过map()函数实现相同功能时效率要高很多

> 例子
>
> ```python
> def f(n):
>  return len(n)
> 
> s = map(f,('xiao','zheng','666'))
> list(s)     # [4, 5, 3]
> ```



#### 8.10.4 reduce() 函数

```python
reduce(function,iterable[,initializer])
```

> function：实现特定规约功能的函数，他是一个二元函数
>
> iterable：可迭代数据对象
>
> initializer：可选项。规约操作时可能用到的初始参数

> 例子
>
> ```python
> from functools import reduce
> 
> reduce(lambda x,y:x+y,[1,2,3,4,5])   # 15
> ```



#### 8.10.5 sorted() 函数

==排序==

```python
ls = [-1,6,9,3,-5,-4,8,-6,2,7]
sorted(ls)    				# [-6, -5, -4, -1, 2, 3, 6, 7, 8, 9]	# 顺序
sorted(ls,reverse=True)  	# [9, 8, 7, 6, 3, 2, -1, -4, -5, -6]    # 逆序
sorted(ls,key=abs)      	# [-1, 2, 3, -4, -5, 6, -6, 7, 8, 9]   	# 绝对值排序
```

> 不影响原列表顺序







# 二、Python面向对象



## 1 面向对象程序设计

面向对象程序设计有三大特征：封装性、继承性、多态性

* 面向过程编程（Procedure Oriented Programming,  OPO）

  > 程序 = 算法 + 数据结构

* 面向对象程序设计（Object Oriented Programming,  OOP）

  > 程序 = 对象 + 消息传递
  >
  > 对象 = 数据 + 方法
  >
  > 程序 = 对象 + 消息传递 = （数据 + 方法）+ 消息传递

### 1.1 类和对象

```python
# 类
class 类名:
    类的属性
    类的方法
```

> 类名：名字（满足**大驼峰命名法**[^1]）
>
> 属性：特征
>
> 方法：行为



```python
# 对象
对象名 = 类名()
对象名.新的属性名 = 值
```

> 点操作符“.”对应的应为是“dot”，通常’t‘的发音弱化，因而读成“[dɔ:]”，而他的发音很接近汉语中的“的”。
>
> 此外，“的”在含以上也有“所属”的意思。
>
> 因此将点操作符读成“的”，音和意皆有内涵。

> 类是封装对象属性和行为的载体。具有相同属性和行为的实体被抽象为类。
>
> * [数据成员]: 在类中定义的变量（属性）
>
>   * [类属性]:定义在类中，但在方法外
>
>   * [实例属性]:定义在类的方法中
>
> * [方法成员]: 类中的定义函数

[^1]: 每一个单词的首字母大写，单词与单词之间没有下划线



> 例子
>
> ```python
> class Car:
>  def move(self):
>      print("车在奔跑")
> 
>  def toot(self):
>      print("车在鸣笛")
> 
> 
> jeep = Car()
> jeep.color = '黑色'
> jeep.move()
> jeep.toot()
> print(jeep.color)
> 
> print(jeep)   
> addr = id(jeep)	   # 打印对象 <__main__.Car object at 0x16进制内存地址>
> print("%d"%addr)   # 10进制
> print("%x"%addr)   # 16进制
> ```

> **类的设计：**
>
> * 名词提炼法：分析整个业务流程，看出现的名词
>
> * 对象的特征描述：属性
>
> * 对象具有的行为（动词）：方法
>
>   [^注意]: 需求中没有设计的属性或者方法在设计类时，不需要考虑

> 在计算机中，通常使用16进制表示内存地址
>
> * 10进制和16进制都是用来表达数字的，只是表达的方式不一样
> * 10进制和16进制的数字之间可以来回转换



### 1.2 构造方法

固定名称：`__init__()`

当创建类的实例的时候，系统会自动调用构造方法，从而实现类进行初始化的操作

```python
def __init__(self):
    self.name = '小政'    # 在初始化方法内部定义属性
    
demo = Demo()
-----------------------------------  
def __init__(self,name,color):
    self.name = name     # 初始化的同时设置初始值
    self.color = color
    
demo = Demo(name,color)
```



### 1.3 析构方法

固定名称：`__del__()`

当删除一个对象来释放类所占用资源的时候，python解释器会调用析构方法

```python
def __del__(self):
    print("析构方法")       # 程序结束的时候执行

demo = Demo()       

del demo   #  手动释放空间（立即执行，不再自动回收）
```

> **生命周期**
>
> * 一个对象从调用 `类名()` 创建，生命周期开始
> * 一个对象的 `__del__` 方法一旦被调用，生命周期结束
> * 在对象的生命周期内，可以访问对象属性，或者让对象调用方法



### 1.4 self

方法的定义中，第一个参数永远是`self`

self：也就是this指针。

> 哪一个对象调用的方法，self就是哪一个对象的引用



### 1.5 访问权限

* 保护型成员，单下划线开头（protected）

  > _foo
  >
  > 保护型成员只允许在本类和子类进行访问

* 私有成员，双下划线开头（private）

  > __foo
  >
  > 私有成员理论上只允许在定义该方法的类中进行访问，并且也不能通过类的实例直接访问，
  >
  > 但是可以通过“ **类的实例名._类名__属性名** ”的方式进行访问

  > **伪私有属性和私有方法**
  >
  > ```python
  > class Demo:
  >  def __init__(self):
  >      self.name = '小政'
  >      self.__age = 22  # 私有属性
  > 
  >  def __str__(self):
  > 		return f'{self.name}今年{self.__age}岁'  # 内部可以访问
  > 
  >  def __provid(self):   # 私有方法
  >  	print('我是私有的，你访问不到我')
  > 
  > 
  > demo = Demo()
  > print(demo)
  > # demo.__provid()   # 私有属性在外界不能被直接访问
  > demo._Demo__provid() # 可以前面加_类名的方式访问
  > # print(demo.__age)
  > print(demo._Demo__age)
  > ```

  > 【继承】
  >
  > * 子类对象不能直接访问父类的私有属性或私有方法
  > * 子类对象可以通过父类的公有方法间接访问

* 属性定义的名字，首尾双下划线

  > 表示定义的特殊方法，一般是系统定义的名字



### 1.6 魔术指令

#### 1.6.1 \_\_str\_\_

在开发中，希望使用print输出对象变量时，能打印自定义内容

```python
class Dog:

    def __str__(self):
        return "小狗汪汪叫"      # 必须要返回一个字符串

dog = Dog()
print(dog)  

# <__main__.Dog object at 0x0000015531C73820>
# 小狗汪汪叫
```

> 必须要返回一个字符串



### 1.7 生成器与迭代器

#### 1.7.1 生成器

* 在Python语言中，这种一边循环一遍计算的机制，称为 **生成器（generator）**

```python
# 生成器的定义
a = (x**2 for x in range(10) if x % 2 == 0)
print(a)     # <generator object <genexpr> at 0x0000024BD52D9120>
type(a)      # generator
```

```python
# 生成器的使用
next(a)         # 全局函数 
a.__next__()    # 内置函数

for num in a:   # 循环
    print(a)
```

> 当我们不断执行next(a)时候，它会不断的输出a的下一个元素，直到没有更多的元素输出时，它会抛出StopIteration异常
>
> 使用和循环，确保访问不会越界，因此不会发生StopIteration异常

> 例子
>
> ```python
> # 生成斐波那契数列的生成器
>  n, a, b = 0, 0, 1
>  while n < xterms:
>      yield b           # 表明这是一个生成器 
>      a, b = b, a + b
>      n = n + 1
>  return "输出完毕"
> 
> func = fibonacci(10)
> ```
>
> > **yield**：生产、产出。
> >
> > 如果某个函数定义中包含yield关键字，那么这个函数就不一般了，它不再是一个普通的函数，而是一个生成器。

* **生成器的最佳应用场景**：

  > 我们不想将所有计算出的大量结果一块保存到内存之中。

* **生成器的执行流程**

  > 生成器的函数，在每次调用next()的时候执行，遇到yield语句就“半途而废”，再次执行时，就会从上次返回的yield语句处接着往下执行。

  ```python
  
  ```

  



#### 1.7.2 迭代器

* 存储数据的容器（container）
* **迭代：**操作这些容器时，我们常需要逐个访问其中的元素，这种逐个获取容器中元素的过程，就叫迭代（iteration）







### 1.8 封装

* 将属性和方法封装到一个抽象的类中
* 外界使用类创建对象，然后让对象调用方法
* 对象方法的细节都被封装在类的内部

> * 在对象的方法内部，是可以直接访问对象的属性的
>
> * 同一个类创建的多个对象之间，属性互不干扰
>
>   （每创建一个对象，就会开辟一个空间一个内存地址）

```python
# 家具类
class HouseItem:
    def __init__(self, name, area):
        self.name = name
        self.area = area

    def __str__(self):
        return f"{self.name}占地{self.area}平米"

# 房子类
class House:
    def __init__(self, house_type, area):
        self.house_type = house_type
        self.area = area
        self.free_area = area
        self.item_list = []

    def __str__(self):
        return (f'户型：{self.house_type}'
                f' 总面积：{self.area}'
                f' 剩余面积：{self.free_area}'
                f' 家具名称列表：{self.item_list}')

    def add_item(self, item):
        if self.free_area < item.area:
            print(f"面积不够了,{item.name}添加失败")
            return
        self.item_list.append(item.name)
        self.free_area -= item.area

# 构建家具
bed = HouseItem("席梦思", 4)
chest = HouseItem("衣柜", 2)
table = HouseItem("餐桌", 1.5)
print(bed, chest, table)
# 构建房子并添加家具
house = House("两室一厅", 7)
house.add_item(bed)
house.add_item(chest)
house.add_item(table)
print(house)
```

> * 在定义属性时，如果 **不知道设置什么初始值**，可以设置为**None**
> * 在 **封装的** 方法内部，还可以让 **自己的** **使用其他类创建的对象属性** 调用已经 **封装好的方法** 



### 1.9 继承

**继承**：**子类** 拥有 **父类** 的所有 **方法** 和 **属性**

**派生：**在己有类的基础上新增自己的特性，继而产生新类的过程

**基类（Base Class）、超类（Super Class）、父类（Parent Class）：**己有的类

**派生类（Derived Class）、子类（Subclass）：**派生出来的新类

> * 继承的目的在于实现代码重用，即对于己有的、成熟的功能，令子类从父类处奉行”拿来主义“。
> * 派生的目的在于当新的问题出现且原有代码无法解决或不能完全解决时，需要对原有代码进行全部或部分改造



#### 1.9.1 单继承

```python
class 子类(父类名):
    pass
```

**继承的传递性**

> * 子类可以继承父类，子类的子类也可以继承父类

**单一继承**

> ```python
> class Person:
>  height = 140
> 
>  def __init__(self, name, age, weight):
>      self.name = name
>      self.age = age
>      self.__weight = weight
> 
>  def sepeak(self):
>      print(f'{self.name}   {self.age}   {self.__weight}  {Person.height}')
> 
> 
> class Student(Person):
>  grad = ""
> 
>  def __init__(self, name, age, weight, grad):
>      Person.__init__(self, name, age, weight)
>      self.grade = grad
> 
>  def speak(self):
>      print(f'{self.name}   {self.age}    {self.grade}')
> 
> 
> stu = Student('小政', 22, 60, 3)
> stu.speak()            #  小政   22    3
> ```



#### 1.9.2 多继承

```python
class 子类名(父类名1,父类名2...):
    pass
```

> 【注意事项】    **不推荐使用**
>
> 如果是不同父类的中存在同名方法，先继承谁就用谁的方法
>
> ```python
> class Father_one:
>  def d1(self):
>  	print('Father_one------d1')
>  def d2(self):
>  	print('Father_one------d2')
> 
> class Father_two:
>  def d1(self):
>  	print('Father_two------d1')
>  def d2(self):
>  	print('Father_two------d2')
> 
> class Son(Father_one, Father_two):      # one在前，用它
> 	pass
> 
> son = Son()
> son.d1()
> son.d2()
> print(Son.__mro__)   # mro
> ---------------------------------------------------------
> Father_one------d1
> Father_one------d2
> (<class '__main__.Son'>, <class '__main__.Father_one'>, <class '__main__.Father_two'>, <class 'object'>)
> ```

**python中的 MOR——方法搜索顺序**

> ```python
> print(对象.__mro__)
> ```
>
> * 从左往右的顺序查找
> * 如果在当前类中，找到方法，就立即执行，不再搜索
> * 没有找到就查找下一个类
> * 都找完了，还没有找到，程序报错



#### 1.9.2 方法的重写（覆盖）

父类的方法不能满足子类的需求，就需要在子类中从新编写一下父类的方法实现

```python
class Animal:            # 父类
    def eat(self):
        print("吃饭")

class Dog(Animal):    # 子类
    def jiao(self):
        print("汪汪汪汪汪……")

class XiaoDog(Dog):   # 子类的子类
    def jiao(self):   # 重写父类的jiao方法
        print("嗷呜嗷呜嗷呜……") 

xiaodog = XiaoDog()
xiaodog.jiao()  # 嗷呜嗷呜啊呜
```

> 如果子类中，重写了父类的方法
>
> 在使用子类对象调用方法时，会调用子类中重写的方法



#### 14.7.3 super()

**【对父类方法进行扩展】**

```python
class Animal:    # 父类
    def eat(self):
        print("吃饭")

class Dog(Animal):  # 子类
    def jiao(self):
        print("汪汪汪汪汪……")

class XiaoDog(Dog):  # 子类的子类
    def fly(self):  # 子类自己的新方法
        print('我是神狗我会飞')
        
    # 重写父类的方法
    def jiao(self):  
        # 针对子类特有的需求，编写代码
        print("巴啦啦能量")
        # 使用super().调用原本在父类中封装的方法
        super().jiao() 
        # Dog.jiao(self)    # 2.0老方法
        # 增加其他子类代码
        print("@##@#@#/**@@")

xiaodog = XiaoDog()
xiaodog.jiao()  
---------------------
巴啦啦能量
汪汪汪汪汪……
@##@#@#/**@@
```

> 【python2.0老方法】   **不推荐使用**
>
> ```python
> 父类名.方法(self)
> ```
>
> * 一定是**父类名调用方法**
> * 若是写成了**当前子类名**调用方法，就会**形成递归调用，进入死循环。**



#### 14.7.4 父类的私有属性和私有方法

1. **子类对象** **不能** 在自己的方法内部，**直接** 访问 父类的 **私有属性** 或 **私有方法**
2. **子类对象** 可以通过 **父类** 的 **公有方法** **间接** 访问到 **私有属性** 或 **私有方法**

> * **私有属性、方法** 是对象的隐私，不对外公开，**外界** 以及 **子类** 都不能直接访问
> * **私有属性、方法** 通常用于做一些内部的事情

```python
class Father:
    def __init__(self):
        self.name = "小政"
        self.__age = 22  # 私有属性
    def __test(self):   # 私有方法
        print("父类的私有方法")
   
    # 父类写一个公有方法，里面写入私有属性和私有方法
    def test(self):
        print(self.name, self.__age) 
        self.__test()  

class Son(Father):
    def demo(self):
        # print(self.name, self.__age)     # 无法调用父类的私有属性
        # self.__test()     # 无法调用父类的私有方法
        self.test()  # 调用到了父类的私有属性和私有方法

son = Son()
son.test()
```



> * 



#### 14.7.6 新式类与经典类

> `object` 是 `Python` 为所有对象提供的 **基类**，提供有一些内置的属性和方法，可以使用 `dir` 函数查看

* **新式类**：以 `object` 为基类的类，**推荐使用**
* **经典类**：不以 `object` 为基类的类，**不推荐使用**

* 在 `Python 3.x` 中定义类时，如果没有指定父类，会 **默认使用** `object` 作为该类的 **基类** —— `Python 3.x` 中定义的类都是 **新式类**
* 在 `Python 2.x` 中定义类时，如果没有指定父类，则不会以 `object` 作为 **基类**

> **新式类** 和 **经典类** 在多继承时 —— **会影响到方法的搜索顺序**

为了保证编写的代码能够同时在 `Python 2.x` 和 `Python 3.x` 运行！
今后在定义类时，**如果没有父类，建议统一继承自 `object`**

```python
class 类名(object):
    pass
```



### 1.10 多态

**面向对象三大特性**

1. **封装** 根据 **职责** 将 **属性** 和 **方法** **封装** 到一个抽象的 **类** 中
   * 定义类的准则 
2. **继承** **实现代码的重用**，相同的代码不需要重复的编写
   * 设计类的技巧 
   * 子类针对自己特有的需求，编写特定的代码
3. **多态** 不同的 **子类对象** 调用相同的 **父类方法**，产生不同的执行结果
   * **多态** 可以 **增加代码的灵活度**
   * 以 **继承** 和 **重写父类方法** 为前提
   * 是调用方法的技巧，**不会影响到类的内部设计**

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def game(self):
        print(f'{self.name}在地上蹦蹦跳跳')


class XiaoDog(Dog):
    def game(self):
        print(f'{self.name}飞到了天上')


class Persion:
    def __init__(self, name):
        self.name = name

    def play(self, dog):
        print(f'{self.name}和{dog.name}在玩耍')
        dog.game()


erha = Dog('二哈')
xiao = XiaoDog('哮天犬')
xiaozheng = Persion('小政')
xiaozheng.play(erha)
xiaozheng.play(xiao)
```



### 14.9 类的结构

创建对象分两步

1. 在内存中为对象分配空间
2. 调用初始化方法`__init_`为对象初始化

对象创建好后，内存中有了一个对象实实在在存在（实例）



### 14.10 属性

#### 14.10.1 类属性

```python
# 类属性
类属性名 = 属性值
```

> **类属性** 就是针对 **类对象** 定义的属性
>
> * 使用 **赋值语句** 在 `class` 关键字下方可以定义 **类属性**
> * **类属性** 用于记录 **与这个类相关** 的特征

【**类属性**】

```python
class Demo():
    count = 0  # 类属性
    def __init__(self, name):
        self.name = name  # 实例属性
        Demo.count += 1  # 类名.类属性
        
d1 = Demo('one')
d2 = Demo('two')
d3 = Demo('three')
print(d1.count)   # 对象.类属性
print(d3.count)
print(Demo.count) # 类名.类属性
```

* 类属性就是给类对象中定义的属性
* 通常从来记录与这个类相关的特征
* 类属性不会用于记录具体对象的特征

【**获取类属性**】

> 存在**向上查找机制。**
>
> * 首先在对象内部查找对象属性
> * 没有找到就会向上寻找类属性
>
> 访问类属性的方式
>
> 1. **类名.类属性**
> 2. 对象.类属性（不推荐）
>
> ```python
> # 对象.类属性（不推荐的原因）
> class Demo():
>     count = 0  # 类属性
>     def __init__(self, name):
>         self.name = name
>         Demo.count += 1  # 类名.类属性
>         
> d1 = Demo('one')
> d2 = Demo('two')
> d3 = Demo('three')
> d3.count = 99   
> print(d3.count)   # 对象.类属性  99
> print(Demo.count) # 类名.类属性   3
> ```
>
> > 原因是d3.count = 99执行会在d3里面找有没有count这个属性，没有这个属性就会创建一个这个属性，并赋值为99。

#### 14.10.2 实例属性



### 14.11 方法

类方法、静态方法、实例方法

#### 14.11.1 类方法

```python
@classmethod
def 类方法名(cls):
    pass
```

> **类方法** 就是针对 **类对象** 定义的方法
>
> * 在 **类方法** 内部可以直接访问 **类属性** 或者调用其他的 **类方法**
>
> ```python
> class Tool:
>     count = 0   # 类属性
> 
>     @classmethod  # 修饰器
>     def test(cls): # 类方法
>         print(cls.count) # cls.类属性
> 
>     def __init__(self, name): # 构造方法
>         self.name = name # 实例属性
>         Tool.count += 1 # 类名.类属性
> 
> 
> tool1 = Tool('直尺')
> tool2 = Tool('三角板')
> Tool.test()  # 类名.调用类方法
> ```
>
> 通过 **类名.** 调用 **类方法**，**调用方法时**，不需要传递 `cls` 参数

#### 14.11.2 静态方法

如果这个方法不访问类属性，也不访问实例属性，就可以考虑定义为静态方法。

```python
@staticmethod
def 静态方法名():
    pass
```

> 静态方法的调用不需要实例化对象
>
> ```python
> class Test:
> @staticmethod        # 修饰器
> def happy():        # 不需要参数
> print('今天你微笑了吗？')
> 
> Test.happy()  # 类名.静态方法
> ```

#### 14.11.3 实例方法

不用修饰器修饰的方法





### 14.12 单例

#### 14.12.1 单例设计模式

* **目的** —— 让 **类** 创建的对象，在系统中 **只有** **唯一的一个实例**
* 每一次执行 `类名()` 返回的对象，**内存地址是相同的**

#### 14.12.2 ` __new__`方法

```python
def __new__(cls, *args, **kwargs):
	pass
```

* 创建对象时，解释器首先会调用new方法为对象分配空间
* 是object基类提供的内置的静态方法
* 作用
  * 在内存中为对象分配空间
  * 返回对象的引用
* 解释器获得引用后，作为第一个参数，传递给init方法

`__new__`**方法的重写**

```python
class Test:
    # 重写__new__方法
    def __new__(cls, *args, **kwargs):
        print("创建对象，分配空间")   # 多的内容
        instance = super().__new__(cls)   # 一定要return
        return instance
    def __init__(self):
        print('我执行了吗？')

test = Test()
print(test)
```

> 重写new方法，一定要 `return super().__new__(cls)`
>
> 否则解释器得不到分配的空间的引用对象，就不用调用对象的初始化方法

> new方法是一个静态方法，需主动调用cls参数



#### 14.12.3 单例设计模式

```python
class Test:
    instance = None
    def __new__(cls, *args, **kwargs):
        if cls.instance is None:
            cls.instance = super().__new__(cls)
        return cls.instance

    def __init__(self):
        pass

test1 = Test()
print(test1)
test2 = Test()
print(test2)
```

#### 14.12.4 初始化动作只执行一次

```python
class Test:
    instance = None
    init_flag = False   # 定义一个标记
    def __init__(self):
        if Test.init_flag:  # 如果标记为真直接函数直接结束
            return
        print('I love you')   # 只执行一次
        Test.init_flag = True  # 不为真这个改为真
        
test1 = Test()
print(test1)
test2 = Test()
print(test2)
```





### 9.5 闭包

如果在一个内部函数中对外部函数作用域的变量进行引用，那么内部函数就会被称为闭包

* 存在于**嵌套关系的函数**中
* 嵌套的内部函数**引用了外部函数的变量**
* 嵌套的外部函数会将**内部函数名作为返回值**返回

```python
# 外部函数
def demo_one(a, b):
    c = 100     # 外部函数的变量

    # 内部函数
    def demo_two():
        he = a + b + c     # 调用外部函数的变量
        print(he)

    return demo_two  # 返回内部函数函数名


result1 = demo_one(1, 2)  
result2 = demo_one(20, 60)
print(result1)   # <function demo_one.<locals>.demo_two at 0x000001B43E7DE440>
print(result2)  # <function demo_one.<locals>.demo_two at 0x000001B43E7DE4D0>
result1() # 103
result2() # 180

```



### 9.6 装饰器

#### 9.6.1 封闭开放（不用）

```python
# 把函数名作为参数传入    【封闭开放】
def print_log(func):
    print("函数正在运行中")
    func()

def test():
    print("test")

print_log(test)
```

#### 9.6.2 简单的装饰器

```python
# 简单的装饰器
def wrap(func):
    print("正在装饰")

    def inner():
        print("正在验证权限")
        func()

    return inner


@wrap       # test = warp(test)
def test():
    print("test")
    
test()
```

#### 9.6.3 多个装饰器

```python
# 多个装饰器
def warp_one(func):
    print("正在装饰1")  # 4. 输出

    def inner(): 
        print("正在验证权限1")  # 5. 输出 
        func()

    return inner


def wrap_two(func):
    print("正在装饰2")   # 2. 输出

    def inner():
        print("正在验证权限2")  # 6. 输出
        func()

    return inner


@warp_one     # 装饰器1    # 3. 再执行这个
@wrap_two     # 装饰器2    # 1. 先执行这个
def test():
    print("test")


test()  # 装饰完毕后，程序从上向下的顺序运行
-------------------------------------
正在装饰2
正在装饰1
正在验证权限1
正在验证权限2
test
```

#### 9.6.4 有参数的装饰器

```python
# 两个参数
def warp(func):
    def inner(a, b):
        print('开始验证权限')
        func(a, b)
    return inner

@warp
def test(a, b):
    print('a=%d,b=%d' % (a, b))

test(1, 2)
```

```python
# 多个参数
def warp(func):
    def inner(*args, **kwargs):  # 列表 元组 字典
        print('开始验证权限')
        func(*args, **kwargs) # 列表 元组 字典

    return inner


@warp
def test(*args, **kwargs): # 列表 元组 字典
    print("-" * 20)

test(1, 2, 3)
test(a=1, b=2, c=3)
```

#### 9.6.5 装饰器对带有返回值的参数进行装饰

```python
def close(func):
    def close_in():
        return func()
    return close_in

@close
def test():
    return 'xiao zheng'

result = test()
print(result)
```

9.6.6 带有参数的装饰器

```python
def func_arg(args):
    def func(function_name):
        def fun_in():
            print("dsadsfasfdfdfsafdasf***%s" % args)
            function_name()

        return fun_in

    return func


@func_arg('你好')    # 如果给装饰器添加参数，那么需要增加一层封装，西安传递参数，然后再传递函数名。
def test():
    print('****test****')


test()

```







## 10 异常处理

### 10.1 常见错误

#### 10.1.1 语法错误

也称解析错误。指不遵循语言的语法结构引起的错误，此时程序无法正常编译。

> 在编译型语言中：编译期出现
>
> 在解释型语言中：运行期出现

1. 遗漏了冒号，逗号，括号
2. 关键字拼写错误
3. 缩进不正确
4. pass语句的不正确使用

#### 10.1.2 逻辑错误

也称语义错误。是指程序的执行结果与预期不符。

1. 运算符优先级考虑不周
2. 变量名使用不正确
3. 语句块缩进层次不对
4. 在布尔表达式中出错
5. 算法设计方面的错误

#### 10.1.3 运行时错误

是指程序可以运行，但是在运行过程中遇到的错误，导致意外退出。



### 10.2 异常类



### 10.3 异常处理

#### 10.3.1 捕获异常

```python
# 捕获简单异常
try:
    语句块
except [异常类型]:
    异常处理代码
```

```python
# 完整语句
try:
    # 语句块
except A:
    # 异常A处理代码
except:
    # 其他异常处理代码
else:
    # 没有异常处理代码
finally:
    # 最后必须处理代码
```

```python
# 捕获多个异常
try:
    语句块		# 可能发生异常的代码块
except 异常名称1 as 变量名:		# 变量名存储的是具体的错误信息
    print("捕获到异常，执行except")
except 异常名称2 as 变量名:    # 可以捕获多个异常
    异常处理代码
except Exception as 变量名:   # 万能异常捕获，放最后。
    print(变量名)
else:
    print("没有捕获到异常，执行else")
finally:
    print("无论是否发生异常，都会执行")
    print("一般用来资源回收")
```

> 先执行try
>
> 若try中没发生异常，except不执行，执行else
>
> 若try中发生异常，try剩下的部分被忽略，转而执行except，不执行else
>
> finally无论是否发生异常，都会执行

> 可以有多个except语句，分别用来处理不同的特定异常，而最多只有一个分支被执行



#### 10.3.2 抛出异常

##### 10.3.2.1 raise语句

显式的触发异常

```python
raise [SomeException[,args[,traceback]]]

# raise IndexError("索引下标超出范围")
```

> SomeException：异常类/异常类的实例
>
> args：说明信息（元组）
>
> traceback：提供一个跟踪记录对象

##### 10.3.2.2 assert语句

又称作断言。指期望用户满足指定的条件。

当用户定义的约束条件不满足的时候，会触发**AssertionError**异常

```python
assert 逻辑表达式, data

# assert a!=0, "a的值不能为0"
```

> assert语句用来收集用户定义的约束条件，而不是不住内在的程序设计错误

> ```python
> try:
> s = int(input("请输入你的年龄："))
> assert s > 0, "输入的年龄大于0"
> print(s)
> except Exception as result:
> print('捕捉到的异常：', result)
> ```



### 10.4 自定义异常

```python
class ShortInputException(Exception):
    '''
    自定义异常类
    '''
    def __init__(self, length, atleast):
        self.length = length
        self.atleast = atleast

try:
    text = input("请输入密码：")
    if len(text) < 3:
        # raise引发刚定义的异常
        raise ShortInputException(len(text), 3)
except EOFError:
    print('你输入了一个结束标记')
except ShortInputException as result:
    print("ShortInputException：输入的长度是%d，长度至少应是%d" % (result.length, result.atleast))
else:
    print("没有异常发生")

------------------------
# 请输入密码：12
# ShortInputException：输入的长度是2，长度至少应是3
# 请输入密码：123
# 没有异常发生
```

### 10.5 预定义清理

finally语句：手动释放资源

with语句：预定义清理操作

> 无论资源在使用过程中是否异常发生，都会执行释放资源的操作

#### 10.5.1 with语句

适用于对资源进行访问的场合，确保不管使用过程中是否发生异常都会执行必要的“清理”操作，释放资源。

```python
with 上下文表达式 [as 资源对象]:
    对象的操作

# with open("/data.txt") as file:
#	data = file.read()
```

> 上下文表达式：返回一个上下文管理对象
>
> 资源对象：单个变量、元组
>
> 对象的操作：执行前，调用__ enter __ () 方法；执行后，调用__ exit __()方法

#### 10.5.2 上下文管理器

python2.5开始支持。用于规定某个对象的使用范围，一旦进入或者离开使用范围，会有特殊的操作被调用。

```python
# 上下文管理协议
__enter__(self)		# 进入上下文管理器时调用
__exit__(self,type,value,tb)   # 离开上下文管理器时调用

# 上下文管理器
# 运行时上下文
# 上下文表达式
```

1. 执行上下文表达式，生成一个上下文管理器对象
2. 调用`__enter_()`方法。如果使用as，就把返回值传给资源对象
3. 执行with语句代码块
4. 无论是否有异常，都会执行`__exit_()`。（负责执行程序的“清理”工作）
5. 如果执行过程中没有异常，或者执行了`break`、`continue`、`return`，则以None作为参数调用`__exit_()`。
6. 如果执行过程中出现异常，则会使用`sys.exc_into`得到的异常信息为参数调用`__exit_()`
7. 出现异常时，如果`__exit_()`返回False，则会重新抛出异常，让with之外的语句逻辑来处理异常。
8. 如果返回True，则忽略异常，不再对异常进行处理。



### 10.6 异常的传递性

```python
def demo1():
    a = int(input("请输入一个整数："))

def demo2():
    return demo1()

try:
    print(demo2())
except Exception as result:
    print(f"未知错误：{result}")
```

> 在主程序中增加异常



## 11 文件读写与管理



### 11.1 基础知识

#### 11.1.1 文件编码

* UTF-8

#### 11.1.2 文件打开模式

| 文件打开模式 | 含义                                                         | 注意事项 |
| ------------ | ------------------------------------------------------------ | -------- |
| r            | 只读。指针放开头（默认）                                     |          |
| w            | 只写。文件存在，打开删除开头写；文件不存在，创建写           |          |
| a            | 追加写。文件存在，打开末尾追加写；文件不存在，创建写         |          |
| r+           | 读写。可以读，也可以写入新的（覆盖）                         |          |
| w+           | 读写。打开清空再写                                           |          |
| a+           | 读写。文件存在，打开末尾追加；文件不存在，创建写             |          |
| rb           | 只读。二进制打开。指针放开头。                               |          |
| wb           | 只写。二进制打开。文件存在，打开删除开头写；文件不存在，创建写 |          |
| ab           | 追加写。二进制打开。文件存在，打开末尾追加写；文件不存在，创建写 |          |
| rb+          | 读写。二进制打开。读写                                       |          |
| wb+          | 读写。二进制打开。文件存在，打开删除开头写；文件不存在，创建写 |          |
| ab+          | 追加写。二进制打开。文件存在，打开末尾追加写；文件不存在，创建写 |          |
| t            | 文本文件模式                                                 |          |
| b            | 二进制模式                                                   |          |
| x            | 写模式。新建一个文件（文件不能存在）                         |          |



### 11.2 文件

#### 11.2.1 文件的打开

```python
# 文件的打开
file = open('文件名','访问模式',encoding='编码格式')   # 需要手动关闭
with open('文件名','访问模式',encoding='编码格式') as 别名  # 自动关闭
```

#### 11.2.2 文件的关闭

```python
# 文件的关闭
file.close()
```

#### 11.2.3 文件的读写

```python
# 写文件
file.write('内容')   # 写到内存中
file.fulsh       # 刷新到硬盘中
```

```python
# 读文件
file.read()				# 没参数，一次读完
file.read(size)			# 读size字节（一个汉字算一个字节）
file.readlines()		# 一行一行读，一次读完，返回列表
file.readline()			# 一行一行读，一次一行。返回字符串
for line in file: print(line)   # for循环读一行
```

#### 11.2.4 文件的指针

```python
# 获取指针
file.tell()
```

```python
# 移动指针
file.seek('偏移量'[,'方向'])
```

> 方向：
>
> * SEEK_SET 或 0 ：文件的起始位置（默认）
> * SEEK_CUR 或 1 ： 文件的当前位置
> * SEEK_END 或 2 ：文件的末尾位置
>
> 偏移量：移动的字节数（正负）

#### 11.2.5 文件的重命名和删除

```python
# 重命名
os.rename('老文件名','新文件名')
```

```python
# 删除
os.remove('文件路径/文件名')
```

#### 11.2.6 查看文件状态、文件名、打开模式

```python
# 查看文件状态
file.closed       # True:关闭   False:打开
```

```python
# 查看文件名
file.name
```

```python
# 查看文件的打开模式
file.mode
```



### 11.3  文件夹

```pyton
import os
```

#### 11.3.1 创建文件夹

```python
# 创建文件夹
os.mkdir("文件夹名")
```

#### 11.3.2 获取当前目录

```python
# 获取当前目录
os.getcwd()
```

#### 11.3.3 改变默认目录

```python
# 改变默认目录
os.chdir("路径")
```

#### 11.3.4 获取目录列表

```python
# 获取目录列表
os.listdir("路径")
```

#### 11.3.5 删除文件夹

```python
# 删除文件夹
os.rmdir("文件名")
```



### 11.4 CSV

#### 11.4.1 打开

```python
# 文件的打开
writer = open('文件名','访问模式',encoding='编码格式'，newline="")   # 需要手动关闭 
with open('文件名','访问模式',encoding='编码格式') as 别名  # 自动关闭
```

> newline=“”        写入内容时不要出现空行

#### 11.4.2 关闭

```python
# 文件的关闭
file.close()
```

#### 11.4.3 读写

```python
# 写
csv.writer(csvfile,dialect='excel',**fmtparams)
t = csv.DictWriter(csvfile,fieldnames,restval='',extrasaction='raise',dialect='excel',*args,**kwds)
```

> writer.writerow(row)   # 写入一行数据
> writer.writerows(rows) # 写入多行数据
> writer.dialect   # 返回dialect

```python
# 读
t = csv.reader(csvfile,dialect='excel',**fmtparams)
t = csv.DictReader(csvfile,fieldnames=None,restkey=None,restval=None,dialect='excel',*args,**kwds)
```

> * fieldnames: 指定字段名，如果没有指定，第一行为字段名

> t.dialect   # 返回CSV格式
> t.line_num  # 返回读入的行数

> t.__next__()
> t.dialect
> t.line_num
> t.fieldnames















# 二、常用的内建模块



## 1 collections 模块

> 高性能的数据容器类型

### 1.1 namedtuple

> **加强版元组**

> 生成可以使用名字来访问元素内容的元组子类

```python
from collections import namedtuple

Point = namedtuple('Point', ['x', 'y'])
p = Point(3, 4)
print(p.x)    # 3
print(p.y)    # 4

# isinstance()  可以做到“隔代指认”
print(isinstance(p, Point))   # True    # 对象是否是Point的实例
print(isinstance(p, tuple))   # True    # 对象是否是元组实例  

p[0]   # 3
p[1]   # 4

# 解包
a,b = p
a,b   # (3,4)
```

> 解包：
>
> * 解包是Python的特有属性
>
> * 把一个包含多个元素的对象（如列表、元组等）一次性的赋值给多个简单变量，对象内部的元素会被解开，并按照位置顺序，一一赋值给简单变量

### 1.2 deque

> **双向队列**

```python
from collections import deque

dq = deque(['a','b','c'])

dq.append(1)      	# 最后插入
dq.appendleft(2)   	# 最左侧插入
dq.insert(2,'x')   	# 指定位置插入
dq.pop()       		# 弹出最后一个元素
dq.popleft()   		# 弹出左边第一个元素
dq.remove('x')  	# 删除指定元素 
dq.reverse()   		# 逆序
```

### 1.3 OrdereDict

> 定制版字典——**有序字典**

> 有序字典底层是通过双向链表来实现的，内部通过map()函数对指定字典元素序列做映射，以高效存储键值对

```python
from collections import OrderedDict

od = OrderedDict()
od['a'] = 1
od['b'] = 2
od['c'] = 3
print(od)    # OrderedDict([('a', 1), ('b', 2), ('c', 3)])
list(od.keys())
```

### 1.4 defaultdict

> 如果希望键不存在时能返回一个默认值，就需要使用提供默认的字典类型defaultdict

```python
from collections import defaultdict

dd = defaultdict(lambda: '不存在')
dd['key1'] = 'abc'
print(dd['key1'])   # abc
print(dd['key2'])   # 不存在
```

### 1.5 Counter

> 简易计数器类

```python
from collections import Counter

g = ['小政', '小政', '逍遥震', 'HAUT', 'HAUT', 'HAUT']
result = Counter(g)
print(dict(result))             # {'小政': 2, '逍遥震': 1, 'HAUT': 3}
print(result.most_common(2))    # 返回出现频率最高的2个对象       # [('HAUT', 3), ('小政', 2)]
```





## 2 datetime 模块

> 处理日期和时间的标准库

> 是 date 和 time 模块的截个

### 2.1 获取当前时间

```python
from datetime import datetime

now = datetime.now()
print(now)     # 返回当前时间			 # 2023-04-11 15:56:37.749275
```

```python
from datetime import datetime

date = datetime(2023, 4, 11, 16, 0)
print(date)    # 返回特定时间          # 2023-04-11 16:00:00
```

```python
date.year
date.month
date.hour
date.minute
```

### 2.2 datetime 转换为 timestamp

> epoch time(纪元时间)：1970年1月1日 00:00:00 UTC+00:00

> 我们当前的时间就是相对于纪元时间流逝的秒数，称为timestamp（时间戳）

```python
from datetime import datetime

now = datetime.now()
now.timestamp()    # 1681200000.0      # 浮点数，小数位表示毫秒
```

### 2.4 字符串 转换为 datetime

```python
# 字符串 转 datetime
from datetime import datetime

cday = datetime.strptime('2023-4-11 16:44:00', '%Y-%m-%d %H:%M:%S')
print(cday)
```

strptime（）函数中常见的日期格式

### 2.3 datetime 转换为 字符串

```python
from datetime import datetime

now = datetime.now()
print(now.strftime('%Y'))   # 2023
```

### 2.4 datetime 加减

```python
from datetime import datetime, timedelta

now = datetime.now()
print(now.strftime('%Y-%m-%d %H:%M:%S'))   # 2023-04-11 16:53:36

date = now + timedelta(days=3, hours=2)
print(date.strftime('%Y-%m-%d %H:%M:%S'))  # 2023-04-14 18:53:36
```





## 3 json 模块

> JavaScript Object Notation

> 全部用小写的形式

### 3.1 dumps 与 loads

* json.dumps()：将Python对象序列化为json格式的字符串
* json.loads()：将JSON格式的字符串反序列化为Python对象

```python
import json
dic = {'wo':5,'ai':2,'ni':1}
json_str = json.dumps(dic)    # {"wo": 5, "ai": 2, "ni": 1}
d = json.loads(json_str)      # {"wo": 5, "ai": 2, "ni": 1}
```

### 3.2 dump 与 load

> 如果我们处理的不是字符串，而是文件

```python
with open('data.json','r') as t:
    data = json.load(t)
print(data[0])
```





## 4 random 模块

> 用于生成随机数

```python
import random

random()		# [0,1.0)  随机浮点数
uniform(a,b)   	# [a,b)  随机浮点数
randint(a,b)  	# [a,b]  随机整数
randrang([start],stop[,step])   # 随机整数  range()
choice(seq)   	# 从列表seq中，随机取一个
choices(seq,k)  # 从列表seq中，随机取k个
shuffle(x)   	# 洗牌
sample(seq,k) 	# 从列表seq中，随机取k个。不会修改原有序列
```



### 4.1 random()

> 用于生成一个0-1之间的随机浮点数

```python
import random

n = random.random()
print(n)      # 0.26768172566792614
```

### 4.2 uniform()

> 返回指定区间的**随机浮点数**

```python
print(random.uniform(10, 20))   # 17.811627164752608
```

**设置随机种子**

```python 
random.seed(666)
print(random.uniform(10, 20))   # 14.561196489769683
```

> 一旦设定固定的种子，后续每次产生的随机数都是相同的，反而没有“随机”效果了

> 如果想复现上次随机结果，可以使用随机种子；否则，无须专门设定随机种子

> 如果不设置随机种子，Python会根据系统时间来执行选择，由于每次运行时，系统时间都是不同的，因此生成的随机数也会因时间差异不同

### 4.3 randint()

> **随机整数**

```python
print(random.randint(10, 20))   # 16
```

### 4.4 randrange()

> 某个特定序列中随机挑选一个元素

### 4.5 choice()

### 4.6 choices()

### 4.7 sample()

### 4.8 shuffle()







## 1 创建游戏窗口

### 1.1 游戏的初始化和退出

```python
pygame.init()   # 初始化。在使用其他模块之前，必须调用init方法
pygame.quit()  # 卸载。在游戏结束之前调用
```

### 1.2 游戏中的坐标系

原点：左上角（0,0）

x轴： 水平向右

y轴：水平向下

```python
python.Rect(x,y,w,h)   -> Rect
```

> 描述矩形区域
>
> 原点（x,y）     	// .x     .y
>
> 矩形（w,h）   宽 高      // .w  .h     .size

### 1.3 创建游戏主窗口

```python
pygame.display.set_mode()   # 初始化游戏显示窗口
pygame.display.update()     # 刷新屏幕内容显示
```

```python
set_mode(resolution=(0,0), flags=0, depth=0)   -> Surface
```

> 作用：创建游戏显示窗口
>
> resolution：指定屏幕的 宽和高。（默认大小=屏幕大小）  【**参数是元组类型**】
>
> flags：指定屏幕的 附加选项（默认不需要传递）
>
> depth：颜色的为数（默认自动匹配）
>
> 返回值：游戏的屏幕

### 1.4 游戏循环

```python
while True:
    pass
```





# 三、数据可视化

## 1 概述

## 2 numpy

* Numpy是使用python进行数组计算的软件包

### 2.1 数据类型

### 2.2 创建数组

```python
import numpy as np

# array()
a = np.array([1, 2, 3])  # 列表->数组
b = np.array((1, 2, 3))  # 元组->数组
c = np.array(([1, 2, 3], [4, 5, 6]))  # 嵌套列表->数组
# d = np.array(([1,2,3],[4,5]))    # 不规则的->数组

# zeros()
e = np.zeros((2, 3))  # 2行3列   浮点型
f = np.zeros((2, 3), dtype=int)  # 行数 列数
g = np.zeros((3, 3, 4))  # 三维数组    (层数 行数 列数)

# ones()
l = np.ones((2,3),dtype=int)

# arange()
h = np.arange(5)  # [0,5)
i = np.arange(-2, 2, dtype=float)  # [-2,2)

# linspace(a,b,c)
j = np.linspace(1, 5, 6)  # (第一个元素, 最后一个元素, 个数)   间隔(b-a/c-1)

# indices()
k = np.indices((2, 6))    # 2*6
```

> range和arange的区别：
>
> * range是不能以小数为步长

### 2.3 数组的形状

```python
import numpy as np

a = np.arange(12)

print(a.shape)  	# 查看数组形状

a.shape = (3, 4)    # 改变数组形状
print(a)

c = a.reshape((6, -1))  # 改变数组形状，并返回新数组。   -1是自动计算
print(c)

a.resize((4, 3))  # 改变数组形状
print(a)
a.resize((4, 5), refcheck=False)  # 可以改变元素  多的用0补
print(a)

---------------------------------------------------
E:\software\anaconda3\python.exe E:\pythonProject\numpy\two.py 
(12,)
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
[[ 0  1]
 [ 2  3]
 [ 4  5]
 [ 6  7]
 [ 8  9]
 [10 11]]
[[ 0  1  2]
 [ 3  4  5]
 [ 6  7  8]
 [ 9 10 11]]
[[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11  0  0  0]
 [ 0  0  0  0  0]]

进程已结束,退出代码0
```

### 2.4 索引、切片、迭代

### 2.5 数组运算

```python
# 数组与常量
import numpy as np

a = np.arange(12)
a + 2
a - 2
a * 2
a / 2
a ** 2
a // 2
a < 2.5     # [ True  True  True False False False False False False False False False]
```

```python
# 矩阵运算
import numpy as np

a = np.array([[1, 2], [4, 5]])
b = np.array([[2, 3], [5, 6]])

a + b   # 矩阵加法
a - b   # 矩阵减法
a * b   # 元素乘法
a @ b   # 矩阵乘法
a.dot(b) # 矩阵乘法
a.T     # 矩阵转置
```

```python
# 赋值运算法
a += 2
a *= 2
```

```python
a.min()   # 最小值
a.max()   # 最大值
a.sun()   # 所有元素求和

a.max(axis=0)  # 返回最大值所在行
a.max(axis=1)  # 返回每一行最大值
```



## 3 pandas

[[第三章\]_pandas_理论.pdf](file:///E:/河南工业大学/7. 科学计算库综合实践/[第三章]_pandas_理论.pdf)

### 3.1 环境安装

> 安装pandas需要的基础环境是Python

```Linux
pip install pandas

>>> import pandas
>>> pandas.__version__    # 查看版本
'1.1.5'


pip list   # 查看是否有
conda list   # 查看是否有
```

### 3.2 读写文件

#### 3.2.1 文本

```python
# 读文本文件
pandas.read_table(filepath_or_buffer, sep=’\t’, header=’infer’, names=None, index_col=None,dtype=None, engine=None, nrows=None)
```

> ![image-20230312183100185](D:\Typora\picture\image-20230312183100185.png)

#### 3.2.2 CSV

```python
# 读CSV文件
pandas.read_csv(filepath_or_buffer, sep=’，’, header=’infer’, names=None, index_col=None,dtype=None, engine=None, nrows=None)
```

> ![image-20230312184451684](D:\Typora\picture\image-20230312184451684.png)

```python
# 写CSV文件
DataFrame.to_csv(path_or_buf = None, sep = ’,’, na_rep,columns=None,header=True,index=True,index_label=None, mode=’w’, encoding=None)
```

> path_or_buf：文件路径
>
> index：显示索引（True）
>
> sep：分隔符。默认“.”

#### 3.2.3 Excel

```python
# 读Excel文件
pandas.read_excel(io, sheetname, header=0, index_col=None, names=None, dtype)
```

> ![image-20230312185207293](D:\Typora\picture\image-20230312185207293.png)

```python
# 写Excel文件
DataFrame.to_excel(excel_writer=None, sheetname=None, na_rep=”,header=True, index=True, index_label=None, mode=’w’,encoding=None)
```

> excel_writer：文件路径
>
> sheet_name：工作表名称。默认“Sheet1”
>
> na_rep：缺失数据
>
> index：是否写行索引。默认True

#### 3.2.4 HTML

```python
# 读HTML表格数据
pandas.read_html(io='路径名称',header='指定行列标题所在行',index_col='指定行列标题所在列',attrs='表格的属性值')
```

#### 3.2.5 数据库

```python
# 读写数据库
read_sql_table()    # 读取整张表——>DF
read_sql_query()    # SQL的结果——>DF
read_sql()   # 既可以读表，也可以读SQL
to_sql()   # 将数据写入SQL数据库
```

> 连接MySQL数据库，使用mysqlconnertor驱动
>
> ```Linux
> pip install mysql-connector
> ```

### 3.3 pandas基础

* 数据结构

  > **序列（Series）**	1维	一维数组，大小==不可变==，数据==可变==，==同种==数据类型元素
  >
  > **数据帧（DataFrame）**	2维	二维数组，大小==可变==，数据==可变==，每列可以是==不同==的数据类型
  >
  > **面板（Panel）**	3维	三维数组，大小==可变==，数据==可变==。

#### 3.3.1 Series

Series是一维标签数组，能够容纳任何类型的数据（整数，字符串，浮点数，python对象等

```python
pandas.Series(data,index,dtype,copy)
```

> | 编号 | 参数    | 说明                                                  |
> | ---- | ------- | ----------------------------------------------------- |
> | 1    | `data`  | 传入的数据。支持多种数据类型，                        |
> | 2    | `index` | 索引。必须是唯一值，且与`data`的长度相同。默认0-N整数 |
> | 3    | `dtype` | 数据类型                                              |
> | 4    | `copy`  | 是否复制数据。默认False                               |

```python
import pandas as pd

# 增
s = pd.Series([1, 2, 3, 4, 5])
s = pd.Series([1, 2, 3, 4, 5], index=['a', 'b', 'c', 'd', 'e'])
dic = {'one': 1, 'two': 2, 'three': [3, 4]}
s = pd.Series(dic)
s = pd.Series(5,index=[0,1,2,3])


# 查
print(s.index)  # 索引
print(s.values)  # 值
print(s['one'])  # 访问列名
print(s[:3])    # 切片
# print(s['five'])     # 访问不存在的索引会报错

s * 2
print(s)
```

> | 属性和方法 | 描述                          |
> | ---------- | ----------------------------- |
> | axes       | 返回行轴标签列表              |
> | dtype      | 返回对象的dtype               |
> | empty      | 如果series为空,则返回True     |
> | ndim       | 根据定义1返回基础数据的维度数 |
> | size       | 返回基础数据中的元素数量      |
> | values     | 将该序列作为ndarray返回       |
> | head()     | 返回前n行                     |
> | tall()     | 返回最后n行                   |

#### 3.3.2 DataFrame

DataFrame 是一个表格型的数据结构，它含有一组有序的列，每列可以是不同的值类型（数值 、字符串、布尔型值）

DataFrame 既有行索引也有列索引，它可以被看做由 Series 组成的字典（共同用一个索引）

![image-20230312222454674](D:\Typora\picture\image-20230312222454674.png)

```python
pandas.DataFrame( data, index, columns, dtype, copy)
```

> | 编号 | 参数    | 说明               |
> | ---- | ------- | ------------------ |
> | 1    | data    | 数据采用各种形式。 |
> | 2    | index   | 行标签             |
> | 3    | columns | 列标签             |
> | 4    | dtype   | 每类的数据类型     |
> | 5    | copy    | False复制          |

```python
import pandas as pd

# 创建
p = pd.DataFrame()  # 空的

data = [1, 2, 3, 4, 5]  # 列表创建
df = pd.DataFrame(data)
   0
0  1
1  2
2  3
3  4
4  5


data = [['one', 1], ['two', 2], ['three', 3]]  # ndarrays/lists创建
df1 = pd.DataFrame(data, columns=['name', 'age'], dtype=float)
    name  age
0    one  1.0
1    two  2.0
2  three  3.0


data = {'Name': ['Tom', 'Jack', 'Aaron', 'Abel'], 'Age': [18, 24, 29, 42]}
df2 = pd.DataFrame(data)
    Name  Age
0    Tom   18
1   Jack   24
2  Aaron   29
3   Abel   42


data = {'Name': ['Tom', 'Jack', 'Aaron', 'Abel'], 'Age': [18, 24, 29, 42]}
df3 = pd.DataFrame(data, index=['r1', 'r2', 'r3', 'r4'])
     Name  Age
r1    Tom   18
r2   Jack   24
r3  Aaron   29
r4   Abel   42


data = [{'a': 11, 'b': 12}, {'a': 15, 'b': 10, 'c': 20}]
df4 = pd.DataFrame(data)
    a   b     c
0  11  12   NaN
1  15  10  20.0


data = [{'a': 11, 'b': 12}, {'a': 15, 'b': 10, 'c': 20}]
df5 = pd.DataFrame(data, index=['first', 'second'])
         a   b     c
first   11  12   NaN
second  15  10  20.0


data = [{'a': 11, 'b': 12}, {'a': 15, 'b': 10, 'c': 20}]
df6 = pd.DataFrame(data, index=['one', 'two'], columns=['a', 'b'])
df7 = pd.DataFrame(data, index=['one', 'two'], columns=['a', 'd'])
     a   b
one  11  12
two  15  10
      a   d
one  11 NaN
two  15 NaN


data = {'one': pd.Series([1, 2, 3], index=['a', 'b', 'c']), 'two': pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}
df8 = pd.DataFrame(data)
   one  two
a  1.0    1
b  2.0    2
c  3.0    3
d  NaN    4

df8.iloc[2]   # 看第2+1行
df8[2:4]  # 切片

```

```python
# 删除
def df['列名columns']
df.pop('列名columns')
```

```python
# 添加
df.['新列名columns'] = pd.Series([10, 20, 30],index=['a', 'b', 'c'])
df['新列名columns'] = df['第一列columns'] + df['第二列columns']


df = pd.DataFrame([[11, 12], [13, 14]], columns = ['a','b'])
df2 = pd.DataFrame([[15, 16], [17, 18]], columns = ['a','b'])
df = df.append(df2)
   a  b
0 11 12
1 13 14
0 15 16
1 17 18


df = df.drop(0)  # 删除0的行
print (df)
   a b
1 13 14
1 17 18
```

```python
df.T   # 转置
df.axes   # 轴 返回行轴标签和列轴标签的列表。
df.dtype  # 返回每列的数据类型
df.empty  # 返回布尔值，表示对象是否为空; True表示该对象为空。
df.ndim  # 返回对象的维数。根据定义，DataFrame是一个2D对象。
df.shape  # 返回表示DataFrame维度的元组。元组（a，b），其中a代表行数， b 代表列数。
df.size  # 返回DataFrame中元素的数量
df.values  # 作为 NDarray 返回DataFrame中的实际数据 
df.head(2)   # 返回前2行。默认5
df.tail(2)  # 范湖后2行。默认5
df.sample(n)  # 查看n个样本。随机。默认1
```

#### 3.3.3 索引操作及高级索引

```python
# 重置索引
DataFrame.reindex(label=None,   
                 index=None,   # 用作索引的新序列
                 coluns=None,  
                 axis=None,
                 method=None,  # 插值填充方式 
                               # （ffill/pad:向前填充值   bfill/backfill:后向填充值  nearest:从最近的索引值填充）
                 copy=True, 
                 level=None,
                 fill_value=nan,   # 引入缺失值时使用的替代值
                 limit=None,  # 向前或 向后填充时的最大填充量
                 tolerance=None)
```

```python
# Series 的索引操作
import pandas as pd

ser = pd.Series([1, 2, 3, 4, 5], index=['a', 'b', 'c', 'd', 'e'])
print(ser['c'])  # index名
print(ser[1])  # 下标
print(ser[2:4])  # 下标切片
print(ser['b':'d'])  # index切片
print(ser[[1, 0, 4]])  # 取下标1,0,4的数据集
print(ser[['a', 'b', 'd']])  # 取索引abd的数据集
# 布尔索引
ser_bool = ser > 3
print(ser_bool)   # 创建布尔型的series类型
print(ser[ser_bool])  # 获取True的数据
```

```python
# DataFrame 的索引操作
import numpy as np
import pandas as pd

df = pd.DataFrame(np.arange(12).reshape(3, 4), columns=['a', 'b', 'c', 'd'])
print(df['b'])  # 获取b列
print(df[['b', 'd']])  # 获取bd列
print(df[:2])  # 获取前两行数据
print(df[:3][['b', 'd']])  # 获取前两行的bd列
# 高级
print(df.loc[1:2, ['c', 'a']])   # 基于标签索引（切片包含结尾）
print(df.iloc[1:3, [2, 0]])  # 基于位置索引（切片不包含结尾）
```

#### 3.3.4 算术运算与数据对齐

```python
import numpy as np
import pandas as pd

ser1 = pd.Series(range(10, 13), index=range(3))
ser2 = pd.Series(range(20, 25), index=range(5))

# 加法运算  （先对齐，对齐做加法，没对齐NAN填充）
print(ser1 + ser2)   # 没对齐NAN填充
print(ser1.add(ser2, fill_value=0))   # 填充0，然后相加
```

#### 3.3.5 数据排序

```python
# 按索引排序
sort_index(axis=0,             # 轴索引（排序的方向），0表示index按行（默认按行），1表示columns按列
          level=None,          # 若不为None，则对指定索引级别的值进行排序
          ascending=True,      # 是否升序排列，默认True，（升序）
          inplace=False,       # 默认False，对数据表进行排序，不创建新的实例
          kind='quicksort',    # 选择排序算法
          na_position='last',
          sort_remaining=True)
```

```python
# 按值排序
sort_values(by,   # 表示排序的列。
            axis=0,              # 轴索引（排序的方向），0表示index按行（默认按行），1表示columns按列
          	level=None,          # 若不为None，则对指定索引级别的值进行排序
          	ascending=True,      # 是否升序排列，默认True，（升序）
          	inplace=False,       # 默认False，对数据表进行排序，不创建新的实例
         	kind='quicksort',    # 选择排序算法
         	na_position='last')  # first：NAN放开头  last：NAN放末尾（默认） 
```

#### 3.3.6 统计计算与描述

| 函数名         | 说明                              |
| -------------- | --------------------------------- |
| sum            | 和                                |
| mean           | 平均值                            |
| median         | 中位数                            |
| max、min       | 最大值、最小值                    |
| idxmax、idxmin | 最大索引值、最小索引值            |
| count          | 非NaN个数                         |
| head           | 获取前N个值                       |
| var            | 样本值的方差                      |
| std            | 标准差                            |
| skew           | 偏度（三阶矩）                    |
| kurt           | 峰度（四阶矩）                    |
| cunsum         | 累积和                            |
| cummin、cummax | 累积最小值、累积最大值            |
| cumprod        | 累计积                            |
| describe       | 对series和dataframe列计算汇总统计 |



```python

```





## 4 matplotlib

[快速入门指南 — Matplotlib 3.7.1 文档](https://matplotlib.org/stable/tutorials/introductory/quick_start.html)

df['species']

![../../_images/anatomy.png](D:\Typora\picture\anatomy.png)



### 4.1 基本概述

```python
import numpy as np
from matplotlib import pyplot as plt
from pylab import mpl

# 消除错误
import warnings
warnings.filterwarnings('ignore')

# 添加数据
X = np.arange(0,26,2)
Y = np.array([16,18,19,20,24,26,30,28,27,22,18,17,16])

# 解决乱码
plt.rcParams['font.sans-serif'] = ['SimHei']   # 显示中文
plt.rcParams['axes.unicode_minus'] = 'False'   # 正常显示正负号

# 设置画布大小
plt.figure(figsize=(10,4),      # figsize调整长宽，
           dpi=300,   # 清晰度
           facecolor='gray')  # 画布背景色

# 设置标题
plt.xlabel("时间")  # x的标题
plt.ylabel("温度")  # y的标题
plt.title("时间和温度图")   # 图的标题

# 设置刻度
plt.xticks(label=X，rotation=45)   # rotation旋转角度
plt.yticks(Y)

# 设置范围
plt.xlim(0,30)
plt.ylim(0,40)

# 绘制网格 
plt.grid(alpha = 0.3)     # alpha：网格透明度

# 保存图片
# plt.savefig("test2202.pdf")    # 保存路径

# 生成图形
_ = plt.plot(X,Y,label="图例")    # 生成折线图

# 设置图例
plt.legend(loc = "center")

# 关闭坐标轴
plt.axis('off')

# 图形展示
plt.show()     # 展示图形
```

> 图例：
>
> ```txt
> 	    ===============   =============
>   Location String   Location Code
>   ===============   =============
>   'best'            0
>   'upper right'     1
>   'upper left'      2
>   'lower left'      3
>   'lower right'     4
>   'right'           5
>   'center left'     6
>   'center right'    7
>   'lower center'    8
>   'upper center'    9
>   'center'          10
>   ===============   =============
> ```

### 4.2 颜色、样式、标记

```python
# 传入数据
a = np.arange(-10,10)
b = a*0.5

plt.figure(figsize=(10,5),dpi=300)


# 颜色color： 红色r  蓝色B  绿色g  白色w  青色c  品红m  黄色y  黑色k
# 样式linestyle： 直线-  虚线--  ：   点划线-.
# 标记marker： 实心圆圈o  菱形D  正方形s  六边形h H  八边形8  点.  三角形 ^ < > v   星号*  加号+  
# 粗细markersize：
    
    
# 绘图
# plt.plot(a,b,color='r',linestyle='--',linewidth=5,alpha=0.5)
plt.plot(a,b,'r-o')      # 红色 实线 -
plt.plot(a,b-1,'g--D')   # 绿色  虚线 --
plt.plot(a,b-2,'b-.h')   # 蓝色   点划线 -.
plt.plot(a,b-3,'b:H')   # 白色   点虚线:
# cmyk
plt.plot(a,b-4,'c8-')   # 青色    
plt.plot(a,b-5,"mp-")   # 洋红
plt.plot(a,b-6,'y+-')   # 黄色
plt.plot(a,b-7,'k.-')   # 黑色

plt.plot(a,b+1,'ks-')   # 黑色
plt.plot(a,b+2,'k*-')   # 黑色
plt.plot(a,b+3,'kv-')   # 黑色
plt.plot(a,b+4,'k^-')   # 黑色
plt.plot(a,b+5,'k>-')   # 黑色
plt.plot(a,b+6,'k<-')   # 黑色
plt.show()
```

### 4.3 多子图

```python
# 多子图1
x_one = np.arange(0,100,0.5)
y_one = np.sin(x_one)

x_two = np.arange(100,150,0.5)
y_two = np.sin(x_two)

plt.subplot(221)   # 2行2列子图1
_ = plt.plot(x_one,y_one)

plt.subplot(222)   # 2行2列子图2
_ = plt.plot(x_two,y_two)

plt.subplot(212)   # 2行1列子图2
_ = plt.plot(x_two,y_two)
```

![image-20230303105823105](D:\Typora\picture\image-20230303105823105.png)

```python
# 多子图2
x_one = np.arange(0,100,0.5)
y_one = np.sin(x_one)

x_two = np.arange(100,150,0.5)
y_two = np.sin(x_two)

fig,axes = plt.subplots(nrows=2,ncols=2)   # 画布对象，子图对象    nrows行数  ncols列数  sharex sharey xy  True/all  Flase/None  row   col
axes[0,0].plot(x_one,y_one)
axes[0,1].plot(x_two,y_two)
axes[1,1].plot(x_two,y_two)
fig.show()
```

```python
# 多子图3
x_one = np.arange(0,100,0.5)
y_one = np.sin(x_one)

fig = plt.figure()

plt1 = fig.add_subplot(2,2,1)
plt2 = fig.add_subplot(2,2,2)
plt4 = fig.add_subplot(2,2,4)

plt1.plot(x_one,y_one)
plt1.set_xlabel("时间")
plt1.set_ylabel("分数")
plt1.set_title("测试图表1")

plt4.plot(x_two,y_two)
```

```python
# 图中图
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0,2*np.pi,200)
y = np.sin(x * x)

fig = plt.figure()
left1,bottom1,widht1,hight1 = 0.1,0.1,0.8,0.8

plt.rcParams['font.sans-serif'] = 'SimHei'
plt.rcParams['axes.unicode_minus'] = False

axes_1 = fig.add_axes([left1,bottom1,widht1,hight1])
axes_1.scatter(x,y)
axes_1.set_xlabel('x')
axes_1.set_ylabel('y')
axes_1.set_title("这是第一个图")

# 绘制第二个子图
left2,bottom2,widht2,hight2 = 0.6,0.6,0.3,0.3
axes_2 = fig.add_axes([left2,bottom2,widht2,hight2])
axes_2.plot(x,y)
axes_2.set_xlabel('x')
axes_2.set_ylabel('y')
axes_2.set_title("这是第二个图")

plt.show()
```

![图中图](D:\Typora\picture\image-20230303114224419.png)

```python
# 填充图
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0,1,500)
y = np.sin(3*np.pi*x)*np.exp(-4*x)

fig,ax = plt.subplots(1,1)
ax.plot(x,y)
plt.fill_between(x,0,y,facecolor = 'g',alpha=0.3)
plt.show()
```

![填充图](D:\Typora\picture\image-20230303115641087.png)

```python
# 叠图
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 2 * np.pi, 400)

y = np.sin(x ** 2)

fig = plt.figure()

ax1 = fig.add_axes([0.1, 0.1, 0.5, 0.5])
ax2 = fig.add_axes([0.2, 0.2, 0.5, 0.5])
ax3 = fig.add_axes([0.3, 0.3, 0.5, 0.5])
ax4 = fig.add_axes([0.4, 0.4, 0.5, 0.5])

ax4.plot(x, y, 'r-')

plt.show()
```

![image-20230316223033017](D:\Typora\picture\image-20230316223033017.png)

```python
# 等比例坐标
import numpy as np
import matplotlib.pyplot as plt

X = np.linspace(0, 10, 100)

fig, ax = plt.subplots()
#线条的风格
styles = ['-', '--', '-.', ':']
colors = ['c', 'm', 'y', 'k']

lines = []

for i in range(4):
    lines += ax.plot(X, np.sin(X - i * np.pi / 2),
           styles[i],
            color = colors[i]
            #label = f'sin(x -{i} * π /2 )'  #<-重要的知识点
           )

ax.axis('equal')

ax.legend(lines[:2], ['$sin(x)$', '$sin(x + \\frac{1}{2} \pi)$'],
         loc = 'upper right',
          frameon = False
         )

from matplotlib.legend import Legend
leg = Legend(ax, lines[2:], ['$X_{1}^{3}$', 'Line D'],
      loc = 'lower left',
       frameon = False
      )


ax.add_artist(leg)

plt.xticks(ticks = np.arange(0, 3 * np.pi, 0.5 * np.pi),
          labels = ['0', '$\\frac{1}{2}\pi$',
                   '$\pi$',
                    '$\\frac{3}{2}\pi$',
                    '$\\frac{4}{2}\pi$',
                    '$\\frac{5}{2}\pi$'
                   ]
          )


#plt.legend()
plt.show()
```

![image-20230316222032398](D:\Typora\picture\image-20230316222032398.png)



### 4.4 其他图形

#### 4.4.1 条形图（bar）

```python
bar(x,    # 表示x的坐标值
    height,  # 表示柱形的高度
    width=0.8,  # 表示柱形的宽度，默认为0.8
    bottom=None, # 表示柱形底部的y坐标值，默认为0
    align='center',  # 表示柱形的对齐方式，有’center’和’edge’两个取值，
    			     # 其中’center’表示将柱形与刻度线居中对齐,'edge’表示将柱形的左边与刻度线对齐
    data=None,   
    tick_label=None,
    xerr=None,  # 若未设为None,则需要为柱形图添加水平/垂直误差棒
    yerr=None,
    error_kw=None,  # 表示误差棒的属性字典,字典的键对应errorbar()函数的关键字参数.
    **kwargs)
```

```python
import numpy as np
import matplotlib.pyplot as plt

grade = ["人工2201","人工2202","人工2203","人工2204","人工2205"]
people = [30,30,29,30,29]

plt.bar(grade,people)
# x: x轴数据[array]   
# height：条形高度 [array]  
# width：条形宽度（0.8）[float  0-1]   
# color：条形颜色   
# edgecolor：条形边框颜色
plt.show()
```

```python
# 左右形式
import numpy as np 
import matplotlib.pyplot as plt

zhangsan = np.array((90, 55, 40, 65))
lisi = np.array([5, 62, 54, 20])
plt.rcParams['font.sans-serif'] = ['SimHei']
X = np.arange(1, 5)

bar_width = 0.3

plt.bar(X, zhangsan, 
        width = bar_width,
        color = "w", edgecolor = 'k',
       hatch = r'+', tick_label = ['语文', '数学', '英语', '物理'],
        label = '张三的成绩'
       )

plt.bar(X + bar_width, #左右结构的关键
        height = lisi, 
        width = bar_width,  #默认值为0.8，特定值，需要设置
        color = "y",  
       hatch = r'**', tick_label = ['语文', '数学', '英语', '物理'],
        label = '李四的成绩'
       )
plt.legend()
plt.show()
```



#### 4.4.2 水平条形图（bath）

```python
import numpy as np
import matplotlib.pyplot as plt

grade = ["人工2201","人工2202","人工2203","人工2204","人工2205"]
people = [30,30,29,30,29]

plt.barh(grade,people)
# x: x轴数据   height：条形高度   width：条形宽度（0.8）   color：条形颜色   edgecolor：条形边框颜色
plt.show()
```



#### 4.4.3 直方图（hist）

```python
import numpy as np
import matplotlib.pyplot as plt

grade = ["人工2201","人工2202","人工2203","人工2204","人工2205"]
# people = [30,30,29,30,29]

plt.hist(grade)    # 统计数组里的个数
# color：条形填充颜色
# edgecolor：条形边框颜色
# hatch：填充物   (*** +++ /// \\\ ...)
# density = 1  是否是密度函数，概率
plt.show()
```



#### 4.4.4 饼图（pie）

```python
matplotlib.pyplot.pie(x,    # 浮点型数组，表示每个扇形的面积。
                      explode=None,  # 数组，表示各个扇形之间的间隔，默认值为0。
                      labels=None,   # 列表，各个扇形的标签，默认值为 None。
                      colors=None,   # 数组，表示各个扇形的颜色，默认值为 None。
                      autopct=None,  # 设置饼图内各个扇形百分比显示格式，
                      				      # %d%% 整数百分比，        %0.1f 一位小数，
                                          # %0.1f%% 一位小数百分比， %0.2f%% 两位小数百分比。
                      pctdistance=0.6, # 类似于 labeldistance，指定 autopct 的位置刻度，默认值为 0.6。
                      shadow=False,  # 布尔值 True 或 False，设置饼图的阴影，默认为 False，不设置阴影。
                      labeldistance=1.1,  # 标签标记的绘制位置，相对于半径的比例，默认值为 1.1，如 <1则绘制在饼图内侧。
                      startangle=0,  # 起始绘制饼图的角度，默认为从 x 轴正方向逆时针画起，如设定=90则从y轴正方向画起。
                      radius=1,   # 设置饼图的半径，默认为 1。
                      counterclock=True, # 布尔值，设置指针方向，默认为 True，即逆时针，False 为顺时针。
                      wedgeprops=None, # 字典类型，默认值 None。参数字典传递给 wedge 对象用来画一个饼图。例如：		                                          wedgeprops={'linewidth':5} 设置wedge 线宽为5。 
                      textprops=None,   # 字典类型，默认值为：None。传递给 text 对象的字典参数，用于设置标签（labels）                                           和比例文字的格式。
                      center=0, 0,  # 浮点类型的列表，默认值：(0,0)。用于设置图标中心位置。
                      frame=False,  # 布尔类型，默认值：False。如果是 True，绘制带有表的轴框架。
                      rotatelabels=False,  # 布尔类型，默认为 False。如果为 True，旋转每个 label 到指定的角度。
                      *,
                      normalize=None, 
                      data=None)
```

```python
import numpy as np
import matplotlib.pyplot as plt

grade = ["人工2201","人工2202","人工2203","人工2204","人工2205"]
people = [30,30,29,30,29]

plt.pie(people,explode=(0.1,0,0,0,0),labels=grade,autopct =' %1.2f%%')
# x；数据[array]
# explode: 指定项离饼图圆心为n个半径（None）[array]
# labels：每一项的名称（None）[array]
# color：颜色（None）[string   array]
# autopct：指定数值（None）[string]
# pctdistanc：每一项的比例和距离饼图圆心n个半径（0.6）
# labeldistance：每一项的名称和距离饼图圆心n个半径（1.1）
# radius：饼图的半径（1）
plt.show()
```

> * [关于python：如何使用matplotlib autopct？ | 码农家园 (codenong.com)](https://www.codenong.com/6170246/)
>
> * [Python可视化29|matplotlib-饼图（pie） - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/203527939)

#### 4.4.5 光谱图（speegram）

#### 4.4.6 堆积区域图（stackplot）

#### 4.4.7 散点图（scatter）

> mark：
>
> * .
> * *
> * ,
> * d
> * D
> * _
> * +
> * <
> * `>`
> * ^

```python
import numpy as np
import matplotlib.pyplot as plt

X = np.arange(1,20)
Y = X * X
plt.scatter(X, Y, marker = 'D', s = 200)
plt.plot(X,Y, 'r-.')
plt.show()
```

![image-20230316224440260](D:\Typora\picture\image-20230316224440260.png)



#### 4.4.8 折线图（plot）

#### 4.4.9 箱型图（boxplot）





## 5 Seaborn



#### 热力图

函数名称：sns.heatmap

函数作用：绘制矩阵颜色图。

函数参数：

- data：必选参数，rectangular dataset，可以转换为ndarray类型的数据集，如果提供一个 pandas.DataFrame，那么索引/列信息将被用于标记列和行。
- vmin, vmax：可选参数，浮点型，颜色映射的锚定值，否则它们将从数据和其他关键字参数中推断出来。
- cmap：可选参数，matplotlib 对象或者是列表形式的颜色，将数据值映射到颜色空间。如果未提供，则默认情况下将取决于是否设置 center。
- center：可选参数，浮点型，绘制发散数据时将映射到颜色图的中心值。使用此参数将更改缺省的 cmap 如果没有指定的话。
- robust：可选参数，bool型，如果为True并且 vmin 或 vmax不存在，则使用鲁棒性量化计算 colormap 范围，而不是极端值。
- annot：可选参数，bool型或者rectangular dataset，如果为True，则在每个单元格中写入数据值。如果是与data具有相同形状的类数组，则使用它来注释热图而不是数据。请注意，DataFrames将匹配位置，而不是索引。
- fmt：可选参数，str型，添加注释时要使用的字符串格式代码。
- annot_kws：可选参数，dict型，关键字参数：matplotlib.axes.Axes.text 是True时。
- linewidths：可选参数，浮点型，将分割每个单元格的线的宽度。
- linecolor：可选参数，color型，将分割每个单元格的线的颜色。
- cbar：可选参数，bool型，是否绘制颜色条。
- cbar_kws：可选参数，dict 型，当cbar为True时，关键字参数传递给 matplotlib.figure.Figure.colorbar。
- cbar_ax：可选参数，matplotlib Axes类型，用于绘制颜色条的坐标轴，否则从主轴中移出空间。
- square：可选参数，bool型，如果是True，则将Axes方面设置为“相等”，使每个单元格都是正方形。
- xticklabels, yticklabels：可选参数，"auto"，bool型，列表形式的字符，整数类型。如果为True，则绘制数据框架的列名。如果为False，则不绘制列名。如果是列表样式，则将这些替代标签作为xticklabels。如果是整数，则使用列名但仅绘制每个n个标签。如果是"auto"，则尝试密集地绘制不重叠的标签。
- mask：可选参数，布尔数组或DataFrame，如果传递，则没有显示mask=True的单元格中的数据。带有缺失值的单元格将自动蒙版。
- ax：可选参数，matplotlib Axes类型，用于绘制绘图的坐标轴，否则使用当前活动的Axes。
- kwargs：可选参数，其他关键字参数，所有其他关键字参数都传递给matplotlib.axes.Axes.pcolormesh。

函数返回：

- ax：matplotlib Axes类型，具有热图的Axes对象。

参考示例：

```python
import seaborn as sns;
import numpy as np
uniform_data = np.random.rand(10, 12)
ax = sns.heatmap(uniform_data)

sns.set_theme()
flights = sns.load_dataset("flights")
flights = flights.pivot("month", "year", "passengers")
ax = sns.heatmap(flights, annot=True, fmt="d")

corr = np.corrcoef(np.random.randn(10, 200))
mask = np.zeros_like(corr)
mask[np.triu_indices_from(mask)] = True
with sns.axes_style("white"):
    f, ax = plt.subplots(figsize=(7, 5))
    ax = sns.heatmap(corr, mask=mask, vmax=.3, square=True)
```



# 四、OpenCV计算机视觉

## 1 OpenCV起步

>  OpenCV：开源计算机视觉库（Open Source Computer Vision Library）

* 1999年：Inter公司的Gary Bradsky创建
* 2000年发布第一个版本
* 2006年10月    OpenCV 1.0
* 2009年9月      OpenCV 2.0
* 2015年6月      OpenCV 3.0，不向后兼容2.x
* 2018年            OpenCV 4.0
* 2020年10月    OpenCV 4.5.0

### 1.1 配置开发环境

1. 安装python

   > ([Welcome to Python.org](https://www.python.org/))

2. 安装numpy

   ```linux
   pip install numpy
   ```

3. 安装OpenCV-Python

   ```linux
   pip install opencv-python     # 只安装OpenCV的主版块
   pip install opencv-contrib-python    # 同时安装OpenCV的主模块和贡献模块
   ```

4. 安装visual studio code

5. 安装PyCharm

   > [PyCharm: the Python IDE for Professional Developers by JetBrains](https://www.jetbrains.com/pycharm/)



## 2 图像处理基础

```python
import cv2

cv2.imread("图片的地址",图像读取格式标志)   # 读
cv2.imwrite("图片的地址", 图像数组)   # 写
cv2.imshow("窗口的名称", 图像数组)   # 显示
cv2.waitKey("等待的毫秒数")   # 等待
cv2.distoryWindow(图像数组)   # 关闭窗口
--------------------------------------------------
import cv2

vc = cv2.VideoCaptrue("视频的地址")   # 生成对象
success, frame = cv2.read()   # 读一帧
vw = cv2.VideoWrite("保存的视频名", 视频解码格式, 帧率, 大小)   # 生成对象
vw.wirte(frame)   # 写
vc.release()   # 关闭
---------------------------------------------------
import cv2

b,g,r = cv2.split(图像)   # 拆分
img = cv2.merge([b,g,r])   # 合并
```



### 2.1 图像

#### 2.1.1 读   cv2.imread()

```python
import cv2

img = cv2.imread('..\picture\demo.png')  # 读图像
print(type(cv2))  # 数据类型
print(img)   # 图像数组
print(img.shape)  # 数组形状   (850, 797, 3)
print(img.dtype)  # 数组元素的数据类型   
print(img.size)   # 数组元素个数
```

> 彩色图像的数组是一个三维数组  ==（高度，宽度，通道数）==
>
> 图像的分辨率是：高度 X 宽度
>
> 每个数组元素为一个像素的==BGR==通道的颜色值   
>
> 颜色值取值范围：[0, 255]

> ==**img = cv2.imread(fliename, flag)**==
>
> fliename：图像文件名
>
> flag：图像读取格式标志

#### 2.1.2 写   cv2.imwrite()

```python
import numpy as np
import cv2

img = np.ones((6, 6), dtype=np.uint8)
cv2.imwrite('..\picture\mypic2-1.jpg', img)    # cv2.imwrite(文件名,数组)
```

#### 2.1.3 显示   cv2.imshow()

```python
import numpy as np
import cv2

img = cv2.imread('..\picture\demo.png')
cv2.imshow('demo', img)

# 解决显示后立即关闭
key = 0
while key != 27:      # 按Esc键
    key = cv2.waitKey()   # 等待按键
cv2.destoryWindow('demo')
```

> ```python
> rv = cv2.waitKey([delay])
> ```
>
> * rv：保存函数的返回值。【键没按下，返回-1；键按下，返回键的ASCII码】
> * delay：表示等待按键的时间。默认0。【负数或0：无限等待；正数：等待参数毫秒后结束等待，返回-1】

### 2.2 视频

#### 2.2.1 播放视频

```python
import cv2 as cv

vc = cv.VideoCapture("../video/demo.mp4")  # 创建videocapture对象  （视频文件）
fps = vc.get(cv.CAP_PROP_FPS)  # 读取视频帧速率
size = (vc.get(cv.CAP_PROP_FRAME_HEIGHT), vc.get(cv.CAP_PROP_FRAME_WIDTH))  # 读取视频大小
print("帧速率：", fps)
print("大小", size)
success, frame = vc.read()  # 读第一帧  
while success:      # 循环读取帧
    cv.imshow('myvideo', frame)    # 在窗口中显示帧图像
    success, frame = vc.read()    # 读下一帧
    key = cv.waitKey(25)     # 延时时间
    if key == 27:
        break
vc.release()    # 关闭视频
```

> ```python
> vc = cv2.VideoCapture()
> vc.read()   # 获取视频的每一帧，每一帧都是一副图像
> vc.write()  # 将帧写入视频文件
> cv2.imshow('窗口名',图像数组)   
> ```
>
> 默认是浮点数，可以换成整数
>
> (int(vc.get(cv.CAP_PROP_FRAME_HEIGHT)),int(vc.get(cv.CAP_PROP_FRAME_WIDTH)))

#### 2.2.2 将视频写入文件

```python
import cv2 as cv

vc = cv.VideoCapture("test2-6out.avi")  # 创建videocapture对象  （视频文件）
# vc = cv.VideoCapture("../video/demo.mp4")  # 创建videocapture对象  （视频文件）
fps = vc.get(cv.CAP_PROP_FPS)  # 读取视频帧速率
size = (int(vc.get(cv.CAP_PROP_FRAME_HEIGHT)),int(vc.get(cv.CAP_PROP_FRAME_WIDTH)))  # 读取视频大小

vw = cv.VideoWriter('test2-6out.avi', cv.VideoWriter_fourcc('X', 'V', 'I', 'D'), fps, size)
success, frame = vc.read()
while success:
    vw.write(frame)
    success, frame = vc.read()

vc.release()  # 关闭视频
```

> ==cv2.VideoWriter(‘指定保存视频的文件名’, 视频解码格式, 帧速率, 大小)==
>
> **常用的解码器格式**
>
> ```python
> cv2.VideoWriter_fourcc('P','I','M','1')   # XVID的MPEG-1编码格式（.avi）
> cv2.VideoWriter_fourcc('M','P','4','2')   # Microsoft的MPEG-4编码格式（.avi）
> cv2.VideoWriter_fourcc('X','V','I','D')   # XVID的MPEG-4编码格式（.avi）
> cv2.VideoWriter_fourcc('F','L','V','1')   # XVID的MPEG-4编码格式（.flv）
> ```

#### 2.2.3 捕获摄像头视频

```python
import cv2 as cv
vc = cv.VideoCapture(0)    # 0表示默认摄像头
fps = 30   # 帧率
size = (int(vc.get(cv.CAP_PROP_FRAME_HEIGHT)), int(vc.get(cv.CAP_PROP_FRAME_WIDTH)))  # 读取视频大小

vm = cv.VideoWriter('../video/test2-3-1.avi',   # 设置保存视频的文件名
                    cv.VideoWriter_fourcc('X', 'V', 'I', 'D'),    
                    fps,
                    size)   
success, frame = vc.read()  
while success:
    vm.write(frame)
    cv.imshow('mycarmra', frame)
    key = cv.waitKey(0)
    if key == 27:
        break
    success, frame = vc.read()
vc.release()
```

####  2.2.4 操作灰度图像

```python
import cv2
import numpy as np

img = np.zeros((10, 10), dtype=np.uint8)

n = 0
while True:
    cv2.imshow("操作灰度图像", img)
    n += 20
    img[:, :] = n    # img[行, 列]
    print(img[1, 1])
    print(img)
    key = cv2.waitKey(1000)
    if key == 27:
        break
```

#### 2.2.5 操作彩色图像

```python
import cv2
import numpy as np

img = np.zeros((240, 320, 3), dtype=np.uint8)
r0 = 0
r1 = 1
r2 = 2
while True:
    img[:80, :, r0] = 255
    img[80:160, :, r1] = 255
    img[160:, :, r2] = 255
    cv2.imshow("彩色窗口", img)
    key = cv2.waitKey()
    img[:, :, :] = 0
    t = r0
    r0 = r1
    r1 = r2
    r2 = t
    if key == 27:
        break
```

#### 2.2.6 图像通道操作

```python
import cv2

img = cv2.imread("../picture/demo.png", cv2.IMREAD_REDUCED_COLOR_2)
cv2.imshow("test", img)

# 通过数组索引拆分通道
b = img[:, :, 0]   # 获得B通道图像
g = img[:, :, 1]   # G
r = img[:, :, 2]   # R

# 使用cv2.split()函数拆分
b, g, r = cv2.split(img)


cv2.imshow("testb", b)
cv2.imshow("testg", g)
cv2.imshow("testr", r)
cv2.waitKey(-1)

# 合并图像通道 
b, g, r = cv2.split(img)   #  按通道拆分图像
rgb = cv2.merge([r, g, b])  # 合并 
gbr = cv2.merge([g, b, r])  # 合并
cv2.imshow('test_rgb', rgb)
cv2.imshow('test_gbr', gbr)
```

> cv2.split()拆分效率不如数组索引
>
> 在处理较大图像时，优先考虑 **数组索引**

### 2.3 图像运算

#### 2.3.1 加法运算

```python
# 加法运算
'''
	    +:如果两个像素相加大于256，则按256取模    （两图像融合）
cv2.add():如果两个像素相加大于256，则取255       （b的轮廓看a的照片）
'''

import cv2

img1 = cv2.imread("../picture/demo.png", cv2.IMREAD_REDUCED_COLOR_2)
img2 = cv2.imread("../picture/demo_one.png")
img3 = img1 + img2          
img4 = cv2.add(img1, img2)

cv2.imshow('img1', img1)
cv2.imshow('img2', img2)
cv2.imshow('img3', img3)
cv2.imshow('img4', img4)

cv2.waitKey(0)
```

![加法运算](D:\Typora\picture\image-20230301180333121.png)

>  +:如果两个像素相加大于256，则按256取模    （两图像融合）
>
>  cv2.add():如果两个像素相加大于256，则取255   （b的轮廓看a的照片）

#### 2.3.2 加权加法运算

```python
import cv2

img1 = cv2.imread("../picture/demo.png", cv2.IMREAD_REDUCED_COLOR_2)
img2 = cv2.imread("../picture/demo_one.png")
img3 = cv2.addWeighted(img1, 0.8, img2, 0.2, 0)

cv2.imshow('img1', img1)
cv2.imshow('img2', img2)
cv2.imshow('img3', img3)   # 加水印

cv2.waitKey(0)
```

> ```python
> dst = cv2.addWeighted(src1, alpha, scr2, beta, gamma)
> 保存结果 = cv2.addWeighted(图像数组1, 权重1, 图像数组2, 权重2, 附加值)
> ```
>
> dst = src1 * alpha + src * beta + gamma

#### 2.3.3 位运算

```python
import cv2

img1 = cv2.imread("../picture/one.png")
img2 = cv2.imread("../picture/three.png")

img3 = cv2.bitwise_and(img1, img2)   # 按位与
img4 = cv2.bitwise_or(img1, img2)   # 按位或
img5 = cv2.bitwise_not(img1)    # 按位非
img6 = cv2.bitwise_xor(img1, img2)   # 按位异或

cv2.imshow("img1", img1)
cv2.imshow("img2", img2)
cv2.imshow("img3", img3)
cv2.imshow("img4", img4)
cv2.imshow("img5", img5)
cv2.imshow("img6", img6)

cv2.waitKey(0)
```

## 3 图形用户界面

### 3.1 窗口控制

```python
# 创建窗口
cv2.namedWindow(Winname[,flags])  
```

> Winname：窗口名称
>
> flags：窗口属性常量

```python
# 关闭窗口
cv2.destroyAllWindows()     # 关闭所有窗口
cv2.destroyWindow(winname)  # 关闭指定窗口
```

```python
# 调整窗口大小
cv2.resizeWindow(winname,size)
```

> size：窗口大小的二元组

### 3.2 绘图

```python
# 绘制直线
cv2.line(img,pt1,pt2,color[,thinckness[,lineType[,shift]]])
     绘制图像，起点坐标，终点坐标，颜色，粗细，线条类型，坐标的数值精度

# 绘制矩形
cv2.rectangle(img,pt1,pt2,color[,thinckness[,lineType[,shift]]])
             一个顶点，另一个顶点

# 绘制圆
cv2.circle(img,center,radius,color[,thinckness[,lineType[,shift]]])
               圆心坐标，半径

# 绘制椭圆
cv2.ellipse(img,center,axes,angle,startAngle,endAngle,color[,thinckness[,lineType[,shift]]])
             圆心坐标，轴(长半轴，短半轴)，旋转角度，开始角度，结束角度

# 绘制多边形
cv2.polylines(img,pts,isClosed,color[,thinckness[,lineType[,shift]]])
            多边形各顶点坐标，True封闭多边形

# 绘制文本
cv2.polylines(img,text,org,fontFace,fontScale,color[,thinckness[,lineType[,bottomLetOrigin]]])
               绘制文本，文本左下角位置，字体类型，字体大小                      文本方向（True垂直镜像）
    
# 绘制中文
import numpy as np
import cv2
from PIL import ImageFont, ImageDraw, Image

img = np.zeros((200, 320, 3), np.uint8) + 255  # 创建白色图像
fontpath = 'STSONG.TTF'  # 指定字体文件名
font1 = ImageFont.truetype(fontpath, 36)   # 载入字体，设置字号
img_pil = Image.fromarray(img)   # 转换成PIL格式
draw = ImageDraw.Draw(img_pil)   # 创建draw对象
draw.text((50, 60), '计算机视觉', font=font1, fill=(0, 0, 0))  # 绘制文本
img = np.array(img_pil)   # 转换成数组对象
cv2.imshow('draw', img)   # 显示成图像
cv2.waitKey(0)

# 绘制箭头
cv2.arrowedLine(img,pt1,pt2,color[,thinckness[,lineType[,shift[,tipLength]]]])
                                                              箭尖相对于箭头长度的比例
```

> img：用于绘制图像的图像
>
> pt1：起点坐标
>
> pt2：终点坐标
>
> color：颜色。BGR模型，（255,0,0）蓝色
>
> thickness：线条粗细。默认1。填充图形：-1
>
> lineType：线条类型。默认cv2.Line_8
>
> > ```python
> > cv2.FILLED：  # 填充
> > cv2.LINE_4：  # 4条连接线
> > cv2.LINE_8：  # 8条连接线
> > cv2.LINE_AA： # 抗锯齿线，线条更平滑
> > ```
>
> shift：坐标的数值精度
>
> 
>
> center：圆心坐标
>
> axes：椭圆的轴。（长轴的一半，短轴的一半）
>
> angle：椭圆长轴的旋转角度。长轴与X轴的夹角
>
> startAngle：开始角度
>
> endAngle：结束角度
>
> 
>
> isClosed：封闭多边形：True；否则依次连接各个顶点，绘制一条曲线
>
> test：要绘制的文本
>
> org：文本左下角的位置
>
> fontFace：字体类型
>
> > ```python
> > cv2.FONT_HERSHEY_SIMPLEX： # 正常大小的sans-serif字体
> > cv2.FONT_HERSHEY_PLAIN: # 小号的sans-serif字体
> > cv2.FONT_HERSHEY_DUPLEX： # 较复杂的正常大小的sans-serif字体
> > cv2.FONT_HERSHEY_COMPLEX：# 正常大小的serif字体
> > cv2.FONT_HERSHEY_TRIPLEX：# 较复杂的正常大小的serif字体
> > cv2.FONT_HERSHEY_COMPLEX_SMALL：# 简化版正常大小的serif字体
> > cv2.FONT_HERSHEY_SCRIPT_SIMPLEX：# 手写风格的字体
> > cv2.FONT_HERSHEY_SCRIPT_COMPLEX：# 较复杂的手写风格的字体
> > ```
>
> bottomLeftOrigin：文本方向。默认False。设置为True时，文本方向为垂直镜像。
>
> 
>
> tipLength：箭尖相对于箭头长度的比例。默认0.1

### 3.3 响应鼠标事件

```python
# 鼠标回调函数
def mouseCallbace(event,x,y,flags,param ...)
    自定义函数名称 鼠标事件对象，坐标xy，常量，传递给回调函数的其他数据

# 为图像窗口绑定鼠标回调函数
cv2.setMouseCallback(wname,mouseCallback)
                   图像窗口名称，鼠标回调函数名称
```

> event：调用时传递给函数的鼠标事件对象
>
> x，y：触发鼠标事件时，鼠标指针在窗口中的坐标（x,y）
>
> flags：触发鼠标事件时，鼠标拖动或键盘按键操作，参数可设置为下列常量
>
> > ```python
> > # 鼠标左键
> > cv2.EVENT_LBUTTONDBLCLK    # 双击
> > cv2.EVENT_LBUTTONDOWN     # 按下
> > cv2.EVENT_LBUTTONUP   # 释放
> > 
> > # 鼠标中键
> > cv2.EVENT_MBUTTONDBLCLK  # 双击
> > cv2.EVENT_MBUTTONDOWN  # 按下
> > cv2.EVENT_MBUTTONUP  # 释放
> > cv2.EVENT_MOUSEHWHEEL  # 滚动（正负代表向左向右）
> > cv2.EVENT_MOUSEWHEEL  # 滚动（正负代表向前向后）
> > 
> > # 鼠标移动
> > cv2.EVENT_MOUSEMOVE  # 鼠标移动
> > 
> > # 鼠标右键
> > cv2.EVENT_RBUTTONDBLCLK  # 双击
> > cv2.EVENT_RBUTTONDOWN  # 按下
> > cv2.EVENT_RBUTTONUP  # 释放
> > 
> > # 键盘
> > cv2.EVENT_FLAG_ALTKEY  # 按下Alt
> > cv2.EVENT_FLAG_CTRLKEY # 按下Ctrl
> > cv2.EVENT_FLAG_SHIFTKEY # 按下shift
> > 
> > # 拖动
> > cv2.EVENT_FLAG_LBUTTON  # 按左键拖
> > cv2.EVENT_FLAG_MBUTTON  # 按中键拖
> > cv2.EVENT_FLAG_RBUTTON  # 按右键拖
> > ```

例子

```python
import cv2
import numpy as np

img = np.zeros((360, 400, 3), np.uint8) + 255   # 白色图像

def draw(event, x, y, flags, param):
    global img
    if event == cv2.EVENT_MOUSEMOVE and flags == cv2.EVENT_FLAG_LBUTTON:
        cv2.circle(img, (x, y), 5, (255, 0, 0), -1)
    elif event == cv2.EVENT_LBUTTONDBLCLK:
        img = np.zeros((360, 360, 3), np.uint8) + 255

cv2.namedWindow("drawing")
cv2.setMouseCallback('drawing', draw)
while True:
    cv2.imshow('drawing', img)
    key = cv2.waitKey(1)
    if key == 27:
        break
cv2.destroyAllWindows()
```



### 3.4 使用跟踪栏

```python
# 创建跟踪栏
cv2.creatTrackbar(trackbarname, wname, value, count, onChange, userdata)
                    跟踪栏名称，图像窗口名称，跟踪栏中滑块的初始位置，跟踪栏的最大值，回调函数名称，其他可选数据

# 返回跟踪栏的当前值
retval = cv2.getTrackbarPos(trackbarname, wname)
                             跟踪栏名称，图像窗口名称
```

> count：跟踪栏的最大值。最小值为0
>
> onChange：跟踪栏滑块位置变化时调用的回调函数名称
>
> userdata：传递给回调函数的其他可选数据

> ```python
> import numpy as np
> import cv2
> 
> img = np.zeros((142, 400, 3), np.uint8)
> 
> 
> def doChange(x):
> b = cv2.getTrackbarPos('B', 'trackbar')
> g = cv2.getTrackbarPos('G', 'trackbar')
> r = cv2.getTrackbarPos('R', 'trackbar')
> img[:] = [b, g, r]
> 
> 
> cv2.namedWindow("trackbar")
> b = cv2.createTrackbar('B', 'trackbar', 0, 255, doChange)
> g = cv2.createTrackbar('G', 'trackbar', 0, 255, doChange)
> r = cv2.createTrackbar('R', 'trackbar', 0, 255, doChange)
> while True:
> cv2.imshow("trackbar", img)
> k = cv2.waitKey(1)
> if k == 27:
>   break
> cv2.destroyAllWindows()
> ```





## 4 图像变换

### 4.1 色彩空间变换

常见的色彩空间包括：RGB、GRAY、XYZ、YCrCb、HSV

> 在OpenCV中，RGB颜色空间的顺序是BGR

```python
# 转换色彩空间类型
dst = cv2.cvtColor(src, code[, dstCn])
转换后的图像    转换前原图，色彩空间类型转换码，目标图像的通道数
```

> code：
>
> ```python
> cv2.COLOR_XXX2XXX
> ```

* RGB

  > Red   Green   Blue 

* GARY

  > 8位灰度空间
  >
  > $Gary = 0.299R + 0.587G + 0.114B$

* YCrCb

  > 亮度Y、红色Cr、蓝色Cb
  >
  > $Y = 0.299R + 0.587G + 0.114B$
  >
  > $Cr = 0.713(R - Y) + delta$
  >
  > $Cb = 0.564(B - Y) + delta$
  >
  > > $delta$：
  > >
  > > * 128   8位图像
  > > * 32767  16位图像
  > > * 0.5   单精度图像

* HSV

  > Hue色调   Saturation饱和度  Value亮度

### 4.2 几何变换

几何变换是指对图像的放大、缩小、选装等各种操作

#### 4.2.1 缩放

```python
# 1. 缩放
dst = cv2.resize(src,dsize[,dst[,fx[,fy[,interpolation]]]])
转换后的图像    缩放的原图，转换后的图像大小  水平方向的缩放比例，垂直方向的缩放比例，插值方式
```

> dsize不为None时：不管fx，fy的设置，都由（width，height）确定。
>
> dsize为None时：fx和fy不能为0。 宽：round(原图宽 x fx)   高：round(原图高 x fy)

> `interpolation参数`
>
> ```python
> cv2.INTER_NEAREST
> cv2.INTER_LINEAR
> cv2.INTER_CUBIC
> cv2.INTER_AREA
> cv2.INTER_LANCZOS4
> cv2.INTER_LINEAR_EXACT
> cv2.INTER_MAX
> cv2.WARR_FILL_OUTLIERS
> cv2.WARR_INVERSE_MAP
> ```

#### 4.2.2 翻转

```python
# 2. 翻转
dst = cv2.flip(src,flipCode)
                    翻转类型
```

> 0：垂直翻转
>
> 大于0：水平翻转
>
> 小于0：水平和垂直翻转

#### 4.2.3 仿射

==【原图像中的所有平行线在转换后的图像中仍然平行】==

```python
# 3. 仿射   【原图像中的所有平行线在转换后的图像中仍然平行】
# 仿射：平移、旋转、缩放    
dst = cv2.warpAffine(src,M,dsize[,dst[,flags[,borderMode[,borderValue]]]])
#                     2x3的转换矩阵     插值方式    边类型        边界值
```

> M：是一个大小为2X3的转换矩阵，使用不同的转换矩阵可实现平移、旋转等多种操作
>
> dsize：转换后的图像大小
>
> flags：插值方式。（默认：`cv2.INTER_LINEAR`）
>
> borderMode：边类型。（默认：`cv2.BORDER_CONSTANT`）
>
> borderValue：边界值。（默认：0）

```python
# 平移
m = np.float32(
    [1, 0, m],
    [0, 1, n]
)

# 缩放
m = np.float32(
    [h, 0, 0],
    [0, v, 0]
)

# 旋转
m = cv2.getRotationMatrix2D(center, angle, scale)
            原图像中作为旋转中心的坐标，旋转角度，目标图像与原图像的大小比例

# 三点映射变换
m = cv2.getAffineTransform(src, dst)
               原图像中3个点的坐标，原图像中3个点在目标图像中对应坐标
```

#### 4.2.4 透视

==【原始图像中所有直线在转换后的图像中仍然是直线】==

```python
# 4. 透视   【原始图像中所有直线在转换后的图像中仍然是直线】
m = cv2.getPerspectiveTransform(src,dst)
                   原图像中4个点的坐标，原图像中4个点在目标图像中对应坐标
```



例子：

```python
import numpy as np
import cv2

img = cv2.imread('../picture/demo.png')
sc = [1, 0.2, 0.5, 1.5, 2]
cv2.imshow('4.2', img)
height = img.shape[0]
width = img.shape[1]
while True:
    key = cv2.waitKey(10)
    if key == 48:  # 按0  [缩放]
        img1 = cv2.resize(img, None, fx=0.2, fy=0.2)
        cv2.imshow('4.2', img1)
    elif key == 49:  # 按1  [翻转]
        img1 = cv2.flip(img, 0)  # 垂直翻转
        # img1 = cv2.flip(img, 1)  # 水平翻转
        # img1 = cv2.flip(img, -1)  # 垂直水平翻转
        cv2.imshow('4.2', img1)
    elif key == 50:  # 按2  [仿射：平移]
        img1 = cv2.warpAffine(src=img,
                              M=np.float32([[1, 0, 100], [0, 1, 50]]),  # 右移100，左移50
                              dsize=(width, height))  # 转换后的图像大小
        cv2.imshow('4.2', img1)
    elif key == 51:  # 按3  [仿射：缩放]
        img1 = cv2.warpAffine(src=img,
                              M=np.float32([[0.5, 0, 0], [0, 0.5, 0]]),  # 宽高都缩小50%
                              dsize=(width, height))  # 转换后的图像大小
        cv2.imshow('4.2', img1)
    elif key == 52:  # 按4  [仿射：旋转]
        img1 = cv2.warpAffine(src=img,
                              M=cv2.getRotationMatrix2D(center=(width / 2, height / 2),  # 旋转中心坐标
                                                        angle=60,  # 旋转角度。正数逆时针，负数顺时针。
                                                        scale=0.5),  # 图像和原图像的大小比
                              dsize=(width, height))  # 转换后的图像大小
        cv2.imshow('4.2', img1)
    elif key == 53:  # 按5  [仿射：三点映射变换]
        img1 = cv2.warpAffine(src=img,
                              M=cv2.getAffineTransform(
                                  # 三个点：平行四边形左上角、右上角、左下角
                                  src=np.float32([[0, 0], [width - 10, 0], [0, height - 1]]),  # 原图像三个点
                                  dst=np.float32([[50, 50], [width - 100, 80], [100, height - 100]])),  # 在目标图像中对应的三个点
                              dsize=(width, height))  # 转换后的图像大小
        cv2.imshow('4.2', img1)
    elif key == 54:  # 按6  [透视]
        img1 = cv2.warpPerspective(src=img,
                                   M=cv2.getPerspectiveTransform(
                                       src=np.float32(
                                           [[0, 0], [width - 10, 0], [0, height - 10], [width - 1, height - 1]]),
                                       # 取四个点
                                       dst=np.float32([[50, 50], [width - 50, 80], [50, height - 100],
                                                       [width - 100, height - 10]])),  # 设置四个点在目标图像中的坐标
                                   dsize=(width, height))
        cv2.imshow('4.2', img1)
    elif key == 27:
        break
```



### 4.3 图像模糊

图像模糊（也叫**图像平滑处理**）主要处理图像中与周围差异较大的点，将其像素值调整为与周围的点像素值近似的值。

==目的：消除图像噪声和边缘==

#### 4.3.1 均值滤波

* 以当前点为中心，用其周围NXN个点的像素值的平均值来代替当前的像素值。
* 用于计算平均值的NXN个邻域
* 用于滤波计算的卷积核大小与邻域相同

```python
 dst = cv2.blur(src, ksize, [,anchor [,borderType]])
# 滤波图像结果    原图 卷积核大小    锚点   边界值处理方式  
```

> ksize：卷积核大小。表示（width, height），通常设置为相同值，且为正数和奇数
>
> anchor：锚点。默认（-1，-1）。表示锚点谓语卷积核中心

#### 4.3.2 高斯滤波

* 按像素点与中心点的不同距离，赋予像素点的权重值，越靠近中心点的权重值越大，越远离中心的权重值越小。
* 根据权重值计算邻域内所有像素点的和，将和作为中心的像素值

```python
 dst = cv2.GaussianBlur(src, ksize, sigmaX, [,sigmaY [,borderType]])
#                              水平方向上的权重值，垂直方向上的权重值        
```

> * 如果sigmaY为0，则令其等于sigmaX
>
> * 如果sigmaX和sigmaY都为0，则按下面公式计算，ksize为（width，height）
>
>   ```txt
>   sigmaX = 0.3 x ((width - 1) x 0.5 - 1) + 0.8
>   sigmaY = 0.3 x ((height - 1) x 0.5 - 1) + 0.8
>   ```

#### 4.3.3 方框滤波

* 以均值滤波为基础，可选择是否对滤波结果进行归一化
* 如果选择进行归一化，则滤波结果为邻域内点的像素值之和的平均值
* 否则滤波结果为像素之和

```python
 dst = cv2.boxFilter(src, ddepth, ksize, [,anchor [,normalize [,borderType]]])
#                       目标图像的深度             True时执行归一化操作   
```

> ddepth：目标图像的深度。（-1表示与原图像的深度一致）
>
> normalize：（True：执行归一化。默认）  （False：不执行）

#### 4.3.4 中值滤波

* 将邻域内的所有像素值排序，取中间值作为邻域中心的像素值

```python
dst = cv2.medianBlur(src, ksize)
```

> ksize：卷积核大小。必须是大于1的奇数。

#### 4.3.5 双边滤波

* 计算像素值的同时会考虑 **距离和色差** 信息，从而可在消除噪声的同时保护边缘信息。
* 在执行双边滤波操作时，如果像素点与当前点色差较小，赋予其较大的权重值，否则赋予其较小的权重值。

```python
 dst = cv2.bilateralFilter(src, d, sigmaColor, sigmaSpace [,borderType])
#                       以当前点为中心的邻域的直径，双边滤波选择的色差范围，空间坐标中sigma值
```

> d：一般为5
>
> sigmaColor：双边滤波选择的色差范围
>
> sigmaSpace：空间坐标中sigma值。值越大表示越多的像素点参与滤波计算。
>
> > 当 d > 0：忽略sigmaSpace，由 d 决定邻域大小
> >
> > 否则d由sigmaSpace计算得出，与sigmaSpace成比例。

#### 4.3.6 2D卷积

```python
 dst = cv2.filter2D(src, ddepth, kernel [,anchor [,delta [,borderType]]])
#                     目标图像的深度，单通道卷积核，图像处理的锚点，修正值，边界值处理方式
```

> ddepth：目标图像dst的深度。一般用-1表示与原图像src一致
>
> kernel：单通道卷积核（一维数组）
>
> anchor：图像处理的锚点
>
> delta：修正值。未省略时，将加上该值作为最终的滤波结果。
>
> borderType：边界值处理方式





### 4.4 阈值处理

* 阈值处理用于剔除图像中像素值高于或者低于指定值的像素点

#### 4.4.1 全局阈值处理

* 将大于阈值的像素值设置为255，将其他像素值设置为0

* 将大于阈值的像素值设置为0，将其他像素值设置为255

```python
#  全局阈值处理后的结果图像     是阈值类型为THRESH_BINARY和THRESH_BINARY_iNV时使用的最大值                  
  retval, dst = cv2.threshold(src, thresh, maxval, type)
# 返回的阈值                   原图像 设置的阈值       阈值类型
```

**1. 二值化阈值处理**

>  将==大于==阈值的像素值设置为255，将其他像素值设置为0

```python
retval, dst = cv2.threshold(src, thresh, maxval, cv2.THRESH_BINARY)
```

**2. 反二值化阈值处理**

>  将==大于==阈值的像素值设置为0，将其他像素值设置为255

```python
retval, dst = cv2.threshold(src, thresh, maxval, cv2.THRESH_BINARY_INV)
```

**3. 截断阈值处理**

> 将==大于==阈值的像素值设置为阈值，其余像素值保持不变

```python
retval, dst = cv2.threshold(src, thresh, maxval, cv2.THRESH_TRUNC)
```

**4. 超阈值零处理**

>  将==大于==阈值的像素值设置为0，其余像素值保持不变

```python
retval, dst = cv2.threshold(src, thresh, maxval, cv2.THRESH_TOZERO_INV)
```

**5. 低阈值零处理**

>  将==小于==阈值的像素值设置为0，其余像素值保持不变

```python
retval, dst = cv2.threshold(src, thresh, maxval, cv2.THRESH_TOZERO)
```

**6. Otsu算法阈值处理**

> 对于色彩不均衡的图像，这样处理更好，他会遍历当前图像的所有阈值，再选择最佳阈值

```python
retval, dst = cv2.threshold(src, thresh, maxval, 阈值类型 + cv2.THRESH_OTSU)
```

**7. 三角算法阈值处理**

> 

```python
retval, dst = cv2.threshold(src, thresh, maxval, 阈值类型 + cv2.THRESH_TRIANGLE)
```



#### 4.4.2 自适应阈值处理

* 也称 **局部阈值处理**
* 通过计算每个像素点邻域的加权平均值来确定阈值，并用该阈值处理当前像素点
* <u>全局阈值处理</u>适用于 **色彩均衡的图像**，<u>自适应阈值处理</u>适用于 **明暗差异较大的图像**

```python
     dst = cv2.adaptiveThreshold(src, maxValue, adaptiveMethod, thresholdType, blockSize, C)
#阈值处理的结果图像                 原图像   最大值      自适应方法      阈值处理方式   计算局部阈值的邻域大小  常量
```

> 自适应方法：
>
> * cv2.ADAPTIVE_THRESH_MEAN_C（邻域中所有像素点的权重值相同）
> * cv2.ADAPTIVE_THRESH_GAUSSIAN_C（邻域中所有像素点的权重值与其到中心点的距离有关，通过高斯方程可计算各个点的权重值）
>
> 阈值处理方式：
>
> * cv2.THRESH_BINARY（二值化阈值处理）
> * cv2.THRESH_BINARY_INV（反二值化阈值处理）
>
> C：常量。自适应阈值为blockSize指定邻域的加权平均值减去C



### 4.5 形态变换

* 主要用于二值图像的形状操作，实现原理基于数字形态学
* 数字形态学也成形态学，它主要从图像内部提取信息来描述图像形态

#### 4.5.1 形态操作内核

```python
 retval = cv2.getStructuringElement(shape, ksize)
#                                   内核形状 内核大小（行数,列数）
```

> cv2.MORPH_RECT	矩形
>
> cv2.MORPH_CROSS 	十字形
>
> cv2.MORPH_ELLIPSE 	椭圆形

#### 4.5.2 腐蚀

> 取最小值 
>
> 会使白色区域的边缘像素值减少，从而使白色区域的面积减少
>
> 迭代次数越多，腐蚀效果越明显
>
> 内核越大，腐蚀效果越明显

```python
dst = cv2.erode(src, kernel[, anchor[, iterations[, borderType[, borderValue]]]])
```

> src：原图像
>
> kernel：内核。默认3x3全1的矩阵
>
> anchor：锚点。默认（-1，-1），表示锚点为内核中心
>
> iterations：迭代次数。默认1
>
> borderType：边界类型。默认BORDER_CONSTANT
>
> borderValue：边界值。

#### 4.5.3 膨胀

> 取最大值
>
> 会使白色区域的边缘像素值增大，从而使白色区域的面积增大
>
> 迭代次数越多，膨胀效果越明显
>
> 内核越大，膨胀效果越明显

```python
dst = cv2.dilate(src, kernel[, anchor[, iterations[, borderType[, borderValue]]]])
```

#### 4.5.4 高级形态操作

```python
dst = cv2.morphologyEX(src, op, kernel [,anchor [,iterations [,borderType [,borderValue]]]])
```

> op：形态操作类型
>
> > ```python
> > op = cv2.MORPH_OPEN   # 开运算 [先腐蚀再膨胀]
> > op = cv2.MORPH_CLOSE  # 闭运算 [先膨胀再腐蚀]
> > op = cv2.MORPH_GRADIENT # 形态学梯度运算 [膨胀减去腐蚀]
> > op = cv2.MORPH_BLACKHAT # 黑帽运算 [闭运算减去原图像]
> > op = cv2.MORPH_TOPHAT   # 礼帽运算 [原图像减去开运算]
> > ```

> * 开运算：去除图像中的噪声，消除较小连通域，保留较大连通域
> * 闭运算：去除连通域的小型空间，平滑物体轮廓，连接两个临近的连通域





## 5 边缘和轮廓

* 图像的边缘是指图像中灰度值发生急剧变化的位置
* 边缘检测的目的是唯一绘制出边缘线条

### 5.1 边缘检测

#### 5.1.1 Lapacian边缘检测 

> 拉普拉斯边缘检测

> * 使用 **图像矩阵** 与 **拉普拉斯核** 进行卷积运算
> * 本质是计算图像中任意一点与其在水平方向和垂直方向上4个相邻点平均值的差值

```python
dst = cv2.Laplacian(src, ddepth [,ksize [,scale [,delta [,borderType]]]])

# 边缘检测结果图像 = cv2.Laplacian(原图像, 目标图像的深度 [,用于计算二阶导数滤波器的系数（正数奇数） [,可选比例因子 [,添加到边缘检测结果中的可选增量值 [,边界值类型]]]])
```

#### 5.1.2 Sobel边缘检测

> * 将 **高斯滤波** 和 **微分** 结合起来执行图像卷积运算
> * 结果具有一定的抗噪性

```python
dst = cv2.Sobel(src, ddepth, dx, dy [,ksize [,scale [,delta [,borderType]]]])

# 边缘检测结果图像 = cv2.Laplacian(原图像, 目标图像的深度, 导数x的阶数, 导数y的阶数 [,扩展的Sobel内核大小（1357） [,计算导数的可选比例因子 [,添加到边缘检测结果中的可选增量值 [,边界值类型]]]])
```

#### 5.1.3 Canny边缘检测

> 1. 使用高斯滤波去除图像噪声
> 2. 使用sobel核进行滤波，计算梯度
> 3. 在边缘使用非最大值抑制
> 4. 对检测出的边缘使用双阈值以去除假阳性
> 5. 分析边缘之间的连续性，保留真正的边缘，消除不明显的边缘

```python
dst = cv2.Canny(src, threshold1, threshold2 [,apertureSize [,L2gradient]])

# 边缘检测结果图像 = cv2.Laplacian(原图像, 第1阈值, 第2阈值 [,计算梯度时使用的Sobel核大小 [,标志]])
```





### 5.2 图像轮廓

#### 5.2.1 查找轮廓

> 从 **二值图像** 中查找图像轮廓

```python
contours, hierarchy = cv2.findContours(image, mode, method [,offset])

# 返回的轮廓，返回的轮廓的层次结构 = cv.findContours(原图像，轮廓的检索模式，轮廓的近似方法 [,每个轮廓点移动的可选偏移量])
```

> * 返回结果：返回一个list对象，保存了轮廓数组。轮廓数组的每个元素都是一个表示轮廓的array对象；返回的轮廓层次是一个numpy.ndarray对象
>
> * 轮廓层次：根据轮廓的嵌套关系，可将轮廓之间的层次关系分为父级和子级，外部的轮廓为父级，内部轮廓为子级。[下一个轮廓   前一个轮廓   第一个子级轮廓   父级轮廓]
>
> * 轮廓的检索模式：
>
>   ```python
>   cv2.RETR_LIST：仅检索所有轮廓，不创建任何父子关系
>   cv2.RETR_EXTERNAL:仅检索所有的的外部轮廓，不包含子集轮廓
>   cv2.RETR_CCOMP:检索所有的轮廓并将他们排列为2级层次结构，所有的外部轮廓为1级，所有的子级轮廓为2级
>   cv2.RETR_TREE：检索所有轮廓并创建完整的层次列表
>   ```
>
> * 轮廓的近似方法：
>
>   ```python
>   cv2.CHAIN_APPROX_NONE：存储所有轮廓点，轮廓的任意两个相邻点是水平、垂直或对角线上的邻居
>   cv2.CHAIN_APPOX_SIMPLE:只保存水平、垂直和对角线的端点
>   cv2.CHAIN_APPROX_TC89_L1：应用Teh-Chin链逼近算法中的一种确定轮廓点
>   ```

> ```python
> # 例子：查找轮廓
> import cv2
> import numpy as np
> 
> img = cv2.imread("../picture/five.png")
> cv2.imshow('original', img)
> gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
> ret, img2 = cv2.threshold(gray, 125, 255, cv2.THRESH_BINARY)
> c, h = cv2.findContours(img2, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)
> print('轮廓：', c)
> print('轮廓类型：', type(c))
> print('轮廓个数：', len(c))
> print('层次：', h)
> print('层次类型：', type(h))
> for n in range(3):
> img3 = np.zeros(img.shape, np.uint8) + 255
> cv2.polylines(img3, [c[n]], True, (255, 0, 0), 2)
> cv2.imshow('%s' % n, img3)
> cv2.waitKey(0)
> cv2.destroyAllWindows()
> ```

#### 5.2.2 绘制轮廓

```python
image = cv2.drawContours(image, contours, contourIdx, color [,thickness [,lineType [,hierarchy [,maxLevel [,offset]]]]])

# image = cv2.drawContours(在其中绘制轮廓的图像, 要绘制的轮廓, 要绘制的轮廓的索引, 轮廓颜色 [,画笔的粗细 [,使用的线型 [,对应cv2.findContours()函数返回的轮廓层次 [,可绘制的最大轮廓层次深度 [,绘制轮廓的偏移位置]]]]])
```

#### 5.2.3 轮廓特征

1. **轮廓的矩：**

   > 轮廓的各种几何特征：面积、位置、角度、形状

   ```python
   ret = cv2.moents(array [,binaryImage])
   
   # 轮廓距 = cv2.moents(轮廓的数组 [,True时，会将array对象中的所有非0值设置为1])
   ```

   > ret: 返回轮廓矩【字典】。零阶矩表示轮廓的面积
   > array：轮廓的数组
   > binarylmage：True：会将array对象中的所有非0值设置为1

2. **轮廓的面积**

   ```python
   ret = cv2.contourArea(contour [,oriented])
       
   # 返回的面积 = cv2.contourArea(轮廓 [,True返回值的正负表示顺逆时针，False表示返回值为绝对值])
   ```

3. **轮廓的长度**

   ```python
   ret = cv2.arcLength(contour,closed)
   
   # 返回的长度 = cv2.arcLength(轮廓, True表示轮廓是封闭的)
   ```

4. **轮廓的近似多边形**

   ```python
   ret =  cv2.approxPolyDP(contour, epsilon, closed)
   ```

   > ret: 返回的近似多边形
   > contour：轮廓
   > epsilon：精度。表示近似多边形接近轮廓的最大距离
   > closed：布尔值。True：表示轮廓是封闭的

5. **轮廓的凸包**

6. **轮廓的直边界矩形**

7. **轮廓的旋转矩形**

8. **轮廓的最小外包园**

9. **轮廓的拟合椭圆**

10. **轮廓的拟合直线**

11. **轮廓的最小外包三角形**

### 5.3 霍夫变换

#### 5.3.1 霍夫直线变换

```python
# 利用霍夫变换算法检测图像中的直线
lines = cv2.HoughLines(image, rho, theta, threshold)
```

```python
# 利用概率霍夫变换算法来检测图像中的直线
lines = cv2.HoughLinesP(image, rho , theta, threshold [,minLineLength[,maxLineGap]])
```

#### 5.3.2 霍夫圆变换









5.3 霍夫变换
    5.3.1 霍夫直线变换
        

    5.3.2 霍夫圆变换

​            ret：面积
​            contour：轮廓
​            oriented：True：返回的正与负表示轮廓是顺时针还是逆时针；  False：返回绝对值
​    轮廓的长度：
​        
​            ret：返回的长度
​            contour：轮廓
​            closed：布尔值。True：表示轮廓是封闭的
​    轮廓的近似多边形
​    
​            



# 五、类库

## 1 turtle

turtle库：	海龟 	turtle绘图体系的Python实现
	
turtle绘图体系：	1969年诞生	主要用于程序入门设计

库：
	python计算生态 = 标准库 + 第三方库
	标准库：随解释器直接安装到操作系统中的功能模块
	第三方库：需要经过安装才能使用的功能模块

turtle的绘图窗体：
	turtle.setup(width,height,startx,starty)
	                        长         高     内宽    内高          

      	1. setup()设置窗体大小及位置
          2. 4个参数中后两个可选  （默认正中心）
          3. setup()不是必须的
             #屏幕左上角（0，0）
             #窗体左上角（startx，starty）


turtle空间坐标系：
	turtle.goto(x, y)	【绝对坐标】
	                  x轴  y轴
	turtle.bk(d)	【后退方向】
	turtle.fd(d)	【前进方向】
	turtle.circle(r,angle)	【左侧点为圆心，曲线运行】

```txt
	     左侧方向
后退方向		    前进方向
	     右侧方向
```

turtle角度坐标体系：
	turtle.seth(angle)	【绝对角度】

	1. seth()改变海龟行进方向
	2. setch()只改变方向但不行进
	3. angle为绝对度数

```txt
	      90/-270
180/-180		     0/360
	      270/-90
```

		turtle.left(angle)
	------	    【海龟角度】	------
		turtle.right(angle)


RGB色彩体系：（红绿蓝）
	 有三种颜色构成的万物色：
		整数：0-255	小数：0-1（默认）

```python
turtle.colormode(mode)	#1.0  小数模式	255  整数模式

white	255,255,255		1,1,1	白色
yellow	255,255,0		1,1,0	黄色
magenta	255,0,255		1,0,1	洋红
cyan	0,255,255		0,1,1	青色
bule	0,0,255			0,0,1	蓝色
black	0,0,0			0,0,0	黑色
```

库引用：（ <a>.<b>() ）

​		import <库名>
​			<库名>.<函数名>(<函数参数>)
​	
​		from <库名> import <函数名>
​		from <库名> import *
​		<函数名>(<函数参数>)

​		import <库名> as <库别名>
​		<库别名>.<函数名>(<函数参数>)

turtle画笔控制函数：（成对出现）
	turtle.penup()	=>	turtle.pu()	抬起画笔，海龟在飞行
	turtle.pendown()	=>	turtle.pd()	落下画笔，海龟在爬行
	turtle.pensize(width)   =>	turtle.width(width)	画笔的宽度，海龟的腰围
	turtle.pencolor(color)    =>	(颜色字符串/RGB的小数值/RGB的元祖值)

运动控制函数：（走直线 & 走曲线）
	turtle.forward(d)	===>	turtle.fd(d)	向前行进，海龟走直线（d：正负值）
	turtle.circle(r,extend=None)	 (半径，绘制的弧度)


方向控制函数：（绝对角度 & 海龟角度）
	turtle.setheading(angle)	===>	turtle.seth(angle)	改变行进方向，海龟走角度
	turtle.left(angle)	海龟向左转
	turtle.right(angle)	海龟向右转


循环语句：
	for <变量> in range(<参数>)
		<被循环执行的语句>

range()函数：
	range(N)		产生0到N-1的整数序列，共N个
	range(M,N）	产生M到N-1的整数序列，共N-M个
	

	range(5)	   ===>  0,1,2,3,4,
	range(2,5)  ===>  2,3,4

turtle.done()：
	程序运行结束，窗体不会自动退出，需要手动退出





# pytorch



## 1. 深度学习框架

### 1.1 发展

* 2002	Torch
* 2011    Torch7
* 2016
* 2018.12
* 2019.5



### 1.2 同类框架

* Google
  * theano
  * **TensorFlow ** （静态图）
  * Keras
* Facebook
  * Torch 7 
  * Caffe
  * **pytorch** + caffe2  （动态图）
* Amazon
  * mxnet



### 1.3 pytorch生态

* PyTorch NLP
* Allen Nlp
* TorchVision
* PyTorch geometric
* Fast.ai
* ONNX



## 2 安装

### 2.1 安装Anaconda

### 2.2 NVIDIA显卡

1. 百度搜索：cuda download

2. 进入官网：[CUDA Toolkit 12.1 Downloads | NVIDIA Developer](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10)

   * windows
   * x86_64
   * 11
   * exe（local）
   * Download

   ```window
   mvcc -V
   ```

### 2.3 安装pytorch

### 2.4 安装PyCharm

```python
# 测试
import torch
print(torch.__version__)
print('gpu:',torch.cuda.is_available())
```



## 3 回归问题

