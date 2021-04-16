## 第一天

#### 命名规则

#### 变量定义

~~~python
a,b,c= 1,2,3

a,b=b,a
~~~

#### 数据类型

- 判断type（）或者isinstance（）

- 可变数据类型 

  list，dict，set

- 不可变数据类型

  int，float，str，tuple，bool

> 注：1、空{}是字典类型
>
> 2、一个元素的元组要加逗号，即（1，）
>
> 3、集合不可重复，空集合使用set（）创建，集合无序

##### 列表list

~~~python
#可存储任意数据类型，有序，可变
l=list(1,2,3,4)
l2=[1,2.3,4]
~~~



#####  字典dict

~~~python
#可以存储键值对，key必须是可hash对象，不能是可变对象，key值唯一
d=dict()
d1={}
d2={"key1":"value1"}
~~~



##### 集合set

~~~python
#元素不可重复，无序
s=set()
s={1,2,4,5}
~~~



##### 元组tuple

~~~python
#不可变，有序，可重复
t=tuple()
t=(1,)
~~~



#### 输入输出

~~~python
#输入，接受的都是字符串类型
input("请输入：")
#输出
print("hello world", sep=",", end="%%")

~~~



#### 数据转换

~~~python
age=input("请输入：")
if(age.isdigit()):
    age=int(age)
    print(age, sep=",", end="years")

~~~

| 函数格式            | 使用示例                                       | 描述                                                         |
| ------------------- | ---------------------------------------------- | ------------------------------------------------------------ |
| int(x [,base])      | int("8")                                       | 可以转换的包括String类型和其他数字类型，但是会丢失精度       |
| float(x)            | float(1)或者float("1")                         | 可以转换String和其他数字类型，不足的位数用0补齐，例如1会变成1.0 |
| complex(real ,imag) | complex("1")或者complex(1,2)                   | 第一个参数可以是String或者数字，第二个参数只能为数字类型，第二个参数没有时默认为0 |
| str(x)              | str(1)                                         | 将数字转化为String                                           |
| repr(x)             | repr(Object)                                   | 返回一个对象的String格式                                     |
| eval(str)           | eval("12+23")                                  | 执行一个字符串表达式，返回计算的结果,如例子中返回35          |
| tuple(seq)          | tuple((1,2,3,4))                               | 参数可以是元组、列表或者字典，wie字典时，返回字典的key组成的集合 |
| list(s)             | list((1,2,3,4))                                | 将序列转变成一个列表，参数可为元组、字典、列表，为字典时，返回字典的key组成的集合 |
| set(s)              | set(['b', 'r', 'u', 'o', 'n'])或者set("asdfg") | 将一个可以迭代对象转变为可变集合，并且去重复，返回结果可以用来计算差集x - y、并集x \| y、交集x & y |
| frozenset(s)        | frozenset([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])      | 将一个可迭代对象转变成不可变集合，参数为元组、字典、列表等， |
| chr(x)              | chr(0x30)                                      | chr()用一个范围在 range（256）内的（就是0～255）整数作参数，返回一个对应的字符。返回值是当前整数对应的ascii字符。 |
| ord(x)              | ord('a')                                       | 返回对应的 ASCII 数值，或者 Unicode 数值                     |
| hex(x)              | hex(12)                                        | 把一个整数转换为十六进制字符串                               |
| oct(x)              | oct(12)                                        | 把一个整数转换为八进制字符串                                 |

#### 分支结构

~~~python
if 条件表达式:
    代码快
elif 条件表达式:
    代码块
else:
    代码块
~~~



#### 随机数与range函数

~~~python
import random

# in range [a, b]
a = random.randint(0, 99)

# [0, 1)
b = random.random()

#包头不包尾
c = random.choice(range(0, 99, 2))

#range  ： start默认为0 ，step默认为1
list = [x for x in range(0, 99)]
print(list)
~~~

