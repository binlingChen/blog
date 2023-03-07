# python 基础

## 一、基础概论

### 1、数据对象及其组织

什么是数据：数据(data)是信息的表现形式和载体

#### 数据类型归纳：

* 简单类型用来**表示值**：整数int、浮点数float、复数complex、逻辑 值bool、字符串str
* 容器类型用来**组织**这些值：列表list、元组tuple、集合set、字典dic
* 数据类型之间几乎都可以转换

#### 对数据进行组织

* 对大量的数据进行处理的时候，需要建 立各种各样的数据组织，以便提高计算 效率
* 组织方式：
  * 没有组织
  * 标签式组织数据
  * 队列、栈、树、图等

### 2、计算和控制流程

#### 计算与流程

**计算**： 对现实世界处理和过程的抽象

* 普通运算：

  ```python
  12 * 34.5 + 2
  416.0 
  ```

  

* 字符串的运算：

  ```python
   ('acd'+'231') * 3
  'acd231acd231acd231'
  ```

  

* 调用黑盒子（封装好的函数）：

  ```python
  import math
  math.sqrt(25)
  5.0
  ```

  

#### 运算语句

* 将表达式复制给变量进行引用

* 赋值语句用来实现处理与暂存（可以将黑盒子里面的函数进行赋值）：

  ```python
  sqr=math.sqrt
  sqr(25)
  5.0
  ```

  

#### 控制流语句

控制流语句用来组织语句描述过程

* ![image-20230119220220202](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230119220220202.png)
* ![image-20230119220243010](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230119220243010.png)
* ![image-20230119220253535](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230119220253535.png)

#### 定义语句：def 、class

* 定义语句也用来组织语句，把一系列 运算语句集合起来给一个名字

* 描述了一个包含一系列处理过程的计 算单元，主要为了源代码的各种复用

  ```python
  def sum_list(alist):
      sum_temp=0
      for i in alist:
          sum_temp += i
      return sum_temp
  my_list=[1,2,3,4,5,6,7,8,9 ]
  my_sum=sum_list(my_list)
  print(my_sum)
  45
  ```

  

*  可以定义函数、类等“代码”对象
* 调用函数或者类，也可以得到数据对 象，Python里所有可调用的事物称 为callable

## 二、数据类型：基本类型![image-20230302231311562](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230302231311562.png)

### ![image-20230302233943235](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230302233943235.png)1、数值

#### （1）、整数类型：int

* **最大的特点是不限制大小**：无论多复杂的算式都可以直接得到结果
* **常见运算**：

![image-20230126213406364](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126213406364.png)



* 大小比较：

![image-20230126213547887](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126213547887.png)

* 连续比较判断

  ![image-20230126213557987](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126213557987.png)

* 数的进制：通常采用十进制

  ![image-20230126213745289](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126213745289.png)

  * **整数的各种进制表示**：Python语言中可以直接用二进制、八进制和 十六进制来表示整数，只要加一个前缀用以 标识几进制即可

![image-20230126213840199](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126213840199.png)

#### （2）、浮点数类型：float

* **操作和整数类似**
* **浮点数受到17为有效数字的限制**
* **特点**：
  * 科学计数法
  * 有效位数
* **特性**：进制转化造成精度误差

![image-20230126214159742](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126214159742.png)

#### （3）、复数类型

* 复数生成：Python内置复数数据类型
* 复数运算:支持所有常见计算

![image-20230126214335703](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126214335703.png)

* **复数比较**：复数之间只能比较是否相等
* **复数应用**
  * 求平面上两个点(x1,y1)和(x2,y2)的距离
  * ![image-20230126214515358](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126214515358.png)

#### （4）、更多的数学函数：math模块

<img src="C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126214924785.png" alt="image-20230126214924785"  />

* **数学常数**
  * 圆周率π、自然对数的底e等
* **数学函数**
  * 三角函数、对数、最大公约数、最小公倍数等
* 专门面向复数计算
  * math模块中的数学函数只能用于计算整数 和浮点数，对于复数就无能为力了
*  平面直角坐标和极坐标之间的转换
  * ![image-20230126215112149](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230126215112149.png)

****

### 2、逻辑值

#### （1）、判断与真值

*  **逻辑(bool)类型**
  * 逻辑值仅包括真(True)/假(False)两个
  * 用来配合if/while等语句做条件判断

![image-20230127100315907](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127100315907.png)

* 

#### （2）、逻辑运算

* “与” and
  * “并且”
  * and连接的两个真值需要同时为真，计算结果才为真

![image-20230127100452286](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127100452286.png)

* “或” or 
  * “或者”
  * or连接的两个真值只要有一个为真，计算 结果就为真

![image-20230127100706818](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127100706818.png)

* “非” not
  * “否定”
  * not连接的一个真值，非真为假，非假为真

![image-20230127100820568](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127100820568.png)

* **and和or是双目运算，由两个逻辑类型真值进行运算**
* **not是单目运算，作用于一个逻辑类型真值**
* **优先级**：not最高，and次之，or最低

#### （3）、各种类型对应的真值

* **整数、浮点数和复数类型**
  * 0是“假”，所有非0的数值都是“真”
* **字符串类型**
  * 空串("")是“假”，所有非空串都是“真”
* **所有序列类型（包括字符串）**
  * 空序列是“假”，所有非空的序列都是“真”
* **空值None**
  * 表示“无意义”或“不知道”，也是“假“

****

### 3、字符串

#### （1）、文本的表示

* 字符串就是把一个个文字的字符“串起来”的数据
  * 文字字符包含有拉丁字母、数字、标点符号、 特殊符号，以及各种语言文字字符
  * ![image-20230127101616628](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127101616628.png)
* 表示字符串数值
  * 用双引号或者单引号都可以表示字符串， 但必须成对
  * 多行字符串用三个连续单引号表示
  * ![image-20230127101711634](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127101711634.png)
* 特殊字符用转义符号“\”表示![image-20230127101807512](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127101807512.png)
* 字符的编号
  * 第一个字符的编号是0，第二个字符编号是1，...
  * 最后一个字符的编号是-1，倒数第二个字符编号是2，...
* 用这种整数编号可以从字符串中抽取出任 何一个字符

#### （2）、字符串和名字的区别

* 字符串是数据本身
* 名字是数据的标签
* 名字和字符串是“名”和“值”之间的关系
  * 一个字符串数值可以关联多个名字
  * 一个名字在同一时刻只能关联一个字符串数值
  * 字符串数值只能是字符串类型
  * 名字则可以关联任意类型的数值。
  * ![image-20230127102117106](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127102117106.png)

#### （3）、常见的字符串操作

* 获取字符串的长度:**len函数**

  ![image-20230127102241666](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127102241666.png)

* 切片(slice)操作：**s[start:end :step]**:start 和end是位置，step为步长

  ![image-20230127103513082](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127103513082.png)

  * **不包括end**序号的字符，若想取到end需往后多取一位

    ![image-20230127103711042](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127103711042.png)

* “加法”和“乘法”

  * **+**：将两个字符串进行连接，得到新的字符串。
  * *****：将字符串重复若干次，生成新的字符串

* 判断字符串内容是否相同**(==)**

  ![image-20230127103906765](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127103906765.png)

* 判断字符串中是否包含某个字符串**(in)**

  ![image-20230127104043700](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127104043700.png)

* **删除空格**

  * **str.strip**:去掉字符串前后的所有空格，内部的空 格不受影响

    ![image-20230127161800874](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127161800874.png)

  * **str.lstrip：**去掉字符串前部（左部）的所有空格

    ![image-20230127161917243](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127161917243.png)

  * **str.rstrip：**去掉字符串后部（右部）的所有空格

    ![image-20230127162031225](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127162031225.png)

* **判断字母数字**

  * **str.isalpha：**判断字符串是否全部由字母构成
  * **str.isdigit：**判断字符串是否全部由数字构成
  * **str.isalnum：**判断字符串是否仅包含字母和数字， 而不含特殊字符

#### （4）、字符串的高级操作

* **split：分割；join：合并**
* **upper/lower/swapcase：大小写相关**
* **ljust/center/rjust：排版左中右对齐**
* **replace：替换子串**

![image-20230127162346818](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127162346818.png)

#### （5）、字符串是一种序列

* **序列（sequence）**：能够按照整数顺序排列的数据
* **序列的内部结构：**
  * 可以通过从0开始的连续整数来索引单个对象；
  * 可以执行切片，获取序列的一部分；
  * 可以通过len函数来获取序列中包含多少元素；
  * 可以用加法“+”来连接为更长的序列；
  * 可以用乘法“*”来重复多次，成为更长的序列；
  * 可以用“in”来判断某个元素是否在序列中存在。

****

### 4、变量和引用

#### （1）、给数据命名

* **命名语法**：<名字> = <数据>
* **命名规则**
  * 字母和数字组合而成，下划线“_”算字母，字母 区分大小写
  * 不带特殊字符（如空格、标点、运算符等）
  * 名字的第一个字符必须是字母，而不能是数字 （注：在Python语言的名字规则中，汉字算是字母）

#### （2）、名字与变量

* **名字（name)**
  * 名字像一个标签，通过赋值来“贴”在某个数据数值 上
  * 名字和数值的关联，称为引用。
  * 关联数值后的名字，就拥有了数据的值（value） 和类型（type)
  * 一个数值可以和多个名字关联
* **变量（variable)**
  * 与数值关联的名字也称作变量，表示名字 的值和类型可以随时变化。
  * 变量可以随时指向任何一个数据对象，比如True， 1.02，或者"Hello“
  * 变量的类型随着指向的数据对象类型改变而改变
* **赋值(assignment)**
  * 名字与数值关联的过程，称为给变量赋值
  * “==”（相等关系）是对数值的相等性进行判断
  * “=”（赋值号）则是计算等号右边式子的值，赋值 给等号左边的变量

* **赋值语句**
  * 通过赋值号将变量和表达式左右相连的语句
  * 赋值语句the_sum = 0，实际上是创建了名为 the_sum的变量，然后指向数据对象“0"

#### （3）、灵活多变的赋值语句

* **最基本的赋值语句形式**:<名字> = <数据>

*  **合并赋值**:a = b = c = 1 

*  **按顺序依次赋值**:a, b, c = 7, 8, 9

* **简写赋值语句**

  ```python
  price += 1   # price=price+1
  price *= 1.5 # prince=price*1.5
  price /= 3 + 4 # price=price/(3+4)
  ```

  ****

## 三、数据类型：容器类型

#### （1）列表和元组

* **数据收纳盒**

  * 用来收纳数据对象的数据类型
  * 以一种规则的下标索引方式（收纳盒名字+ 数字序号）访问到每个数据
  * 这种收纳盒是一种序列
  * 列表可以**删除、添加、替换、重排**序列中的 元素**（可变类型）**
  * 元组是不能再更新**（不可变）**序列：元组在保留列表大多数功能的同时，去掉了一些灵活性以换取更高的处理性能

* **列表和元组的创建**

  * **创建列表：**方括号法**[]**，指明类型法**list()**
  * **创建元组：**圆括号法**()**，指明类型法**tuple(**)
  * 列表或元组中保存的各个数据称作**元素(element)**，类型没有限制

* **列表的操作：增长/缩减**

  * **增长列表**：append操作/insert操作/extend操作
  * **缩减列表：**pop操作/remove操作/clear操作
  * 列表是一种**可变容器**，可以**随意增减**
  * 但并不是所有的数据容器都能像列表 这样可以继续添加新元素

* **列表的操作：重新组织**

  * **reverse/sort操作**
    * **reverse：**把列表中的数据元素**头尾反转**重新排列
    * **sort：**把列表中的数据元素**按照大小顺序**重新排列
  * **reversed/sorted操作**：到重新排列的列表，而不影原来的列表

* **列表的方法**

  ![image-20230127171307271](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230127171307271.png)

* **列表和元组的操作**

  * **合并**
    * **加法运算+：**连接两个列表／元组
    * **乘法运算*：**复制n次，生成新列表／元组
  * **列表/元组大小**：**len()：**列表／元组中元素的个数

* **列表和元组的操作：索引和切片**

  * **索引：alist[n]或atuple（n）**
    * 可以用赋值语句给列表中的任何一个位置重新赋值
    * 但元组属于不可变类型，索引只能获取对应位置中的 数据值，不可重新赋值
  * **切片**
    * alist[start : end : step]
    * atuple（start : end : step）

* **列表和元组的操作：查找和计算**

  * **查找**
    * **in操作：**判断某个元素是否存在于列表/元组中
    * **index操作：**指定的数据在列表/元组的哪个位置
    * **count操作：**指定的数据在列表/元组中出现过几次
  * **计算**
    * **sum函数：**将列表中所有的数据元素累加
    * **min/max函数：**返回列表中最小/最大的数据元素

#### （2）字典



#### （3）集合

