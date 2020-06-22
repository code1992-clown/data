









# python

```python
print(id(b),type(b))   id type  del 
del a
b=a=[1,3,4]  链式赋值
x,y=12,23  互换
x,y=y,x   Python不支持常量 大写

a=x//y
b=x%y
print(a*y+b)
print(a,b)
w=divmod(x,y)
int()    把小数部分去掉

a=314e-2  科学计数法
float()
round()  四舍五入
import math as m 
dis=m.sqrt((x3-x0)**2+(y3-y0)**2)
  
and or not 有短路的现象
is  not is   比较地址
整数缓存：[-5,256]   python做的优化
print(a is b)  比较地址
print(a == b)  比较值

print(ord('A'))  //65
print(chr(66))   //B
a = "I'r"  单引号和双引号一起使用的情况
a='陈振方'  长度和英文的一样
b="""
hello wodr  多行字符串
1,]
  545
"""
c=''   空字符串
print(len(a))

print("a\nb")  # 转义字符
print('hello\
  fadflasfafaf')   续命符
print(3+4)
print('i love you '  * 3,end='##')  打印3次，不换行，以##结尾，也可用转移字符
print("3"+"4")  字符串拼接
a=input('qins:')  输入阻塞
a=str(501)  #把其他类型转换成字符串
print(type(a))  
a=a.replace('5','3') # 字符串不可变，用replace可以改变，返回改变后的字符串
print(a[-1+1])  # 可以进行运算
a='hesko'
b=a[::2]  # 切片 最后一个式步长，默认为1，前面的参数可正可负，步长可以为负数

a='to be or not to be'
b=a.split()  # 里可以有参数，代表以什么进行分割，变换成列表
c="*".join(b) # 拼接，变成字符串   join的性能比拼接符高
字符串驻留机制：符合字符串规则的字符串
a="hello #"
b="hello #"
print("hx" in a)


a='hello'
print(len(a))  # 字符串的长度
print(a.startswith('h'))
print(a.endswith('h'))  # 判断是不是以什么开头或者结尾
print(a.find('l'))    # 从左往右查找子串出现的第一个索引
print(a.rfind('l'))  # 从右往左查找子串出现的第一个索引
print(a.count('l'))  # 字符出现的次数
print(a.isalnum())    # 是不是数字或者字母

a='hEllO haha'

print(a.strip("*"))   # 去除首尾空格  也可去除指定字符
print(a.capitalize())   #  首字母大写
print(a.title())   # 所有字母首字母大写
print(a.upper())   # 所有字母都变大写
print(a.lower())   # 所有字母都变小写
print(a.swapcase())  # 大变小，小变大
a='hll'
print(a.center(10,"*"))  # 居中对齐
print(a.ljust(10,"*"))    # 左对齐r
print(a.rjust(10,"*"))    # 右对齐

a='hll'
print(a.isalpha())
print(a.isdigit())
print(a.isspace())
print(a.isupper())
print(a.islower())

a="name:{name},age:{age}"
b=a.format(name='lisi',age=12) #  字符串格式化
a="name:{name:*^8},age:{age}"  # 居中  不足的用*补齐
a="name:{name:*>8},age:{age}"  # 右对齐
a="name:{name:*<8},age:{age}"  # 左对齐

import io as i
a='hello.txt'  # 可变字符串
sio=i.StringIO(a)
print(sio.getvalue())
sio.seek(0)  # 指针移动到这个地方
sio.write('m')  # 修改
print(sio.getvalue())

# 字符串，列表 元组，字典，集合  =》序列
import random
a=[1,3,4,5]  # 通过[]创建
a=list("hello"+"world") # ['h', 'e', 'l', 'l', 'o', 'w', 'o', 'r', 'l', 'd']
a=list(range(1,10,2))  #  [1, 3, 5, 7, 9]  start end setp
a= [ x*2 for x in range(5) if x>=2] # [0, 2, 4, 6, 8]=>[6, 8]  可以添加过滤条件
a.append(63)   # 速度快，推荐使用
b=[133,253,963] 
# a=a+b #  [4, 6, 8, 63, 133, 253, 963]   效率低
a.extend(b)   # 效率高，推荐使用
a.insert(0,10000)   # 尽量避免使用  数组的拷贝
a*=2
del a[0]  # 也是数组的拷贝  效率不高
a.pop(0)  #  删除最后一个元素，也可以指定位置索引
a.remove(8) # 删除第一次出现的元素，参数为value
b=a.index(133,0) # 搜索133元素，从0索引开始
b=a.count(133)  #计算元素出现的次数
b=len(a)
c=a[-5::2]  # 和字符串中的切片一样的
c.sort(reverse=True)
random.shuffle(c)  # 随机排序 
sorted(c,reverse=True)  # 返回新的列表
reversed(c)  # 返回一个逆序排列
print(c)
print(b in a) 

a=[1,34,5,66,9]
c=reversed(a) # 返回迭代器
d=list(c)
print(d)  #[9, 66, 5, 34, 1]

a=[1,34,5,66,9]
print(max(a))
print(min(a))
print(sum(a))


二维列表

# 元组不可变序列  访问速度比列表快
a = (1,2,4,5)
a=(20,)
a=tuple([1,2,4])
a=tuple(range(5))
# a[1]="lisi"  # 不能修改，其他的都是一样的
b=a[1:]
b=sorted(a)
# del a  # 元组的删除 
# len sum min max 
d=zip(list(range(5)),list(range(10)))  # zip
print(list(d))
# print(type(a))
a=(i for i in range(5))  # 元组推导式
b=[i for i in range(5)]
print(tuple(a))      # tuple 包装生成元组
print(a.__next__())
print(a.__next__())
print(a.__next__())
print(a.__next__())
print(b)


a={"name":'lisi',"age":12,"age":326}  # 通过{}创建
a=dict(name='lisi')
a=dict([("name","lisi")])
a={}
k=['name','age','job']
v=['lisi',18,'coder']
a=dict(zip(k,v))
 
# a=dict.fromkeys(['name','age'])  # {'naem': None, 'age': None}s
# print(a)  # 键不能重复
# print(a.get('names',"不存在"))  # 推荐
# print(a["name"])
# print(a.keys())
# print(a.items())
# print(a.values())
# print(len(a))
# print('name' in a )
a["address"]="haidian" # 存在就覆盖
b=dict.fromkeys(["n"])

a.update(b)    # 更新a
del a['name']
# a.pop('name')   # 有返回值
# a.clear()
a.popitem()  # 随机弹出键值对
print(a)


序列解包
x,y,z=(1,2,3)
print(x,y,z)
s={"name":2,"age":18}
a,b=s.items()
print(a,b)  # 默认是对键进行操作，可以使用values()对值进行操作，items()
print(a)


k=["姓名","年龄","薪资","城市"]
v1=["高小一","18","30000","北京"]
v2=["高小二","28","40000","上海"]
v3=["高小三","38","50000","深圳"]
r1=dict(zip(k,v1))
r2=dict(zip(k,v2))
r3=dict(zip(k,v3))
a=[r1,r2,r3]
# print(a)
# print(a[0]['姓名'])
for i in range(len(a)):
  print(a[i].get('姓名'))



# 集合是无序可变，元素不能重复，底层是字典，键对象
# x=list('abcd')
x={'a','b','c',3,7}
a={3,5,7}
# a.add(30)  #元素不能重复
# a=set(x)    # 变成集合a.remove()
# a.remove('b')
# a.clear()
print(a|x)  #并集
print(a&x)  #交集
print(x-a)  #差集
print(a.union(x))             
print(a.intersection(x))
print(a.difference(x))
# print(x)
# print(type(a))

# 选择结构
a = int(input("请输入成绩："))
# if a > 2:  # 不可以有赋值运算符
#     print("3>2")
# else:
#     print("a不大于2")

# print('a>2') if a>2 else print('a<2')  # 三元运算符
print("分数：{0}，等级：{1}".format(a,'不及格')) if a<60 else print("分数：{0}，等级：{1}".format(a,'良好')) if 80>a>=70 else \
print("分数：{0}，等级：{1}".format(a,'优秀')) if 100>a>=80 else print("分数：{0}，等级：{1}".format(a,'及格'))



# for i in range(1,10):   # 可迭代对象
#   for j in range(1,i+1):
#     print(j)
# for i in {"name":'lisi',"age":54}.items():
#   print(i)
for i in range(1,10):
  for j in range(1,i+1):
    print("{0}*{1}= {2}".format(i,j,i*j), end="\t")
  print()

break,continue
while   else{正常结束，会执行else}
for   else



# 循环代码优化
# 尽量减少循环内部不必要的计算
# 尽量减少内循环的计算
# 尽量使用局部变量

xs=('lisi','woang','haah')
ys=('lisi','woang','haah')
zs=('lisi','woang')
for x,y,z in zip(xs,ys,zs):  # 并行迭代
  print(x,y,z)



# 推导式
# import math 

# ls=[math.pow(x,2) for x in range(1,5) if x> 2] # [9.0, 16.0]
# ls=[(x,y)for x in range(3) for y in range(3)] # [(0, 0), (0, 1), (0, 2), (1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
# print(ls)

# my = 'i love you'
# a={c:my.count(c) for c in my}  # {'i': 1, ' ': 2, 'l': 1, 'o': 2, 'v': 1, 'e': 1, 'y': 1, 'u': 1}
# print(a)

# a={x for x in range(4) if x > 1} # {2, 3}
# print(a)

# 生成器推导式  只能调用一次  生成元组list
gnt=(i for i in range(4))
print(tuple(gnt)) # 第一次可以看
print(list(gnt))  # 空了



import turtle as tt
a=int(input('请输入圆的半径：'))
colors=['red','yellow','green','cyan']
num=len(colors)
t=tt.Pen()
t.pensize(8)
t.speed(2)
for i in range(1,12):
  t.color(colors[i%num])
  t.circle(i*a)
  t.penup()
  t.goto(0,-i*a+i*10)
  t.pendown()
tt.done()
```

```python
def fun(a):
    print(a)
for i in range(10):
  fun(i+100)


import math

# 形参与实参一一对应
def fun(a,b):
  """
求平方差
  """
  return math.sqrt(math.pow(a,2)+math.pow(b,2))  # 结束函数的运行  没有返回值，默认为none 返回多个值可以用字典，列表，元组等
print(fun(10,10))
help(fun.__doc__)

a=123
def su ():
  b=3455
  global a  # 改变全局中 的a
  a=100000
  print(a)
  print(locals()) # 输出局部变量
  print(globals())  # 输出全局变量
su()
print(a)  # 100000


局部变量效率高于全局变量

# 参数传递不可变对象，由于对象不可变，会新建一个新的地址，可变对象会用同一个地址

import copy
a=[10,20,[30,40]]
b=copy.copy(a)# 浅拷贝

b=copy.deepcopy(a) # 深拷贝
print(a)
print(b)
b.append(30) 
b[2].append(1233) 
print(a)
print(b)   # 传递不可变对象，不可变对象里包含子对象是可变的，发生浅拷贝

def fun (a,b,c=12):  # 默认值参数
  print(b)
fun(b=1,a=3)  # 位置参数，命名参数

def fun (a,b,*c):   # 元组
  print(c)
fun(12,3,4,5,67,7)  # (4, 5, 67, 7)

def fun1 (a,b,**c):   # 字典
  print(c)
fun1(12,3,name='lisi',age=18)  #{'name': 'lisi', 'age': 18}

def fun (*a,b,c):   
  print(a)
fun(12,3,4,5,b=67,c=7)  # (12, 3, 4, 5)  强制命名

f=lambda a,b,c : a+b+c # lambda表达式
print(f(1,2,3))  # 6

a=[lambda a : a**2,lambda b :b+100]
print(a[0](9))  # 81

eval("print(123)")
dic =dict(a=100,b=200)
eval("print(a+b)",dic)  # 300 第二个参数为引用什么位置的


# 递归，自己调用自己，有出口
def fun (n):
  if n ==0:  # 出口
    return 1
  else:    
    return n*fun(n-1)  #自己玩自己
print(fun(3))


# 内部函数，嵌套函数，隐藏细节，提高代码的复用率
def fun ():
  a=10
  def fun2 ():
    nonlocal a  # 和global差不多  改变外部变量的方法
    a=100
    print(a)

  fun2()
  print(a,'outer')
fun()
L=>E=>G=>B
L:函数或者类的内部方法
E:闭包
G:全局变量
B:python为自己保留的特殊名称
# pi="G"
def fun ():
  # pi="E"
  def fun2 ():
    # pi="L"
    print(pi)
  fun2()

fun()
```

```python

# 面向对象：数据和操作相关的方法封装到对象中，提高开发效率，面向对象比面向过程高级，面向对象底层还是面向过程
# 设计者思维，执行者思维
class Students:    # 首字母大写
  def __init__(self,name,score):  # 构造函数，self相当于self
    self.name=name
    self.score=score
  
  def say_score(self):
    print("{0}分数是：{1}".format(self.name,self.score))

s1=Students('gaoqi','12') #1.调用__new__,创建对象  2.调用__init__,初始化，给实例属性赋值 3.方法也是属性
s1.say_score()   # 与下面的方法相同，实质上就是调用下面的方法   pass空占位符
Students.say_score(s1)
print(dir(s1))
print(isinstance(s1,Students))  # 判断是不是类的实列


class Person:
  def __init__(self):
    pass
print(type(Person))  # type类型
# 实例属性  实例方法

# 类属性  类方法
class Student:
  company="gonsis"
  count=0  # 类属性
  def __init__(self,name,age):
    self.name=name
    self.age=age
    Student.count+=1
    self.count= Student.count+1
  def say(self):
    print("我的公司是:{0},我是公司的第{1}个员工".format(self.company,self.count))
    print("我的名字是：{0}，我的年龄是：{1}".format(self.name,self.age))
s1=Student('zx',18)
s2=Student('lisi',18)
s3=Student('lisi',18)

s1.say()
s2.say()
s3.say()
print("一共创建了{0}个对象".format(Student.count))



class Student:
  componey="hongao"

  @classmethod  #类方法  不能调用实例方法和属性，因为还没有创建实列
  def fun(cls):
    print(cls.componey)  # hongao

  @staticmethod  # 静态方法   不能调用实例方法和属性  因为还没有创建实列
  def add(a,b):
    print(a+b)

  # def fun2(cls):  会报错
  # print(cls.componey)  # hongao
Student.fun()
__del__,__call__

# python中没有方法重载
class Person:
  def say (self):
    print('hlelo')
  def say (self):
    print('hlsssselo')
p1=Person()
p1.say()
# 可以定义新的方法，可以重新写老的方法，方法也是对象，函数也是队形，一切都是对象

# 私有属性和私有方法实现封装
class Employee:
  __compony="baizhan"  #类属性也是可以的
  def __init__(self,name,age):
    self.__name=name # 私有属性
    self.age=age
  def __work(self):  # 私有方法
    print("好好工作。。。")
e=Employee('lisi',18)
# print(e.name)  失败
print(e._Employee__name)  # 也可以通过这种方式访问,私有不是真正的私有  内部可以随便用
# e.__work()
e._Employee__work()  # 也可以通过这种方式访问,私有不是真正的私有  内部可以随便用
print(dir(e))


class Student:
  @property  # 装饰器，将方法的调用改成属性的调用，不能设置属性
  def salary(self):
    return 100000
e=Student()
print(e.salary)


class Employee:
  def __init__(self,name,salary):
    self.__name=name
    self.__salary=salary
  def get(self):
    return self.__salary
  def set(self,sala):
    if 1000<sala<50000:
      self.__salary=sala
    else:
      print('工资输入有误')
e=Employee('lisi',52000)
e.set(2000000)
print(e.get())

# 这一版比较好
class Employee:
  def __init__(self,name,salary):
    self.__name=name
    self.__salary=salary
  @property
  def salary(self):
    return self.__salary
  @salary.setter
  def salary(self,sala):
    if 1000<sala<50000:
      self.__salary=sala
    else:
      print('工资输入有误')
e=Employee('lisi',52000)
e.salary=10000
print(e.salary)


# 封装，继承，多态

# 继承  代码复用
class Person:
  def __init__(self,name,salary):
    self.name=name
    self.__salary=salary
  def sayage(self):
    print('Person类中的age')

class Student(Person):
  def __init__(self, name, salary):
    Person.__init__(self,name, salary)  # 调用属性
s=Student("lisi",256)
print(s.name)
print(s._Person__salary)   # 也可以这种方式来访问父级的私有属性
s.sayage()
print(dir(s))

# 方法的重写，就是子类的方法覆盖父类的方法

class A:
  pass
class B(A):
  pass
class C(B):
  pass
print(C.mro())  # 查看类的继承关系图  object是所有类的父类


class Person:
  def __init__(self,name):
    self.name=name
  # def __del__(self):
  #   print('你真的要删除？')
  def __str__(self):
    return "你个大傻逼"
p=Person('lisi')
p.name
del p.name
# python 支持多重继承（有多个爸爸） 避免使用

super()获取父类的定义，不是父类的对象
class A:
  def say(self):
    print('A')
class B(A):
  def say(self):
    super().say()
    print('B')
b=B()
b.say()

# 方法的多态，同一个方法调用的对象不同可能产生不同的结果，属性没有多态
# 运算符的重载

print(object.__dict__)
print(object.__class__)
print(object.__bases__)
print(object.__subclasshook__)

# 对象的深拷贝和浅拷贝
# 浅拷贝知识复制父类，不复制子类
# 深拷贝，会递归的复制所有的父类，子类
# 继承 is a 关系
# 组合  has a  关系  完全可以取代继承，都可以实现代码的复用

# 23中设计模式
# 工程模式：
class Car:
  def creatCar(self,brand):
    if brand=="奔驰":
      # print('benchi')
      return BC()
    elif brand=="宝马":
      return BMW()
    else :
        return 'sb'

class BC:
  pass
class BMW:
  pass

c=Car()
print(c.creatCar("奔驰"))

# 单例模式

```

````python
try:
  1/0 # 出现异常，后面就不会执行
except BaseException as e:
  print(e)


# 异常处理，子类在前，父类在后
try:
  a=input('请输入一个被除数：')
  b=input('请输入一个除数：')
  c=float(a)/float(b)

except ZeroDivisionError as e:  # 先子类后父类
  print("分子不能为0")
except ValueError:
  print('请输入数字')
except BaseException as e:
  print(e)
else:
  print(c)
finally:
  print("finally")
  # return 放到结构之外的最后
# SyntaxError:语法错误
# NameError:尝试访问一个没有申明的变量  undefined
# ZeroDivisionError:零除问题  3/0
# ValueError：输出错误  float('asagd')
# TypeError:类型错误  123+“abc"
# AttributeError:访问对象的不存在属性
# IndexError: 索引越界异常
# KeyError ：字典的关键字不存在

````

```python
# with上下文管理器   会自动释放资源
with open("sin.svg") as f:
  for line in f:
    print(line)
    
import traceback
try:
  print('step1')
  num=1/0
except:
  with open('1.txt','a') as f:
    traceback.print_exc(file=f)
    
class AgeError(Exception):
  def __init__(self,errorinfo):
    Exception.__init__(self)
    self.errorinfo=errorinfo
  def __str__(self):
    return "年龄错误"
  
if __name__=="__main__":
  age=int(input('请输入年龄：'))
  if age<1 or age>150:
    raise AgeError(age)
  else:
    print(age)
```

```python
# I/O操作
f=open('1.txt',"a",encoding='utf-8') # a,w,r,+,b
s="i\tlove\t哈啊哈哈ou\n"
f.write(s)   # 
x=['lisi\t','wangwu\t']
f.writelines(x)   # 行写入
f.close()
# with open('1.txt','r') as f:
#   x=f.read()
#   print(x)

# read readline readlines


with open('1.txt','r',encoding="utf-8") as f:
  # a=f.read(1)  # 读取1个字符，汉字也是一样的
  while True:
    a=f.readline()
    if not a:
      break
    else:
      print(a)
    
with open('1.txt','r',encoding="utf-8") as f:
  for i in f:
    print(i)
    
    
  with open('1.txt','r',encoding="utf-8") as f:
  a=f.readlines()
c=[str(item) +'    #'+str(index) for index,item in enumerate(a)]
print(c)
with open('1.txt',"w",encoding="utf-8") as f:
  f.writelines(c)

# 图片的拷贝  二进制
with open('result.png','rb') as f:
  with open("1.png",'wb') as w:
    a=f.readlines()
    for i in a:
      w.write(i)
    
    
 with open('1.txt',"r",encoding="utf-8") as f:
  print("文件的名字：{0}".format(f.name))
  print("指针的位置：{0}".format(f.tell()))
  print("读取的内容：{0}".format(f.readline()))
  print("指针的位置：{0}".format(f.tell()))
  f.seek(2)
  print("读取的内容：{0}".format(f.readline()))
    
    
  # 序列化
import  pickle
a=[i for i in range(5)]
with open('1.txt','wb') as f:  
  pickle.dump(a,f) # 序列化
with open('1.txt','rb') as f:
 a= pickle.load(f) # 反序列化
 print(a)
    
    import csv
with open('1.csv','r') as f:
  a=csv.reader(f)
  print(list(a))

with open('1.csv','w') as f:
  a=csv.writer(f)
  a.writerow(['Id',"姓名"])
  a.writerows(list) # 整行列表都写进去
```

```python
# os模块  操作系统  os.path 模块
import os
# os.system("notepad.exe")
# os.system("ping www.baidu.com")
# os.system('cmd')
os.startfile(r"D:\Program Files (x86)\Tencent\WeChat\WeChat.exe")

import os
print(os.name)  # window =>nt  other=>posix
print(os.sep)# \
print(repr(os.linesep)) # \r\t
print(os.stat('1.png'))
# os.mkdir("书籍")  # 创建目录
# os.rmdir('书籍')    # 删除目录
os.makedirs('../2/3')
# os.removedirs('1/24')  #多级目录，删除的时候只能为空
# os.cddir()
os.rename()
os.listdir()

print(os.getcwd())   # 获得的工作目录


import  os
f=os.getcwd()
a=os.walk(f) # 遍历文件和目录
for dirpath,dirname,filenames  in a:
  for dir in dirname:
    print(dir)
  for file in filenames:
    print(file)
    
 import shutil as s
s.copyfile("1.txt","2.txt")
s.copytree("movie/1","dianying",ignore=s.ignore_patterns("*.txt")) # 把1拷贝到dianying下 除了txt文件


import shutil as s
import zipfile as z
zip=z.ZipFile('a.txt','w') # yasuo
zip=z.ZipFile('a.txt','r') #解压缩
zip.write('1.txt')
s.make_archive("压缩后的位置和名称","zip","要压缩谁")
zip.close()

# 递归方法
import os
def get(path,lever):
  childlist=os.listdir(path)
  for file in childlist:
    filepath=os.path.join(path,file)
    if os.path.isdir(filepath):
      get(filepath,lever+1)
    print("\t"*lever+filepath)
get('.vscode',0)
```

````python
# 程序=》包=》模块=》类=》函数+属性=》语句

import math  # 导入一个模块
# import A,B,C  # 导入多个模块
# import  math as m # 别名
from math import pi,sin  # 下面就可以直接用了  可以写 *
print(dir(math))
print(math.__name__)
a=math.sin(math.pi/6)
print(math.round(a))


s="math"  
m=__import__(s)# 动态调用  不推荐
print(m.pi)
# 一个模块无论导入多少次，在解释器里面只生成一个实例
import importlib  # 重新加载的模块
````

