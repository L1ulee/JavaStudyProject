# LiuleeのJava学习项目

本项目是我学习Java的所有工程文件，其中包括我的笔记和示例

## 当前项目状态

[![](https://img.shields.io/discord/778637533461348374?label=Firstwood&logo=Discord&logoColor=%23FF6EC7)](https://discord.gg/SXtgf3C85d) [![Open Isuues Count](https://img.shields.io/github/issues-raw/L1ulee/JavaStudyProject?label=Open%20issues)](https://github.com/L1ulee/JavaStudyProject/issues) [![License](https://img.shields.io/github/license/L1ulee/JavaStudyProject?label=License)](https://github.com/L1ulee/JavaStudyProject/blob/master/LICENSE) 

## 一、Java基础

### 1. Java基础语法

#### 1.1 HelloWorld

目标:让Java输出Hello,World!

```java
public class HelloWorld{					//创建HelloWorld类
    
    public static void main(String[] args){ //实现主方法main
        
        System.out.println("Hello,Wrold!");	//输出Hello,World!
        
    }
    
}
```

#### 1.2 注释（理解）

注释是对代码的解释和说明文字，可以提高程序的可读性，因此在程序中添加必要的注释文字十分重要。Java中的注释分为三种：

单行注释。单行注释的格式是使用//，从//开始至本行结尾的文字将作为注释文字。

~~~java
// 这是单行注释文字
~~~

多行注释。多行注释的格式是使用/* 和 */将一段较长的注释括起来。

~~~java
/*
这是多行注释文字
这是多行注释文字
这是多行注释文字
*/
注意：多行注释不能嵌套使用。
~~~

文档注释。文档注释以`/**`开始，以`*/`结束。（以后讲）

#### 1.3 关键字

关键字是指被Java语言赋予了特殊含义的单词。

关键字的特点：

​	关键字的字母全部小写。

​	常用的代码编辑器对关键字都有高亮显示，比如现在我们能看到的public、class、static等。

#### 1.4 常量

常量：在程序运行过程中，其值不可以发生改变的量。

Java中的常量分类：

​	字符串常量  用双引号括起来的多个字符（可以包含0个、一个或多个），例如"a"、"abc"、"中国"等

​	整数常量  整数，例如：-10、0、88等

​	小数常量  小数，例如：-5.5、1.0、88.88等

​	字符常量  用单引号括起来的一个字符，例如：'a'、'5'、'B'、'中'等

​	布尔常量  布尔值，表示真假，只有两个值true和false

​	空常量  一个特殊的值，空值，值为null

除空常量外，其他常量均可使用输出语句直接输出。

~~~java
public class Demo {
    public static void main(String[] args) {
        System.out.println(10); // 输出一个整数
        System.out.println(5.5); // 输出一个小数
        System.out.println('a'); // 输出一个字符
        System.out.println(true); // 输出boolean值true
        System.out.println("欢迎来到黑马程序员"); // 输出字符串
    }
}
~~~

#### 1.5 变量的介绍

变量的定义格式：

​	数据类型 变量名 = 数据值；

​	数据类型：为空间中存储的数据加入类型限制。整数？小数？

​	变量名：自己要为空间起的名字，没有难度

​	数据值： 空间中要存储的数值，没有难度

#### 1.6 数据类型（应用）

##### 1.6.1 计算机存储单元

我们知道计算机是可以用来存储数据的，但是无论是内存还是硬盘，计算机存储设备的最小信息单元叫“位（bit）”，我们又称之为“比特位”，通常用小写的字母”b”表示。而计算机中最基本的存储单元叫“字节（byte）”，

通常用大写字母”B”表示，字节是由连续的8个位组成。

除了字节外还有一些常用的存储单位，其换算单位如下：

1B（字节） = 8bit

1KB = 1024B

1MB = 1024KB

1GB = 1024MB

1TB = 1024GB

##### 1.6.2 Java中的数据类型

Java是一个强类型语言，Java中的数据必须明确数据类型。在Java中的数据类型包括基本数据类型和引用数据类型两种。

Java中的基本数据类型：

| 数据类型 | 关键字       | 内存占用 | 取值范围                                                     |
| :------- | ------------ | -------- | :----------------------------------------------------------- |
| 整数类型 | byte         | 1        | -128~127                                                     |
|          | short        | 2        | -32768~32767                                                 |
|          | int(默认)    | 4        | -2的31次方到2的31次方-1                                      |
|          | long         | 8        | -2的63次方到2的63次方-1                                      |
| 浮点类型 | float        | 4        | 负数：-3.402823E+38到-1.401298E-45                                                             正数：   1.401298E-45到3.402823E+38 |
|          | double(默认) | 8        | 负数：-1.797693E+308到-4.9000000E-324                                              正数：4.9000000E-324   到1.797693E+308 |
| 字符类型 | char         | 2        | 0-65535                                                      |
| 布尔类型 | boolean      | 1        | true，false                                                  |

说明：

​	e+38表示是乘以10的38次方，同样，e-45表示乘以10的负45次方。

​	在java中整数默认是int类型，浮点数默认是double类型。

#### 1.7 变量

##### 1.7.1 变量的定义

变量：在程序运行过程中，其值可以发生改变的量。

从本质上讲，变量是内存中的一小块区域，其值可以在一定范围内变化。

变量的定义格式：

```java
数据类型 变量名 = 初始化值; // 声明变量并赋值
int age = 18;
System.out.println(age);
```

或者(扩展)

```java
// 先声明，后赋值（使用前赋值即可）
数据类型 变量名;
变量名 = 初始化值;
double money;
money = 55.5;
System.out.println(money);
```

还可以(扩展)

在同一行定义多个同一种数据类型的变量，中间使用逗号隔开。但不建议使用这种方式，降低程序的可读性。

```java
int a = 10, b = 20; // 定义int类型的变量a和b，中间使用逗号隔开
System.out.println(a);
System.out.println(b);

int c,d; // 声明int类型的变量c和d，中间使用逗号隔开
c = 30;
d = 40;
System.out.println(c);
System.out.println(d);
```

##### 1.7.2 变量的修改

```java
int a = 10;
a = 30;  //修改变量的值
System.out.println(a);
```

变量前面不加数据类型时，表示修改已存在的变量的值。

#### 1.8 变量的注意事项

1. 在同一对花括号中，变量名不能重复。
2. 变量在使用之前，必须初始化（赋值）。
3. 定义long类型的变量时，需要在整数的后面加L（大小写均可，建议大写）。因为整数默认是int类型，整数太大可能超出int范围。
4. 定义float类型的变量时，需要在小数的后面加F（大小写均可，建议大写）。因为浮点数的默认类型是double， double的取值范围是大于float的，类型不兼容。

#### 1.9 键盘录入

我们可以通过 Scanner 类来获取用户的输入。使用步骤如下：

1、导包。Scanner 类在java.util包下，所以需要将该类导入。导包的语句需要定义在类的上面。

```java
import java.util.Scanner; 
```

2、创建Scanner对象。

```java
Scanner sc = new Scanner(System.in);// 创建Scanner对象，sc表示变量名，其他均不可变
```

3、接收数据

```java
int i = sc.nextInt(); // 表示将键盘录入的值作为int数返回。
```

示例：

```java
import java.util.Scanner;
public class ScannerDemo {
	public static void main(String[] args) {
		//创建对象
		Scanner sc = new Scanner(System.in);
		//接收数据
		int a = sc.nextInt();
		//输出数据
		System.out.println(a);
	}
}
```

#### 1.10 标识符

标识符是用户编程时使用的名字，用于给类、方法、变量、常量等命名。

Java中标识符的组成规则：

​	由字母、数字、下划线“_”、美元符号“$”组成，第一个字符不能是数字。

​	不能使用java中的关键字作为标识符。	

​	标识符对大小写敏感（区分大小写）。

Java中标识符的命名约定：

​	小驼峰式命名：变量名、方法名

​		首字母小写，从第二个单词开始每个单词的首字母大写。

​	大驼峰式命名：类名

​		每个单词的首字母都大写。

​	另外，标识符的命名最好可以做到见名知意

​		例如：username、studentNumber等。

