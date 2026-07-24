# **<mark>python基础题</mark>**

## **<mark>第一题</mark>**

编写一个程序，找到2000年至3200年（包括在内）中所有可被7整除但不能被5整除的所有数字，得到的数字按逗号分隔，打印在一行上。

```
for i in range(2000,3201):
    if i%7==0 and i%5!=0:
        print(i,end=",")
```

## **<mark>第二题</mark>**

编写一个可以计算给定数阶乘的程序，结果以逗号分隔，打印在一行上；

```
l = map(int, input("请输入数字").split())
def function(x):
    if x < 2:
        return 1
    else:
        return x * function(x-1)
result = []
for i in l:
    result.append(str(function(i)))
print(",".join(result))  
#此程序可以一次输入多个数字并计算其阶乘
```

## **<mark>第三题</mark>**

使用给定的整数n，编写程序生成一个包含（i，ixi）的字典，该字典包含从1到n之间的整数（两者都包含），然后打印字典。假设向程序提供以下输入:8 则输出为:{1:1，2:4，3:9，4:16，5:25，6:36，,7:49，8:64}

```
l={}
n=int(input("请输入数字："))
for i in range(1,n+1):
    l.update({i:i*i})
print(l)
```

## **<mark>第四题</mark>**

编写一个程序，该程序接收控制台以逗号分隔的数字序列，并生成包含每个数字的列表和元组，假设，向程序提供以下输入：34岁,67年,55岁,33岁,12日,98年;则输出为:['34'，'67'，'55'，'33'，'12'，'98] ('34'，'67'，'55'，'33'，'12'，'98')

```
import re
l=input("")
res=re.findall(r"\d+",l)
print(res,end="")
print(tuple(res))
```

## **<mark>第五题</mark>**

定义一个至少有两个方法的类：一、getString：从控制台输入获取字符串；二、

printString：将获取的字符串中的小写字母转为大写字母，并打印整个字符串，并写出简单的测试函数来测试类方法。

```
class Function:

    def getString(self):
        self.l = input("enter string:")  #使用实例属性

    def printString(self):
        print(self.l.upper())
a = Function()
a.getString()
a.printString()  
```

## **<mark>第六题</mark>**

编写一个程序，根据给定的公式计算并打印值：

$$
Q=\sqrt{\frac{2 \cdot C \cdot D}{H}}
$$

其中，假设C=50。H=30。D是一个变量，它的值应该以逗号分隔的序列输入到程序中。例：程序的输入序列为（以逗号分隔）：100，150，180；则程序输出为：18，22，24；
