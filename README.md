# 前言
在「百度飞桨领航团零基础Python速成营」（链接如下：https://aistudio.baidu.com/aistudio/course/introduce/7073）的学习过程中，我学到很多关于python的知识，下面是关于所学内容的总结。
# 一、python基础
## 1.数据类型
可变对象：list dict set
不可变对象：tuple string int float bool
（1）整数(int)：整数 Python可以处理任意大小的整数，当然包括负整数，在程序中的表示方法和数学上的写法一模一样。
（2）浮点数(float)：浮点数也就是小数，之所以称为浮点数，是因为按照科学记数法表示时，一个浮点数的小数点位置是可变的。
（3）字符串(string)：字符串是以单引号'或双引号"括起来的任意文本。
（4）布尔值(bool)：布尔值和布尔代数的表示完全一致，一个布尔值只有True、False两种值布尔值 布尔值可以用and、or和not运算。
（5）空值：空值是Python里一个特殊的值，用None表示。None不能理解为0，因为0是有意义的，而None是一个特殊的空值。
（6）列表(list)：list是一种有序的集合，可以随时添加和删除其中的元素。表示方法为：集合名=[集合中的元素]。
（7）元组(tuple)：tuple和list非常类似，但是tuple一旦初始化就不能修改。表示方法为：集合名=(集合中的元素)。
（8）字典(dict)：dict的支持，dict全称dictionary，在其他语言中也称为map，使用键-值（key-value）存储，具有极快的查找速度。表示方法为：集合名={key:value}。
（9）集合(set)：set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。表示方法为：集合名={集合中的元素)。
## 2.运算符
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209082204888.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
## 3.给变量赋值
（1）直接给变量赋值如（number = 1，number = 5.5，name = 'Molly'，beautiful = True）。
（2）通过如（number += 2，number -= 5，number *= 4，number /= 6，number %= 2，number **= 5，number //= 5）的形式赋值。
（3）起名法则：
简单地理解，标识符就是一个名字，就好像我们每个人都有属于自己的名字，它的主要作用就是作为变量、函数、类、模块以及其他对象的名称
Python 中标识符的命名不是随意的，而是要遵守一定的命令规则，比如说：
标识符是由字符（A~Z 和 a~z）、下划线和数字组成，但第一个字符不能是数字。 标识符不能和 Python 中的保留字相同。 Python中的标识符中，不能包含空格、@、% 以及 $ 等特殊字符。 在 Python 中，标识符中的字母是严格区分大小写的
关键字如图：
![关键字如图](https://img-blog.csdnimg.cn/20210209082833324.png)
## 4.数据类型的转换
结构为：数据类型（数据）
示例如下：int(2.5)，str(4)，bool(3) ，float('0.6')
## 5.流程控制
### （1）条件判断：
（1）流程图如下：![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209084811373.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
（2）代码示例：
<font color=#999AAA >
```c
if light == '红灯':
    print('停')
elif light == '绿灯':
    print('行')
else:
    print('等一等')
   ```
   （3）判断语句可加入逻辑连接词（and,or,not）辅助判断，代码示例：
```c
if score_math>80 and score_english>80 and score_biology>80:
    print('奖励一朵小红花！')
else:
    print('仍需努力')
   ```
### （2）循环语句（while ... do ..a）
   （1）流程图如下：
   ![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209090157974.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
（2）代码示例：
```c
number = 1
while number<10:   
    print(number)
    number+=1
```
### （3）for 循环
（1）流程图如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209091016147.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
（2）代码示例：
```c
for i in range(9):
    print(i+1)
```
```c
fruits = ['banana', 'apple',  'mango']
for fruit in fruits:       
   print( '当前水果 :', fruit)
```
```c
for letter in 'Python':     
   print( '当前字母 :', letter)
```
4、break continue pass
（1）使⽤ break 语句来完全终⽌循环。
（2）使⽤ continue 语句直接跳到循环的下⼀次迭代。
（3）使用 pass 做占位语句，不起任何作用。
## 6.字符串的相关操作
### （1）字符串索引、切片
切片的语法：[起始:结束:步长] 字符串[start: end: step] 这三个参数都有默认值，默认截取方向是从左往右的 start:默认值为0； end : 默认值未字符串结尾元素； step : 默认值为1；
如果切片步长是负值，截取方向则是从右往左的。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209091933805.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
### （2）count 计数
1、显示自定字符在字符串当中的个数。
```c
my_string = 'hello_world'
my_string.count('o')

2
```
2、该运算所记字符串不可重叠。
```c
my_string = 'aabcabca'
my_string.count('abca')

1
```
### （3）find、index查找功能
1、find查找：返回从左第一个指定字符的索引，找不到返回-1。
index：查找返回从左第一个指定字符的索引，找不到报错。
2、代码及结果示例如下：
```c
my_string = 'hello_world'
my_string.find('o')

4
```
```c
my_string = 'hello_world'
my_string.index('o')

4
```
### （4）split 字符串的拆分
1、按照指定的内容进行分割。
2、代码及结果示例如下：
```c
my_string = 'hello_world'
my_string.split('_')

['hello', 'world']
```
### （5）字符串的替换
1、从左到右替换指定的元素，可以指定替换的个数，默认全部替换。
```c
my_string = 'hello_world'
my_string.replace('_',' ')
['hello', 'world']

'hello world'
```
2、括号内的第三项为替换个数
```c
my_string = "I wish to wish the wish you wish to wish"
my_string.replace('wish','wish'.upper(), 3)

'I WISH to WISH the WISH you wish to wish'
```
### （6）字符串标准化
1、默认去除两边的空格、换行符之类的，去除内容可以指定。
2、代码及结果示例如下：
```c
my_string = ' hello world\n'
my_string.strip()

'hello world'
```
### （7）字符串的变形
1、upper全部大写
```c
my_string = 'hello_world'
my_string.upper()

'HELLO_WORLD'
```
2、lower全部小写
```c
my_string = 'HELLO_WORLD'
my_string.lower()

'hello_world'
```
3、capitalize首字母大写
```c
my_string = 'hello_world'
my_string.capitalize()

'Hello_world'
```
### （8）字符串的格式化输出
1、格式及描述![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209095645165.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
2、用法及代码运行示例：
```c
name = 'Molly'
hight = 170.4
score_math = 95
score_english = 89
print('大家好！我叫%s，我的身高是%d cm, 数学成绩%.2f分,英语成绩%d分' % (name, hight, score_math, score_english))

大家好！我叫Molly，我的身高是170 cm, 数学成绩95.00分,英语成绩89分
```
3、format用法及代码运行示例：
```c
'Hello,{0}成绩提升了{1:.1f}分，百分比为 {2:.1f}%'.format('小明', 6, 17.523)

'Hello,小明成绩提升了6.0分，百分比为 17.5%'
```
4、f-string用法及代码运行示例：
```c
name = 'Molly'
hight = 170.4
score_math = 95
score_english = 89
print(f"大家好！我叫{name}，我的身高是{hight:.3f} cm, 数学成绩{score_math}分,英语成绩{score_english}分")

大家好！我叫Molly，我的身高是170.400 cm, 数学成绩95分,英语成绩89分
```
## 7.list的相关操作
### （1）添加新的元素
```c
list1 = ['a','b','c','d','e','f']
list1.append('g') # 在末尾添加元素
print(list1)
list1.insert(2, 'ooo')  # 在指定位置添加元素，如果指定的下标不存在，那么就是在末尾添加
print(list1)

['a', 'b', 'c', 'd', 'e', 'f', 'g']
['a', 'b', 'ooo', 'c', 'd', 'e', 'f', 'g']
```
```c
list2 = ['z','y','x']
list1.extend(list2) #合并两个list   list2中仍有元素
print(list1)
print(list2)

['a', 'b', 'ooo', 'c', 'd', 'e', 'f', 'g', 'z', 'y', 'x']
['z', 'y', 'x']
```
### （2）count 计数 和 index查找
```c
list1 = ['a','b','a','d','a','f']
print(list1.count('a')) 

3
```
```c
list1 = ['a','b','a','d','a','f']
print(list1.index('a')) 

0
```
###   （3）删除元素
```c
list1 = ['a','b','a','d','a','f']
print(list1.pop(3)) 
print(list1)
list1.remove('a')
print(list1)

d
['a', 'b', 'a', 'a', 'f']
['b', 'a', 'a', 'f']
```
### （4）生成列表
1、形式[对元素的操作 for 元素 in 元素集合 (可加if语句判断)]
2、代码示例
```c
list_2 = ['a','b','c_sv','d','e_sv']
[s for s in list_2 if s.endswith('sv')]

['c_sv', 'e_sv']
```
### （5）生成器
1、通过列表生成式，我们可以直接创建一个列表。但是，受到内存限制，列表容量肯定是有限的。而且，创建一个包含100万个元素的列表，不仅占用很大的存储空间，如果我们仅仅需要访问前面几个元素，那后面绝大多数元素占用的空间都白白浪费了。
2、第一种方法：类似列表生成式
```c
g = (x * x for x in range(10))
next(g)
```
3、第二种方法：基于函数
```c
def factor(max_num):
    # 这是一个函数  用于输出所有小于max_num的质数
    factor_list = []
    n = 2
    while n<max_num:
        find = False
        for f in factor_list:
            # 先看看列表里面有没有能整除它的
            if n % f == 0:
                find = True
                break
        if not find:
            factor_list.append(n)
            yield n            
        n+=1
g = factor(10)
next(g)
```
## 8.函数
函数是组织好的，可重复使用的，用来实现单一，或相关联功能的代码段。
函数能提高应用的模块性，和代码的重复利用率。你已经知道Python提供了许多内建函数，比如print()。但你也可以自己创建函数，这被叫做用户自定义函数。
函数代码块以 def 关键词开头，后接函数标识符名称和圆括号()。
任何传入参数和自变量必须放在圆括号中间。圆括号之间可以用于定义参数。
函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。
函数内容以冒号起始，并且缩进。
return [表达式] 结束函数，选择性地返回一个值给调用方。不带表达式的return相当于返回 None。
### 定义一个函数;函数调用
示例
```c
def student_name(name):
    "打印学生的名字"
    print('姓名：', name)
    return {'姓名':name}
rst = student_name('Alice')
rst 

姓名： Alice
{'姓名': 'Alice'}
```
## 9.参数传递
### 1、位置参数
位置参数是最简单的一种函数调用的方式。位置参数须以正确的顺序传入函数、数量必须和声明时的一样。
```c
def student_name_and_age(name, age):
    print('姓名：%s 年龄 %s' %(name, age))
student_name_and_age('张三', 18)

姓名：张三 年龄 18
```
### 2、缺省参数
调用函数时，缺省参数的值如果没有传入，则被认为是默认值。
```c
def student_name_and_age(name, age='不愿透露'):
    print('姓名：%s 年龄 %s' %(name, age))
student_name_and_age('张三')

姓名：张三 年龄 不愿透露
```
也可以为默认参数赋值
```c
student_name_and_age('张三', 18)

姓名：张三 年龄 18
```
### 3、可变参数
顾名思义，可变参数就是传入的参数个数是可变的，可以是1个、2个到任意个，还可以是0个。
```c
def all_student_names(*names):
    for name in names:
        print('姓名：', name)
all_student_names('张三','李四','王五')

姓名： 张三
姓名： 李四
姓名： 王五
```
### 4、关键字参数
关键字参数允许你传入0个或任意个含参数名的参数，这些关键字参数在函数内部自动组装为一个dict。
```c
def student_info(name, age, **kw):
    print(f'我的名字叫：{name},年龄：{age},其它信息：{kw}')
student_info('张三', 18, height=180)

我的名字叫：张三,年龄：18,其它信息：{'height': 180}
```
### 5、命名关键字参数
如果要限制关键字参数的名字，就可以用命名关键字参数
```c
def print_person_info(name, age, *, height, weight):
    print('我的名字叫：', name, '年龄：', age,'身高', height, '体重', weight)
print_person_info('张三', 18, height=180, weight=75)

我的名字叫： 张三 年龄： 18 身高 180 体重 75
```
## 10.变量的作用域和global变量
1.局部变量 作用域:在函数内
2.全局变量 作用域:在函数外
3.函数优先使用局部变量 在没有局部变量的情况下， 使用全局变量
4.定义在函数内部的变量，函数结束之后自动消亡
```c
name = '张三'#全局变量
def print_my_name():
    name='李四'#局部变量
```
5.说明不管外部变量的类型是什么，如果在函数内部想对它做赋值操作就必须使用global声明。
## 11.函数举例
### 1.lambda匿名函数
python 使用 lambda 来创建匿名函数。
lambda 只是一个表达式，函数体比 def 简单很多。
lambda 的主体是一个表达式，而不是一个代码块。仅仅能在 lambda 表达式中封装有限的逻辑进去。
lambda 函数拥有自己的命名空间，且不能访问自有参数列表之外或全局命名空间里的参数。
虽然 lambda 函数看起来只能写一行，却不等同于 C 或 C++ 的内联函数，后者的目的是调用小函数时不占用栈内存从而增加运行效率。
```c
(lambda arg1, arg2: arg1 + arg2 )(1, 2)

3
```
```c
add = lambda arg1, arg2: arg1 + arg2
add(1,2)

3
```
### 2.高阶函数
函数中可以传入另一个函数作为参数的函数。
```c
def func_x(x, f):
    return f(x)
func_x(-1, abs)

1    
```
### 3.map函数
map()函数接收两个参数，一个是函数，一个是Iterable，map将传入的函数依次作用到序列的每个元素，并把结果作为新的Iterator返回。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209114655853.png)
```c
fx = lambda x:x**2
ls = [1,2,3,4,5,6,7,8,9]
rst = map(fx, ls)
list(rst)

[1, 4, 9, 16, 25, 36, 49, 64, 81]
```
### 4.reduce函数
用传给 reduce 中的函数 function（有两个参数）先对集合中的第 1、2 个元素进行操作，得到的结果再与第三个数据用 function 函数运算，依此类推，最后得到一个结果。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210209115036129.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L20wXzUzODc0NzQ2,size_16,color_FFFFFF,t_70)
```c
from functools import reduce
mul_xy = lambda x, y: x*y
reduce(mul_xy, [1, 3, 5, 7, 9])

945
```
### 5.sorted函数
排序也是在程序中经常用到的算法。无论使用冒泡排序还是快速排序，排序的核心是比较两个元素的大小。如果是数字，我们可以直接比较，但如果是字符串或者两个dict呢？直接比较数学上的大小是没有意义的，因此，比较的过程必须通过函数抽象出来。
```c
sorted([36, 5, -12, 9, -21])

[-21, -12, 5, 9, 36]
```
若结尾以reverse=True 结尾则从大到小
```c
sorted([36, 5, -12, 9, -21], reverse=True)

[36, 9, 5, -12, -21]
```
若结尾以key=函数名 结尾则进行该函数处理后排序
```c
sorted([36, 5, -12, 9, -21], key=abs)

[5, 9, -12, -21, 36]
```
### 6.偏函数
通过设定参数的默认值，降低函数调用的难度
```c
def student_info(name, age, city='北京'):
    print(f'我的名字叫{name}, 今年{age}岁，来自{city}')
student_info('Molly',18)

我的名字叫Molly, 今年18岁，来自北京
```
可通过partial修改默认值
```c
from functools import partial
def student_info(name, age, city):
    print(f'我的名字叫{name}, 今年{age}岁，来自{city}')
student_info_beijing = partial(student_info, city='北京')
student_info_beijing('Molly',18)

我的名字叫Molly, 今年18岁，来自北京
```
## 12.模块
通过import
```c
import time 
```
通过import as 可以简化命名
```c
import numpy as np
```
# 二、Python面向对象
## 1.使用类的好处
1、降低复杂性-》更少的bug-》提高可维护性
2、类可以将数据与函数绑定在一起，使代码模块化
3、调用数据和函数，使用对象名.的方式，使代码更加优雅
## 2.面向对象的世界
代码通常称为类的方法，数据通常称为类的属性，实例化的对象称为实例
## 3.如何定义类
class Athlete:
第一部分：class定义类的关键字，Athlete符合python标识符命名规则，：表示类内容的开始
def init(self,a_name,a_dob=None,a_times=[]):
第二部分：def定义函数的关键字，init 方法是一个特殊方法会在实例化对象时自动调用，我们会在这个方法中对数据进行赋值。self作为类中函数的第一个参数，方便该方法调用该类的其他属性和方法。
第三部分：自定义的属性和方法
```c
class Athlete:
    def __init__(self,a_name,a_dob=None,a_times=[]):
        self.name = a_name
        self.dob = a_dob
        self.times = a_times

    def top3(self):
        return sorted(set([self.sanitize(t) for t in self.times]))[0:3]
        
    def sanitize(self,time_string):
        if '-' in time_string:
            splitter = '-'
        elif ':' in time_string:
            splitter = ':'
        else:
            return (time_string)
        (mins,secs) = time_string.split(splitter)
        return (mins+'.'+secs)
```
## 4.如何使用类
1.创建对象
对象名 = 类名(参数)
2.使用.调用类的方法和属性
对象.属性名
对象.方法名()
```c
james = Athlete(james_name,james_dob,james_times)
print('姓名：%s,生日：%s,最快的3次成绩：%s' %(james.name,james.dob,james.top3()))
```
## 5.类属性
1、所有对象共享的数据
2、使用
定义：在 init 之上，或者说在类的范围内与方法同等级别，书写变量名=值
调用：类名.类属性
```c
class Athlete:
    address = '中国足球协会训练基地xx街xx号'
    def __init__(self,a_name,a_dob=None,a_times=[]):
        self.name = a_name
        self.dob = a_dob
        self.times = a_times
```
## 6.类方法
1、所有对象共享的方法
2、使用
定义：方法定义时，使用@classmethod标记
调用：类名.类方法，对象.类方法
```c
    @classmethod
    def changeAddress(self):
        self.address = '中国田径训练基地xx街xx号'
Athlete.changeAddress()
```
## 7.函数的私用
私用的属性和方法的定义：在属性和方法名前加 __ 两个下划线
如何调用:只能通过类中的方法来调用私有的属性和方法
## 8.父类的调用
1、如何使用
定义：
class 子类名(父类名)：
情况1，如果子类有新增的属性，那么需要在子类__init方法中，调用父类的__init__
情况2，如果子类没有新增的属性,子类不需要写__init__方法
使用：
对象名 = 子类名(参数)
2、方法重写
子类方法与父类方法完全相同，子类若重写了父类的方法，则子类对象调用方法时就是调用的自己类中重新的方法。
3、继承的好处：代码重用，升级功能（重写），新增功能（新的方法）
```c
class Rugby(Athlete):
    def __init__(self,a_name,a_bod,a_squat,a_times):
        Athlete.__init__(self,a_name,a_bod,a_times)
        self.squat = a_squat
    def top3(self):
        return sorted([self.sanitize(t) for t in self.times])[-3:]
   ```
##  9.多态性：一个事物多种形态
 1、‘多态的好处是：减少重复代码，分离经常改变的代码与不经常改变的代码，使得代码可维护性提高。
 2、代码举例
 ```c
def print_rugby(athlete):
    print(athlete.name)
    print(athlete.dob)
    print(athlete.squat)
    print(athlete.top3())
print_rugby(loren)
print_rugby(mark)
   ```
## 10.多继承
 ```c
class Father(): 
    def talk(self):
        print("---爸爸的表达能力---")
class Mather():
    def smart(self):
        print("---妈妈聪明的头脑---")
class Child(Father,Mather):
    pass
child1 = Child()
child1.talk()
child1.smart()

---爸爸的表达能力---
---妈妈聪明的头脑---
   ```
## 11.使用模块下的所有代码
 ```c
import sys
sys.path.append('mywork')
from athlete import *
   ```
import sys
导入sys模块 sys.path.append('work')
将模块athlete.py添加到模块搜索路径
from athlete import *
导入athlete模块，使用athlete模块下的所有代码
# 三、文件操作
## 1.文件打开
with open('文件路径') as f:
 ```c
with open('work/train_data_cor.txt') as f:
   ```
##  2.文件内格式问题处理办法
try:
	...
except:
	...
 ```c
try:
	print('姓名：'+data.pop(0)+'生日：'+data.pop(0)+'时间：'+str(data))
except:
    pass
   ```
## 3.文件函数
### 1、f.read()
读取文件
### 2、f.seek()
改变文件当前位置
### 3、f.tell()
读取位置
### 4、f.write()
写入文件但事先以'w'的形式打开文件
 ```c
f = open('work/data.txt','w')
f.write('this is file content')
f.close()
   ```
