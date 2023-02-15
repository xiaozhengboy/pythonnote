[toc]





# python基础

author：小政





## 1 前言

python：

* 解释型语言
* 动态语言
* 动态类型语言
* 强类型语言
* 面向对象程序设计



1989	有想法

1991	第一个python诞生



## 2 安装

地址：[Welcome to Python.org](https://www.python.org/)

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







## 3 向世界说你好

```python
print("Hello World!!")
```



## 4 储备知识

python解释器：   **python.exe**

```txt
想法 ==编写==》 python代码 ==》python解释器 ==翻译==》0101二进制 ==提交==》执行
```



## 5 PyCharm

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



## 6 基础语法

### 6.1 字面量

在代码中，被写下来的固定的值，称为字面量



| 类型               | 描述                                           | 说明 |
| ------------------ | ---------------------------------------------- | ---- |
| 数字（ Number）    | 整数（int)  浮点数 float 复数 complex 布尔bool |      |
| 字符串（String）   | 描述文本                                       |      |
| 列表（List）       | 有序 可变                                      |      |
| 元组（Tuple）      | 有序 不可变                                    |      |
| 字典（Dictionary） | 无序 键值对                                    |      |
| 集合（Set）        | 无序 不重复                                    |      |

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

### 6.2 注释

```python
# 单行注释

'''
多行注释
'''
```

>  单行注释：单行代码；一小段代码
>
>  多行注释：整个python代码文件；类；方法



### 6.3 变量

变量的名称  = 变量的值



### 6.4 标识符

英文	中文	数字	下划线（_）

1. 不推荐使用中文；不能以数字开头
2. 大小写敏感
3. 不能使用关键字



规范：

1. 见名知意
2. 下划线命名法
3. 英文字母全小写



### 6.5 运算符

```python
# 算术运算符
正（+）负（-）
加（+）减（-）乘（*）除（/）
整除（//）取余（%）幂（**）
```

```python
# 关系运算符（比较运算符）
等于（==）不等于（!=）
大于（>）小于（<）
大于等于（>=）
小于等于（<=）
```

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

```python
# 位运算符
&		# 按位与	111
|		# 按位或	101
^		# 按位异或	101
~		# 按位取反	10 01
<<		# 左移动	
>>		# 右移动
```

```python
# 逻辑运算符
and		# 与运算
or		# 或运算
not		# 非运算
```

```python
# 成员运算符
in		# 如果在指定序列中找到值，True
not in	# 如果在指定序列中没有找到值，True
```

```python
# 三目运算符
表达式1 if 判断条件 else 表达式2
```



### 6.6 数据输入

```python
input("请告诉我你是谁？")
```



### 6.7 随机函数

```python
import random

random()	# [0,1.0)  随机浮点数
uniform(a,b)   # [a,b)  随机浮点数
randint(a,b)  # [a,b]  随机整数
randrang([start],stop[,step])   # 整数  range()
choice(seq)   # 从列表seq中，随机取一个
choices(seq,k)   # 从列表seq中，随机取k个
shuffle(x)   # 洗牌
sample(seq,k) # 从列表seq中，随机取k个。不会修改原有序列
```



### 6.8 ASCII码表

* 0-9	48-57
* A-Z    65-90
* a-z     97-122







## 7 数据类型

![image-20221220233302667](D:\Typora\picture\image-20221220233302667.png)

### 7.0 数据类型知识

```python
type("小政")   # String
```

> type(变量)   查看变量存储的数据类型

```python
int(X)	# 将x转换为一个整数
float(x)   # 将x转换为一个浮点数
str(x)   # 将对象x转换为一个字符串

long(x)
complex(real[,imag])
repr(x)   # 字符串表达式
eval(str)   # 评估函数
tuple(s)   # 元组
list(s)   # 列表

chr(x)   # 整数->字符
unichr(x)  # 整数->unicode字符
ord(x)   # 字符->整数

hex(x)   # 16
oct(x)   # 8
```

> 任何类型都可以转字符串
>
> 浮点数转整数会丢失精度

### 7.1数值型



### 7.2 布尔型



### 7.3 字符串

**==只可以存储字符串、长度任意、支持下标索引、允许重复字符串存在、不可以修改、支持for循环==**

#### 7.3.1 字符串定义

```python
name = 'lizhengzhen'
name = "lizhengzhen"
name = """li   zheng   zhen"""
```

#### 7.3.2 格式化输出

```python
print("姓名：",name)
print("姓名：" + name)
print("姓名：%s，年龄：%d，分数：%f"%(name,age,score))
print(f"姓名{name}")
```

> m.n
>
> m：控制宽度      %5d：  【】【】【】11
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

##### 7.3.2.1 .format()

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

#### 7.3.3 切片

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

#### 7.3.4 常用方法

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

#### 7.3.5 常量

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



### 7.4 列表

**==有序、任意数量元素、允许重复元素、可修改==**

#### 7.4.1 创建

```python
ls = []   # 空列表
ls = list()  # 空列表 
```

```python
ls = ['xiao','zheng',2001]    # 可以存储混合类型
```

> 1. 列表索引从0开始
> 2. 元素个数没有限制
> 3. 可以存储整数、小数、字符串、列表、元组等任何数据类型的数据，并且同一个数据列表中元素的类型可以不同

#### 7.4.2 增删改查

```python
# 增
ls.append("666")   # 尾插   一整个插入
ls.extend(['0','1','2'])   # 尾插   一个一个插
ls.insert(4,'3')   # 指定下标插
```

```python
# 删
ls.remove('3')   # 删除第一次
ls.pop()   # 弹出最后一个
ls.clear()   # 清空列表
del ls[0]  # 删除下标
del ls[1:3]  # 删除切片
```

```python
# 改 
ls.copy()   # 复制
ls[0] = 'xiao'
```

```python
# 查
print(ls[0])   # xiao
print(ls[::-1])  # [2001,'zheng','xiao']    # 支持切片
ls.index('666')  # 返回666第一次出现的下标，没有则报错
```

```python
# 拓展
len([1,2,3])    # 3
[1,2,3]+[4,5,6]   # [1,2,3,4,5,6]
['xiao']*2    #['xiao','xiao']
3 in [1,2,3]  # True
for i in [1,2,3]: print(i)    # 1 2 3
```

#### 7.4.3 函数

| 函数                            | 功能                                 | 说明                  |
| ------------------------------- | ------------------------------------ | --------------------- |
| list（seq）                     | 元组转为列表                         |                       |
| all（iterable）                 | 都是真，True                         |                       |
| any（iterable）                 | 一个真，True                         |                       |
| len（s）                        | 求个数                               |                       |
| max（iterable）                 | 最大元素                             |                       |
| min（iterable）                 | 最小元素                             |                       |
| sorted（iterable）              | 排序                                 |                       |
| sum（iterable[，start]）        | 求和                                 |                       |
|                                 |                                      |                       |
| append（x）                     | 追加到末尾                           |                       |
| extend（x）                     | 添加到末尾                           |                       |
| insert（i，x）                  | 指定下标i插入x                       |                       |
| remove（x）                     | 删除第一个x                          | 没有则报错            |
| pop（[i]）                      | 弹出第i个元素并返回它,默认弹最后一个 | 会修改原列表          |
| index（x）                      | 返回第一个x的下标                    | 没有则报错            |
| count（x）                      | 返回x的次数                          |                       |
| sort（cmp，key，reverse=False） | 排序                                 | Flase：升序True：降序 |
| reverse（）                     | 逆置                                 |                       |

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





### 7.5 元组

**==有序、任意数量元素、允许重复元素、不可修改、支持for循环==**

元组一旦定义完成，不可以修改

> 当我们需要在程序内封装数据，又不希望封装的数据被篡改，那么元组就非常合适了。

#### 7.5.1 创建

```python
tup = ()   # 空元组
tup = tuple()   # 空元组
```

```python
t = (100,)
t = ('xiao','zheng',2001)
t = 'a','b','c','d'
```

#### 7.5.2 增删改查

```python
# 增
t = t1 + t2
```

```python
# 删
```

```python
# 改 
```

```python
# 查
print(t[0])   #  下标查
print(t[1:])   # 支持切片
ls.index('666')  # 返回666第一次出现的下标，没有则报错
```

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



### 7.6 字典

**==支持for循环==**

#### 7.6.1 创建

```python
d = {}   # 空字典
d = dict()   # 空字典
```

```python
d = {'name':"小政",'age':'22'}
d = dict('name'='小政','age'='22')

d = dict([(),()])
d = dict([[],[]])
d = dict(((),()))
d = dict(([],[]))

d = dict(zip(['name','age'],['小政',22]))
```

```python
d.fromkeys(seq,value)   # 列表  值          #  d.fromkeys(list,10)
```

#### 7.6.2 增删改查

```python
# 增
d1.update(d2)   # 字典合并。d2的键值对添加到d1
d[key] = value   # 添加键值对
d.copy()   # 复制
```

```python
# 删
del d   # 删除字典
del d[key]   # 删除指定元素
d.pop(key)   # 删除指定元素
d.popitem()  # 删除最后一个元素，并且以元组形式返回。     # ('age',22)
d.clear()    # 清空字典
```

```python
# 改 
d[key] = value
```

```python
# 查
d['name']    # '小政'
d.get(key)   # 获取指定键对应的值。键不存在不报错。
d.setdefault(key,value)   # 获取指定键对应的值。键不存在添加值。
d.values()   # 获取所有键对应的值。列表形式。
d.keys()    # 获取所有键。列表形式。
d.items()   # 遍历字典。[(键,值),(键,值),(键,值)]
```

```python
# 拓展
len(d)   # 键的个数

# 当键为整数时
max(d)  # 键的最大值
min(d)  # 键的最小值
```



### 7.7 集合

**==无序、任意数量元素、不允许重复元素、可修改、支持for循环==**

#### 7.7.1 创建

```python
s = set()   # 空集合
```

```python
s = {'xiao','zheng'}
s = {1,2,3,4,5}
s = set('abcdef')   # {'a','b','c','d','e','f'}
```

#### 7.7.2 增删改查

```python
# 增
s.add(100)    # 添加元素 （会去重）
s.update([100,200])   # 添加序列
```

```python
# 删
s.remove('3')   # 删除3，不存在则报错
s.pop()   # 随机取出一个元素，原集合改变
s.discard(3)   # 删除3，不存在不报错
s.clear()   # 清空
del s	# 删除集合
```

```python
# 改 
```

```python
# 查
```

```python
# 拓展
len(s)   # 集合元素个数
'xiao' in set_name
'xiao' not in set_name
```

#### 7.7.3 集合间运算

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



### 7.8 五种类型比较

* 列表：一批数据，可修改，可重复
* 元组：一批数据，不可修改，可重复
* 字符串：一串字符串
* 集合：一批数据，去重
* 字典：一批数据，根据key检索value

![五种类型比较](D:\Typora\picture\image-20221222000148063.png)



### 7.9 推导式

```python
# 列表推导式
ls = [i for i in range(10)]
ls = [i for i in range(0,10,2)]
ls = [i for i in range(10) if i % 2 == 0]
ls = [(i,j) for i in range(1,3) for i in range(3)]
```

```python
# 字典推导式
d = {i: i**2 for i in range(1,5)}
d = {list1[i]: list2[i] for i in range(len(list1))}
c = {key: value for key, value in counts.items() if value >= 200}
```

```python
# 集合推导式
s = {i ** 2 for i in list1}
```





## 8 流程控制

### 8.1 顺序结构

```txt
自上而下，逐行执行。
```



### 8.2 选择结构

#### 8.2.1 if

```python
if 表达式:
    语句块
```

#### 8.2.2 if-else

```python
if 表达式:
    语句块1
else:
    语句块2
```

#### 8.2.3 if-elif-else

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

#### 8.2.4 if 嵌套

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



### 8.3 循环结构

#### 8.3.1 for循环

```python
for 循环变量 in 序列:
    语句块
```

#### 8.3.2 while循环

```python
while 表达式:
    语句块
```

#### 8.3.3 含else

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

#### 8.3.4  break和continue语句

```python
break   # 跳出循环体
continue  # 结束本次循环，开始下次循环
```





​	

## 9 函数

函数：组织好的、可重复使用的、用来实现特定功能的代码块

使用函数的好处：

+ 将功能封装在函数内，可供随时随地地重复利用

+ 提高代码的复用性，减少重复代码，提高开发效率

  

### 9.1 自定义函数

#### 9.1.1 函数的定义

```python
def 函数名(参数列表):
    代码段
    [return [返回值]]
```

> 即使没参数，小括号也不能省。否则报错**invalid syntax**

> 形参列表：用于指明改参数可以接收多少个参数。多个参数，“,”分隔

> 返回一个值 ，也可以返回多个值    
>
> ```python
> def demo():
>  return 1,'xiao',True
> 
> x,y,z = demo()
> ```
>
> 函数体在遇到return后就结束了，所以写在return后的代码不会执行
>
> 默认返回None

```python
def 函数名(形参,形参=n):
    语句块
```

> 指定默认值的形参必须放在所有形参的最后

#### 9.1.2 函数的调用

```txt
[变量] = 函数名([实参])
```

> 定了多少个形参，就要传多少个实参，且顺序一致

#### 9.1.3 参数传递

参数传递方式有两种：

* 值传递：适用于实参类型为不可变类型（字符串，数字，元组）
* 引用传递：适用于实参类型为可变类型（列表，字典）

> 严格说是：传递不可变对象 和 传递可变对象

在python中，类型属于对象，变量是没有类型的。

```python
# 关键字传参
def demo(name,age,gender):
    print(f'姓名：{name}，年龄：{age}，性别：{gender}')

demo('xiaozheng','22','男')
demo(name="xiaozheng",gender='男',age='22')     # 顺序可以改变
```

```python
# 缺省参数
def demo(name,age,gender='男'):      # 默认值参数放最后
    print(f'姓名：{name}，年龄：{age}，性别：{gender}')

demo('xiaozheng','22','男')
demo('xiaozheng','22')      # 默认值参数可以省
```

```python
# 不定长参数（位置传递）
def demo(*args):       # 一个星号
    print(args)

# 所有参数都被args收集，根据位置合并为一个元组。
demo('xiaozheng','22','男')
# 列表传入
ls = ['xiaozheng','22','男']
demo(*ls)
# 元组传入
t = ('xiaozheng','22','男')
demo(*t)
```

```python
# 不定长参数（关键字传递）
def demo(**kwargs):       # 两个星号
    print(kwargs)
    
# 参数是“键=值”形式，都被kwargs接收，组成字典
demo(name="xiaozheng",gender='男',age='22')      
# 字典传入
d = {'name': "xiaozheng", 'gender': '男', 'age': '22'}
demo(**d)
```

```python
# 命名关键字参数
def demo(name,*,age,sex):    # *后面的被视为关键字
    pass

demo('小政',age=22,sex='男')   # 传不够会报错
```

#### 9.1.4 函数的嵌套

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

#### 9.1.5 函数的递归

```python
def test(num):
    if num == 1:
        result = 1
    else:
        result = test(num - 1) * num
    return result

print(test(5))
```

#### 9.1.6 函数的说明文档

```python
def func(x,y):
    """
    函数说明
    :param x:   解释参数
    :param y:   解释参数
    :return:  解释返回值
    """
    函数体
    return 返回值
```

```python
help(函数名)   # 查看函数的说明文档
```



### 9.2 变量的作用域

#### 9.2.1 局部变量

在函数内定义的变量称为局部变量

它只在函数内部有效，当函数被调用完毕后，该变量就不存在了。

#### 9.2.2 全局变量

在函数外定义的变量称为全局变量

它在整个代码中都有效，无论在函数内使用，还是在函数外使用

#### 9.2.3 global

```python
# 在函数内修改全局变量
s = "小政加油"
def demo():
    global s
    s =  '小政好帅'
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



### 9.3 匿名函数

```python
lambda 参数: 语句块
```

> 没有函数名，且代码只能写成一行。



### 9.4 高级函数

```python
map(function,sequence)
```

> 遍历序列sequence，对序列每个元素都进行函数function操作，返回新序列

```python
reduce(function,sequence)
```

> 累积

```python
filter(function,sequence)
```

> 过滤
>
> 序列或支持迭代的容器火迭代器sequence中的每个元素都进行function的筛选，返回True的元素



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
>  s = int(input("请输入你的年龄："))
>  assert s > 0, "输入的年龄大于0"
>  print(s)
> except Exception as result:
>  print('捕捉到的异常：', result)
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





## 12 模块

### 12.1 导入模块

```python
[from 模块名] import [模块| 类 | 变量 | 函数 | * ] [as 别名]
```

> 写在开头部分

### 12.2 自定义模块

```python
# 文件名1.py

__all__ = ['test1']

def test1(a,b):
    print(a+b)
    
def test2(a,b):
    print(a-b)
 
if __name__ = '__main__'
    test1(3,2)
    
# 文件名2.py
import 文件名1
from 文件名1 import *    

文件名1.test(10,20)
```



## 13 包

### 13.1 创建包

就是一个文件夹，只是里面必须有`__init__.py`

```python
# __init__.py			# 文件夹T
__all__ = ['test1']
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
t1.test1(10,20)


from T.test1 import test1
test1(10,20)
```

### 13.2 导入包

```python
#导入包
import 包名.模块名
from 包名 import *

包名.模块名.目标
```

### 13.3 安装第三方包

```linux
pip install 包名称
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple 包名称
```





## 14 面向对象程序设计

面向对象程序设计有三大特征：封装性、继承性、多态性

* 面向过程开发
* 面向对象开发

### 14.1 类和对象

```python
# 类
class 类名:
    类的属性
    类的方法
```

```python
# 对象
对象名 = 类名()
对象名.新的属性名 = 值
```

> 例子
>
> ```python
> class Car:
> def move(self):
>   print("车在奔跑")
> 
> def toot(self):
>   print("车在鸣笛")
> 
> 
> jeep = Car()
> jeep.color = '黑色'
> jeep.move()
> jeep.toot()
> print(jeep.color)
> 
> print(jeep)    # 打印对象 <__main__.Car object at 0x16进制内存地址>
> addr = id(jeep)
> print("%d"%addr)  # 10进制
> print("%x"%addr)  # 16进制
> ```

> 类是封装对象属性和行为的载体。具有相同属性和行为的实体被抽象为类。
>
> * [数据成员]: 在类中定义的变量（属性）
>
>   * [类属性]:定义在类中，但在方法外
>
>   * [实例属性]:定义在类的方法中
>
> * [方法成员]: 类中的定义函数

> 类名：名字（满足**大驼峰命名法**[^1]）
>
> 属性：特征
>
> 方法：行为

[^1]: 每一个单词的首字母大写，单词与单词之间没有下划线

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



### 14.2 构造方法

固定名称：`__init__()`

当创建类的实例的时候，系统会自动调用构造方法，从而实现类进行初始化的操作

```python
def __init__(self):
    self.name = '小政'    # 在初始化方法内部定义属性
    
demo = Demo()
-----------------------------------  
def __init__(self,name,color):
    self.name = name   # 初始化的同时设置初始值
    self.color = color
    
demo = Demo(name,color)
```



### 14.3 析构方法

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



### 14.4 self

方法的定义中，第一个参数永远是`self`

self：也就是this指针。

> 哪一个对象调用的方法，self就是哪一个对象的引用



### 14.5 访问权限

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

  > 伪私有属性和私有方法
  >
  > ```python
  > class Demo:
  >  def __init__(self):
  >      self.name = '小政'
  >      self.__age = 22  # 私有属性
  > 
  >  def __str__(self):
  >      return f'{self.name}今年{self.__age}岁'  # 内部可以访问
  > 
  >  def __provid(self):   # 私有方法
  >      print('我是私有的，你访问不到我')
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



### 14.6 魔术指令

#### 14.6.1 \_\_str\_\_

在开发中，希望使用print输出对象变量时，能打印自定义内容

```python
class Dog:

    def __str__(self):
        return "小狗汪汪叫"  # 必须要返回一个字符串

dog = Dog()
print(dog)  

# <__main__.Dog object at 0x0000015531C73820>
# 小狗汪汪叫
```

> 必须要返回一个字符串





### 14.5 运算符重载

```python
__add__	加法
__sub__	减法

```



### 14.6 封装

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



### 14.7 继承

**继承的概念**：**子类** 拥有 **父类** 的所有 **方法** 和 **属性**



#### 14.7.1 单继承

```python
class 类名(父类名):
    pass
```

> 子类 === 派生类
>
> 父类 === 基类
>
> 继承  === 派生

> 【继承的传递性】
>
> 子类可以继承父类，子类的子类也可以继承父类



#### 14.7.2 方法的重写（覆盖）

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



#### 14.7.5 多继承

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
>      print('Father_one------d1')
>  def d2(self):
>      print('Father_one------d2')
> 
> class Father_two:
>  def d1(self):
>      print('Father_two------d1')
>  def d2(self):
>      print('Father_two------d2')
> 
> class Son(Father_one, Father_two):  # one在前，用他
>  pass
> 
> son = Son()
> son.d1()
> son.d2()
> print(Son.__mro__)   # mro
> -----------------
> Father_one------d1
> Father_one------d2
> (<class '__main__.Son'>, <class '__main__.Father_one'>, <class '__main__.Father_two'>, <class 'object'>)
> ```

> 【python中的 MOR——方法搜索顺序】
>
> ```python
> print(对象.__mro__)
> ```
>
> * 从左往右的顺序查找
> * 如果在当前类中，找到方法，就立即执行，不再搜索
> * 没有找到就查找下一个类
> * 都找完了，还没有找到，程序报错



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



### 14.8 多态

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
>  @staticmethod        # 修饰器
>  def happy():        # 不需要参数
>      print('今天你微笑了吗？')
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





# pygame



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
pygame.display.update()   # 刷新屏幕内容显示
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







