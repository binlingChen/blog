# 黑马python学习记录

占位符语法：

```
'%s'%变量
```

常用占位符：

* 字符串：%s
* 整数：%d
* 浮点数：%f

![image-20230303164538281](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230303164538281.png)

* 快速格式化：

  ```python
  f'内容{变量}'
  ```

  不关心类型，不做精度控制

* input()输入直接是字符串格式，需要进行格式转换

* ![image-20230303182040681](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230303182040681.png)

* round( x [, n]  )：
* x -- 数字表达式。
* n -- 表示从小数点位数，其中 x 需要四舍五入，默认值为 0。

* 在print语句中，加上 `end=''`就可以输出不换行
* `\t`制表符，对齐
* 每个print默认换行
* for循环可以直接对字符串进行遍历
* for循环无法定义循环条件，只能从处理的数据集中一次取出内容进行处理
* range(num):获取一个从0 开始，到num结束的数字序列（不含num本身)
* range(num1,num2):从num1开始到num2结束的序列，不含num2
* range(num1,num2，step):

* 函数内部变量在声明前面加个 `global`就可以成为全局变量

* ![image-20230304083640112](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230304083640112.png)

* 列表可以一次存储多个数据，且可以为不同的数据类型,可以嵌套

* ```python
  my_list=[12,'chen',True]
  print(type(my_list[0]))
  ```

* ![image-20230304084746519](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230304084746519.png)

* 方法extend:![image-20230304085533910](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230304085533910.png)

* ![image-20230304090314070](C:\Users\BinlingChen\AppData\Roaming\Typora\typora-user-images\image-20230304090314070.png)
