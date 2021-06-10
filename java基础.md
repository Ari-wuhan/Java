# 一、java入门

## java概述

### 什么是Java

作为高级计算机语言，有三个技术平台：

1. Java SE

   为开发普通桌面和商务应用程序

2. Java EE

   为开发企业级应用程序

3. Java ME

   为开发电子产品和嵌入式应用程序

### java特点

​	跨平台

支持多线程

面对对象

## JDK与JRE

什么是JDK？

是Java开发环境。它是整个java对核心，包括java编译器、Java运行工具、Java文档生成工具、Java打包工具等。

什么是JRE？

是Java运行环境，只包含运行工具，没有编译工具。

## 系统环境变量

PATH

​	用于告知操作系统到指定目录去寻找JDK

CLASSPATH

 告知JDK到指定路径去查找类文件（.class)文件

## java运行机制	

1. 编译

   ​	.java（源文件）--编译>>.class（字节码文件）

   > ```java
   > Javac name.java
   > ```
   >
   > 

2. 运行

   java虚拟机对字节码文件进行解释执行

   > ```java
   > Java name
   > ```

## Eclipce运行程序

project>>

package>>

class>>

name.java>>

run as java application

## java常用包

Java.util:

​	包含Java中大量工具类、集合类等

Java.net:

​	包含Java网络编程相关等类和接口

Java.io：

​	包含Java输入、输出的类和接口

Java.awt:

​	包含用于构建图像界面（GUI）的相关类和接口







# 二、Java编程基础

## Java基本语法

声明类

```java
[修饰符] class 类名{

​	代码

}
```

严格区分大小写

连接字符串用“+”

用";"结束语句

可随意换行方便排版

## 注释

单行注释

```java
//用两个斜杠
```

多行注释

```java
/*

这是多行注释

*/
```

文档注释

> ```java
> /** 
> 
> 这是文档注释
> 
> 对程序中某个类或类中的方法进行系统性的说明，使用JDK提供的javadoc工具将文档提取出来生成一份API帮助文档
> 
> */
> ```
>
> 

## 标识符

用于定义名称，如包名、类名、参数名、变量名、方法名等

可由大小写字母、数字、下划线和美元符号（$)组成

但是不能以数字开头，也不能使用关键字

一些规范：

1. 包名字母一律小写

2. 接口和类名首字母大写

3. 常量名所有字母都大写

	4. 变量名和方法名等第一个单词首字母都大写

## 变量

运行程序时产生的数据，会保存在内存单元中，每个单元都用标识符来定义

这些内存单元称之为变量

### 变量定义

定义的标识符就是变量，内存单元中存储的数据就是变量的值

```
变量类型。变量名 = 【初始值】;
```

```java
int x,y;

就是分配两块内存单元给两个变量
```



### 变量的数据类型

分为两类：基本数据类型和应用数据类型

| 基本数据类型 | 引用数据类型 |
| :----------: | :----------: |
|     byte     |      类      |
|    short     |     接口     |
|     int      |     数组     |
|     long     |     枚举     |
|    float     |     注解     |
|    double    |              |
|     char     |              |
|   boolean    |              |





### 变量的类型转换

自动（隐式）类型转换

​	当把一个类型取值范围小的数值直接赋给一个类型取值范围大的数值时，系统会自动进行类型转换

​	表达类型会自动提升，即取值范围自动变大

强制（显式）类型转换

> 目标类型 变量名 = （目标类型）值;

```java
JAVAint n =10;

byte b =(byte)n;
```

### 变量的作用域

变量一定会被定义在一对大括号中，该大括号就是所包含的代码区域即该变量的作用域。

## 常量

### 常量类型

| 整型常量      | 浮点数常量                         | 字符常量                                     | 字符串常量                                            | 布尔常量                 | NULL常量                                   |
| ------------- | ---------------------------------- | -------------------------------------------- | ----------------------------------------------------- | ------------------------ | ------------------------------------------ |
| 二进制 0b110  | 指数形式：2e3f   2e3d   以f或d结尾 | ‘ a’    表示一个字符，用英文半角格式的单引号 | “ abcdefg”.  表示一连串的字符，用英文半角格式的双引号 | false和true,区分条件真假 | null常量只有一个值null，表示对象的引用为空 |
| 八进制  0766  |                                    |                                              |                                                       |                          |                                            |
| 十进制  289   |                                    |                                              |                                                       |                          |                                            |
| 十六进制 0x67 |                                    |                                              |                                                       |                          |                                            |

​	

### 定义常量

> final 常量类型  常量名 = 【初始值】;
>
> ```java
> final String name = "wuhan";
> ```
>
> 

## 转义符----反斜杠\

> \r------回车符
>
> \n-----换行符
>
> \t-----制表符
>
> \b----退格符，==backspace

## 运算符

### 算术运算符

/  取整除

// 除法

% 取余---运算结果的符号取决于被模数（%左边的数），而与右边的数无关

++ 自增1

--  自减1

---

### 赋值运算符

=

+=   加等于

-=   减等于

*=  乘等于

/=。 除等于

%=   模等于

---

### 比较运算符

== 等于

！= 不等于

<  > 小于 大于

<= >= 小于等于 大于等于

---

### 逻辑运算符

& 与---全真为真

｜ 或---有真为真

^  异或---异为真

！  非---真假互换

&&  短路与 左边为false时，右边表达式不会运行

｜｜  短路或  左边为true时，右边不会运行

---

### 位运算符---两边都是单一数值	

& 按位与

｜ 按位或

～ 取反

按位异或

右移>>

左移<<

---

### 条件运算符

（statements）?true_statement:false_statement;

基本等价于if--else

## 选择结构语句

### if

> ```java
> if (判断条件){
> 
> 条件满足时执行语句
> 
> }
> ```
>
> 

---

### if---else

> ```java
> if(判断条件1){
> 
> 条件1满足时执行语句
> 
> }
> 
> else(判断条件2){
> 
> 条件2满足时执行语句
> 
> }
> ```
>
> 

---

### if...else if ...else

> i
>
> ```java
> f(判断条件1){
> 
> 条件1满足时执行语句
> 
> }
> 
> else if(判断条件2){
> 
> 条件2满足时执行语句
> 
> }
> 
> ...
> 
> else if(判断条件n){
> 
> 条件n满足时执行语句
> 
> }
> 
> else{
> 
> 以上条件都不满足时执行语句
> 
> }
> ```
>
> 
>

---

### switch条件语句

> ```java
> switch(//控制表达式){
> 
> Case //目标值1:
> 
> 	//条件满足目标1时执行语句
> 
> 	break;//跳出该switch语句
> 
> Case //目标值2:
> 
> 	//条件满足目标2时执行语句
> 
> 	break;//跳出该switch语句
> 
> ...
> 
> Case //目标值n:
> 
> 	//条件满足目标n时执行语句
> 
> 	break;//跳出该switch语句
> 
> 
> 
> default:
> 
> 	//以上条件都不满足时执行语句
> 
> 	break;//跳出该switch语句
> 
> }
> ```
>
> 

---

## 循环结构语句

### while

>```java
>while(循环条件){
>
>条件满足时执行语句
>
>}
>```
>
>

### do...while

> ```java
> do{
> 
> 在判断条件前先执行一遍这段代码,然后进入条件判断，看是否继续执行这段代码
> 
> }
> 
> while(判断条件);
> ```
>
> 

### for

> ```java
> for(1;2;3){
> 
> 4
> 
> }
> 
> /*
> 
> 第一步，先执行1
> 
> 第二步，执行2，如果条件为true，执行第三步，负责跳出循环
> 
> 第三步，执行4
> 
> 第四步，执行3，在重复第二步
> 
> */
> ```
>
> 

## 跳转语句

### break

跳出当前循环，执行后面大代码

在嵌套循环里，很自私默认跳出当前所在循环，内循环或外循环

### continue

终止本次循环，执行下一次循环

## 数组

### 数组定义

>```java
>//第一种
>
>//数组类型 [] 数组名 = new 数组类型 [数组长度];
>
>int [] id = new int [100];
>
>//第二种
>
>//数组类型 [] 数组名 = new 数组类型 []{数组元素0，数组元素1}；
>
>int	[] ids = new int {1,2,3,4};
>
>//第三种
>
>//数组类型 [] 数组名 =  {数组0，数组1...};
>
>int	[] ids = {1,2,3,4};
>```
>
>

### 数组常见操作

数组名.length获取数组长度，即数组元素 个数

#### 数组遍历

> ```java
> int [] arr = {1,2,3,4};//定义数组
> 
> for(int i =0;i<arr.length;i++){//for循环遍历数组
> 
> System.out.println(arr[i]);//通过索引访问数组元素
> 
> }
> ```
>
> java

#### 数组最值

> ```java
> int	[] arr = {1,2,4,3,7,9,10};//定义一个数组
> 
> int max = arr[0];//定义变量max用于记住最大数，首先假定第一个数最大
> 
> for(int i=1;i<arr.length;i++){//遍历数组，找最大值
> 
> if(arr[i]>max){//比较arr[i]大值是否大于max
> 
> max	=  arr[i];//条件成立，把arr[i]大值赋给max
> 
> }
> 
> System.out.println(max);
> 
> }
> ```
>
> 

#### 数组排序

冒泡排序，不断地比较数组中相邻的两个元素，较小的向上浮，较大的向下沉

> ```java
> int	[] arr={23,4,3,15,90};
> 
> //排序前打印数组元素
> 
> for(int i =0;i<arr.length;i++){
> 
> System.out.println(arr[i]+" ");
> 
> }
> 
> System.out.println();
> 
> for(int i =1;i<arr.length;i++){//外循环定义比较多轮次，n-1轮
> 
> for(int j=0;j<arr.lengh-i;j++){//内循环定义第i轮需要比较的两个数
> 
> if(arr[j]>arr[i]){//比较相邻元素
> 
> int t = arr[j];//进行交换
> 
> arr[j] = arr[j+1];
> 
> arr [j+1] = t;
> 
> }
> 
> }
> 
> }	
> 
> //排序后，打印数组元素
> 
> for(int i =0;i<arr.length;i++){
> 
> System.out.println(arr[i]+" ");
> 
> }
> ```
>
> 

---

### 多维数组

> ```java
> int	[][] [] [] arr =new int [3] [3];
> 
> int	[] []arr ={(1,2),(3,4)};
> ```
>
> 

---

# 三、面对对象（上）

## 面对对象概述

在程序中使用对象来映射现实中的事物，使用对象的关系来描述事物之间的关系，这就是面对对象。

面对对象的特点：

1. 封装

   将对象的属性和行为封装起来，不让外界知道哪部具体细节

2. 继承

   描述的数类与类之间的关系，通过继承，可以无需重新编写原有类的情况下，对原有类的功能进行拓展

3. 多态

   多态指的是在一个类中定义的属性和功能被其他类继承后，当把子类对象直接赋值给父类引用变量时，相同引用类型的变量调用同一个方法所呈现出的多种不同行为特性

## Java中的类与对象

### 类与对象的关系

类是对某一类事物的抽象描述

对象是用于表示现实中该类的个体

如人类是类，每一个人都是类中的每一个对象

### 类的定义

> ```java
> [修饰符]  class 类名 [extends 父类名] [implements 接口名]{
> 
> //类体，包括类的成员变量和成员方法
> 
> //成员变量
> 
> //	[修饰符] 数据类型 变量名 = [值];
> 
> //	private int a =10;
> 
> //成员方法
> 
> //	[修饰符] [返回值类型] 方法名([参数类型 参数名1，参数类型 参数名2]...){
> 
> //		//方法体
> 
> //		...
> 
> //	return 返回值;//当返回值为void时，return及其返回值可以省略
> 
> }
> 
> public class Person{
> 
> 	int age;
> 
> 	void speak(){
> 
> 		System.out.println(“我今年"+age+"岁了！");
> 
> }
> 
> }
> 
> }
> ```
>
> 

在类在定义的变量称为成员变量，在方法中定义的变量称为局部变量。当成员变量和局部变量重名时，方法采用局部变量

### 对象的创建和使用

应用程序要完成具体的功能，仅仅有类时不够的，还要根据类创建实例对象。

在java中使用new创建实例对象

> ```java
> 类名 对象名称 = new 类名（）;
> 
> Person p = new Person();
> 
> /*	new Person()用于创建一个实例对象（内存会分配一个堆内存）
> 
> 		Person p声明一个Person类型的变量p(内存会分配一个栈内存)
> 
> 		中间的等号则是用于将Person对象在内存中的地址赋值给变量p
> 
> 		这样变量p变持有了对象的引用
> 
> 		Persn类型变量p只是一个引用，会指向真正的对象new Person()
> 
> */
> ```
>
> 

创建实例对象后，就可以通过变量名引用成员变量和成员方法

> ```java
> p.spaek()
> 
> p.a=18;
> ```
>
> 

也可以通过创建的对象本身来引用对象成员：

> ```java
> new 类名().对象成员
> 
> new Person().speak();
> ```
>
> 

而当对象被实例化后，如果没有任何变量来引用这个对象，那么这个对象就会成为垃圾对象，被回收

### 访问控制符

| private | default | protected | public   |
| ------- | ------- | --------- | -------- |
| 同一类  | 同一包  | 子类中    | 全局范围 |

  	

## 类的封装

#### 为什么要进行封装

设计一个类时，为了对成员变量的访问做一个限制，不允许外界随意访问内部成员变量，就需要对类进行封装

#### 怎样进行封装

定义类时，将类中的属性私有化，即用private修饰，是的私有属性只能在本类中访问。如果外界想要访问私有属性，则需要提供一些public修饰的共有方法，就包括获取属性值的getxxx()方法和设置属性值的setxx():

> ```java
> public Person(){
> 
> 	private int age;
> 
> 	private String name;
> 
> 	public int getAge(){
> 
> 		return age;
> 
> }
> 
> 	public void setAge(int age){
> 
> 	this.age= age
> 
> }
> 
> 	public String getName(){
> 
> 	return name;
> 
> }
> 
> 	public void setName(String name){
> 
> 	this.name =name;
> 
> }
> 
> }
> ```
>
> 

## 方法的重载和递归

方法的重载：

​	在程序中同一个方法因参数个数和类型的不同分很多种调用情况，所以需要同一种方法名使用不同的参数个数和类型来实现不同情况的方法调用，这就是重载。即同名方法采用不同的参数个数或参数类型

方法的递归：

​	方法的递归时在一个方法内部调用自身的过程。递归必须有结束条件，不然会陷入死循环

## 构造方法

在实例化对象的同时为这个对象的属性进行赋值，构造方法时类的特殊方法，会在类实例化对象时被调用

类中至少有一个无参数的构造方法，因为会默认调用无参的构造方法。如果没有显式地定义构造方法，系统会自动为这个类创建一个默认的无参数的无方法体的构造方法。

如果定义了有参数的构造方法，必须再定义一个无参数的构造方法，因为定义了有参的构造方法后，系统默认的无参构造方法以及不存在了

构造方法的定义：

> 3. ```java
>    //[修饰符] 方法名（参数列表）{
>    
>    //方法体
>    
>    }
>    
>    public	Person(int a){
>    
>    	int age= a;
>    
>    }	
>    
>    /* 
>    
>    	要满足三个条件：
>    
>    1. 方法名和类名同名
>    
>    2. 无返回值，
>    
>    3. 不能使用return返回一个返回值，但可以单独写语句来作为结束
>    
>       */
>    ```
>    
>    

#### 构造方法的重载

> ```java
> class Person(){
> 
> int age;
> 
> public	Person(){
> 
> 	System.out.println("eat");
> 
> }
> 
> public	Person(int a){
> 
> 	int age= a;
> 
> }
> 
> }
> ```
>
> 

## this关键字

this关键字指代当前对象，用来在方法中访问对象的其他成员。

#### this调用成员变量

this调用成员变量，来解决与局部变量重名的问题

> ```java
> class	Person(){
> 
> int age;//成员变量
> 
> public	Person(int age){//局部变量
> 
> this.age =age;//将局部变量赋值给成员变量
> 
> }
> 
> }
> ```
>
> 

#### this调用成员方法

> ```java
> class	Person(){
> 
> 	public	void speak(){
> 
> .....
> 
> }
> 
> public	void talk(){
> 
> 	this.speak();
> 
> }
> 
> }
> ```
>
> 

#### this调用构造方法

通过使用不同参数个数和类型来调用不同的构造方法

this调用构造方法必须在构造方法内

this调用构造方法必须在构造方法第一行

> ```java
> class	Person(){
> 
> 	int age;
> 
> 	public	Person(){
> 
> 	...
> 
> }
> 
> 	public Person(int age){
> 
> 		   this();
> 
> 			this.age=age;
> 
> 		
> 
> }
> 
> }
> ```
>
> 

## static关键字

修饰类的成员：成员变量、成员方法、代码块

### 静态变量

static只能修饰成员变量，不能修饰局部变量

使用static修饰成员变量，使之被所有实例共享

访问静态变量：

> ```java
> 类名.变量名
> 
> Person.age;
> ```
>
> 

### 静态方法

在之前，要使用类中的方法，要先实例化对象才能使用对象中的成员方法。

而静态方法，可以直接使用，不用创建对象。

访问静态方法：

> ```java
> //类名.方法
> 
> //类名.方法
> 
> class	Person(){
> 
> 	public static void say(){
> 
> 		System.out.println("hello!");
> 
> }
> 
> }
> 
> public class Test(){
> 
> 	public static void main(String[] args){
> 
> //类名.方法。调用
> 
> 	Person.say();
> 
> //类名.方法 调用
> 
> Person p = new Person();
> 
> p.say();
> 
> }
> 
> }
> ```
>
> 

### 静态代码块

利用静态代码块只执行一次的特点，使用静态代码块来对成员变量进行初始化

> ```java
> static{
> 
> 	System.out.println("hello!");
> 
> }
> ```
>
> 

# 四、面对对象（下）

## 类的继承

###  继承的概念

在现有类的继承上创建一个新的类，原有的类称为父类，新创建的类称为子类。子类会自动拥有父类所有可继承的属性和方法

继承使用extends关键字

> ```java
> [修饰符] class 子类名 extends 父类名{
> 
> }
> ```
>
> 

只支持单继承，即只可继承一个父类

### 重写父类方法

在继承父类可继承的方法后，可根据需要对父类方法进行重写

重写方法要和父类方法具有相同的方法名、参数列表和返回值类型

>```java
>class	Animal(){
>
>	void say(){
>
>	System.out.println("***");
>
>}
>
>}
>
>class Dog extends Animal(){
>
>	void say(){
>
>		System.out.println("汪汪汪！");
>
>}
>
>}
>```
>
>

### super关键字

当父类被重写后，子类无法访问父类被重写的方法

此时可以使用super来访问父类的成员变量、方法、构造方法：

> ```java
> //super.成员变量
> 
> //super.成员变量（参数列表1，参数列表2...)
> 
> //super(参数1，参数列表2...)
> 
> class	Animal(){
> 
> 	String name="动物";
> 
> 	void say(){
> 
> 	System.out.println("***");
> 
> }
> 
> 	public Animal(){
> 
> System.out.println("我是动物");
> 
> }
> 
> }
> 
> class Dog extends Animal(){
> 
> 	String name="小狗";
> 
> 	void say(){
> 
> 		System.out.println("汪汪汪！");
> 
> }
> 
> 	super.say();
> 
> 	public Dog(){
> 
> 		super();
> 
> }
> 
> System.out.println(name+"是"+super.name);
> 
> }
> ```
>
> 

通过super调用父类构造方法时，super语句要放在构造方法第一行

### Object类

Object类时所有类的父类

如果一个类没有显式地继承其他类，则默认继承Object类

常用方法:

​	equals()比较两个对象是否相等

​	getClass()返回此Object的运行时的类

​	hashCode()返回该对象的哈希码值

​	toString()返回该对象的字符串显示

​	finalize()垃圾回

## final关键字

 #### final关键字修饰类

> ```java
> final	public class A{
> 
> }
> ```
>
> 

final修饰的类无法被继承

#### final关键字修饰方法

> ```java
> public class A{
> 
> 	final void speak(){
> 
> }
> 
> }
> ```
>
> 

final修饰的方法无法被重写

#### final关键字修饰变量

>  ```java
>  public	class A{
>  
>  final n= 100;
>  
>  }
>  ```
>
>  

final修饰的变量为常量，无法被修改

## 抽象类和接口

### 抽象类

方法中除了有成员方法外，还要抽象方法的为抽象类

在类中提供方法，但是不实现方法，即方法体为空

使用abstract 来修饰

> ```java
> [修饰符] abstract class 类名{
> 
> 	[修饰符] abstract 方法返回值类型 方法名 (参数列表)；
> 
> }
> 
> abstract	class A{
> 
> 	public abstract void say();
> 
> 	public void do(){
> 
> 		System.out.println("getup!");
> 
> }
> 
> }
> 
> class B extends A{
> 
> public	 void say(){
> 
> 	System.out.println("hello!");
> 
> }
> 
> }
> 
> public	class Test{
> 
> public static void main(String[] args){
> 
> 	A a =new A();
> 
> 	a.say();
> 
> }
> 
> }
> ```
>
> 

子类实现了父类的抽象方法后，就可以实例化对象，通过实例化的对象来调用实现的方法了

### 接口

抽象类中的方法全为抽象方法，则为接口

接口说一直特殊的抽象类

JDK8定义接口中除了有抽象方法，还可以有默认方法和静态方法

> ```java
> [修饰符] interface 接口名 [extends 父接口1，父接口2...]{
> 
> 	[public] [static] [final] 常量类型 常量名 = 常量值;
> 
> 	[public] [abstract] 方法返回值类型 方法名(参数列表);
> 
> 	[public] default 方法返回值类型 方法名(参数列表){
> 
> 	//默认方法
> 
> }
> 
> [public] static 方法返回值类型 方法名(参数列表){
> 
> 	//静态方法
> 
> }
> 
> }
> ```
>
> 

实现接口:

> ```java
> [修饰符] class 类名 [extends 父类名] [implements 接口1，接口2]{
> 
> }
> ```
>
> 

Example：

> ```java
> interface	Animal{
> 
> 	int id =1；
> 
> 	void say();
> 
> 	default void getName(String name){
> 
> 		System.out.println("name!");
> 
> }
> 
> static int getId(){
> 
> 	return Anima.id;
> 
> } 
> 
> }
> 
> class	Dog implements Animal(){
> 
> 	void say(){
> 
> 	System.out.println("汪汪汪!");
> 
> }
> 
> }
> 
> public	class Test{
> 
> public	static void main(String [] args){
> 
> 	Dog d =new Dog();
> 
> 	d.say();
> 
> System.out.println(d.getId);
> 
> d.getName();
> 
> }
> 
> }
> ```
>
> 

## 多态

### 多态概述

多态是指不同类的对象在调用同一个方法时所呈现的不同行为

在一个类中定义的属性和行为别其他类继承或重写后，当把子类对象直接赋值给父类对象引用变量时，相同引用变量调用同一个方法将呈现多种不同形态

Java的多态时通过继承、方法重写以及父类引用指向子类对象体现的

由于父类有多个子类，不同子类重写的父类方法不同，多个不同子类都可指向同一个父类；只有程序在运行时才知道具体代表的是哪个子类对象，这就体现了多态性。

比如：

> ```java
> abstract class	A{
> 
> 	abstract void say(); 
> 
> }
> 
> class	B extends A{
> 
> 	void say(){
> 
> 	System.out.println"(B");
> 
> }
> 
> }
> 
> class	C extends A{
> 
> 	void say(){
> 
> 	System.out.println("C");
> 
> }
> 
> }
> 
> public class Test{
> 
> 	public static void main(String[] args){
> 
> 	B b =new B();
> 
> 	C c =new C();
> 
> 	b.say();
> 
> 	c.say();
> 
> }
> 
> }
> ```
>
> 

### 对象的类型转换

向上转型：子类对象当作父类类型使用

> ```java
> A a1 =new B();//把B类型对象当作父类A类型来使用
> A a2 =new C();//把C类型对象当作父类A类型来使用
> 
> 向上转型不需要显式的声明，不能通过父类变量去调用子
> 类特有的方法。因为子类已经自动向上转型为了父类对象，就无法调用子类所特有的方法了
> 
> 向下转型：父类对象当作子类类型使用,需要强制转换    
> ```

> ```java
> A a1 =new B();//把B类型对象当作父类A类型来使用
> 
> B b = (B) a1;//进行向下转型，a1转换成B类型,就可以使用子类特有方法了
> ```
>
> 

但时向下转型只能说转为本质类型，如上面的a1，本身B类型，所以，向下转型为B是正确的，但是向下转型为A类型就会报错

为了避免转换时发生上面的错误，采用关键字instanceof来判断一个对象是否为某个类(或接口)的实例或者子实例：

> ```java
> //对象（或对象引用变量) instanceof 类（接口）
> 
> A a1 =new B();
> 
> if(a1 instanceof B){//判断本质类型
> 
> 	B b = (B) a1;//是B类型，向下转型
> 
> }
> 
> else if(a1 instanceof C){//判断本质类型
> 
> 	A a2 =new C();//是C类型，向下转型
> 
> }
> 
> else{
> 
> System.out.println("该类型无法向下转型！");
> 
> }
> ```
>
> 

## 内部类

Java允许在一个类的内部定义类，这样的类称为内部类，内部类所在的类称为外部类

### 成员内部类

在一个类中除了可以定义成员变量、成员方法和构造方法外，还可以定义类，这样的类称为成员内部类。

成员内部类可以访问外部类的所有成员，外部类也可以访问内部类的所有员

> ```java
> class	A{
> 
> int age =10;
> 
> 	class B{
> 
> 	System.out.println(age);
> 
> }
> 
> }
> 
> //main方法中实例化外部类
> 
> A a = new A();
> 
> //main方法中实例化内部类
> 
> 外部类名.内部类名 变量名 = 外部类名.new 内部类名();
> 
> A.B in = A.new B()；
> ```
>
> 

### 局部内部类

​	也叫方法内部类，和局部变量一样，在方法内定义，有效范围只在方法范围内

局部内部类可以访问外部类的所有成员，而局部内部类的成员只能在创建这个局部内部类的方法中访问

> ```java
> class	A{
> 
> void say()
> 
> 		class In{
> 
> 		int i =10;
> 
> 		In i = new In();
> 
> 		System.out.println(i);
> 
> }
> 
> }
> ```
>
> 

### 静态内部类

静态内部类即使用static修饰的成员内部类，外部类可以访问静态内部类，而静态类只能访问外部类的静态成员

通过外部类访问静态内部成员时，，可以跳过外部类直接访问

> ```java
> class A{
> 
> static n =10;
> 
> 	static class B{
> 
> 			void show(){
> 
> 				System.out.println(n);
> 
> }
> 
> }
> 
> }
> 
> //创建静态内部类对象
> 
> A.B in = new A.B();
> 
> in.show();
> ```
>
> 

### 匿名内部类

一个方法的参数时一个接口时，除了使用接口，还可以使用匿名内部类实现接口传入方法中

匿名内部类用来作为一个参数传入以接口为接收参数的方法中：

> ```java
> new 父接口{
> 	匿名内部类实现接口
> 
> >}
> 
> interface A{
> 
> >void show();
> 
> }
> 
> class	B{
> 
> //定义匿名内部类作为参数传递给getShow()方法
> 
> 	getShow(new A(){
> 
> 	public vois show(){
> 
> 		System.out.println("hello");
> 
> >}
> 
> });
> 
> >}
> 
> //定义静态类型方法，接收接口类型参数
> 
> public static void getShow(A a1){
> 
> a1.show();
> 
> }
> ```
>
> 
>

## Lambda表达式

### 初识Lambda表达式

用一个简洁的表达式来表达接口

这种表达式只针对一个抽象方法的接口实现，以简洁的表达式作为接口实现接口参数传入方法

>```java
>(参数列表1，参数列表2...) -> (表达式)
>
>//前面的参数列表时指传入的参数
>
>//->指定参数数据指向
>
>//表达式即抽象方法的具体实现
>```
>
>

### 函数式接口

所谓函数式接口，就是只有一个抽象方法的接口

@FunctionalInterface注解：显式标注该接口是一个函数式接口

### 方法引用与构造器引用

当Lambda表达式主体部分只有一条语句时，可以省略主体部分大括号，通过英文双冒号"::"来引用方法和构造器

#### 类名引用静态方法

> ```java
> @FunctionalInterface
> 
> interface Do{
> 
>      void showtime(int n);
> 
> }
> 
> class A{
> 
> static void show(){
> 
> System.out.println("hello");}
> 
> }
> 
> ......(-10,A::show());
> 
> .....(-10,n->A.show());
> ```
>
> 



#### 对象引用方法

> ```
> A a =new A();
> 
> ....("Hello"->t.show())
> 
> ...("Hello"t::show())
> ```
>
> 

#### 构造器引用方法

c

```java
lass A{

	public A(String name){

		this.name=name

}

}

.....("吴晗",name-new A(name));

...("吴晗",A::name);
```



#### 类名引用普通方法

> ```java
> class	A{
> 
> 	public void show(String name){
> 
> 		System.out.println(name);
> 
> }
> 
> }
> 
> .....(("wuhan"),->A.show())
> 
> ...("wuhan"),A::show();
> ```
>
> 

## 异常

### 异常类体系

异常类都继承自java.lang.Throwable类

| Error----错误类，系统内部问题，修改程序无法恢复 | Exception-----程序本身的错误         |
| ----------------------------------------------- | ------------------------------------ |
| AWTError                                        | 其他子类-----表示编译时的错误        |
| OError                                          | RuntimeException----程序运行时的错误 |
| 其他子类                                        |                                      |



| RuntimeException----程序运行时的错误    |
| --------------------------------------- |
| ClassCastException-----类型转换异常     |
| ArithmeticException----算术异常         |
| IndexOutOfBundsException---下表越界异常 |
| NullPointerException------空指针异常    |
| NumberFormatException-----数字格式异常  |



### 异常类型

编译时异常

除了RuntimeException----程序运行时的错误之外都是编译异常

运行时异常

RuntimeException类及其子类

### try...catch和finally

当程序发生异常时，会立即终止	     无法继续进行。为保证程序能有效执行，Java提供了对异常有效处理的方式------异常捕获

> ```java
> try{
> 
> 	//可能发生异常的语句
> 
> }catch(Exception类或其子类  e){
> 
> 	//对捕获的异常进行相应处理
> 
> }
> ```
>
> 

有时候会希望程序无论是否发生异常都要执行，这时候就可以在try...catch语句后，加一个finally{}语句块

> ```java
> try{
> 
> 	//可能发生异常的语句
> 
> }catch(Exception类或其子类  e){
> 
> 	//对捕获的异常进行相应处理
> 
> }finally{
> 
> //无论程序是否有异常，这段代码块一定会执行
> 
> }
> ```
>
> 

### throws关键字

将异常抛出，用在会抛出异常的方法名后面，并且支持同时一次抛出多个异常：

> ```java
> [修饰符] 返回值类型 方法名 ()[参数类型 参数1] [参数类型 参数2]...)throws 异常1，异常2....{
> 
> }
> 
> public static int chufa(int x, int y)throws Exception{
> 
> 	int result = x/y;
> 
> 	return result;
> 
> }
> ```
>
> 

### throw关键字

throw也是抛出异常，但是时用于方法内，并且抛出的是一个异常类对象

用throw抛出异常后，要需要用try..catch或throws对异常进行处理

> ```java
> [修饰符] 返回值类型 方法名 ([参数类型 参数名]，...){
> 
> ​	throw new Exception类或其子类构造方法;
> 
> }
> 
> .........throws Exception{
> 
> .......throw new Exception("***");
> 
> }
> 
> try	{
> 
> .....
> 
> }catch(Exception){
> 
> 	.........
> 
> }
> ```
>
> 

### 自定义异常

Java允许用户自定义异常，但时必须继承自Exception及其子类

> ```java
> public class DefindeEooro extends Exception{
> 
> 	public DefindeEooro(){
> 
> 		super();
> 
> }
> 
> 	public DefinedException(String message){
> 
> 		super(message);
> 
> }
> 
> }
> ```
>
> 

### 垃圾回收

Java虚拟机会回首垃圾对象所占有的内存空间

但也可以强制进行垃圾回收

1. 调用System类的gc()静态方法：Syste.gc()

2. 调用Runtime对象的gc()实例：

   Runtime.getRuntime().gc()

finalize方法：进行资源回收整理，时定义在Object类中的实例方法

# 五、Java中的常用类

## String类和StringBuffer类

### String类的初始化

1. 使用字符串常量：

> ```java
> String  变量名 = 字符串;
> 
> String name = "wuhan";
> ```
>
> 

2. 使用String构造方法初始化字符串对象：

> ```java
> String 变量名= new String(字符串);
> 
> String name = new String("wuhan");
> ```
>
> 

String常用构造方法：

> ```java
> String()//创建空字符串
> 
> String name=new String();
> 
> String (String value)//根据指定的字符串内容创建对象
> 
> String name=new String("wuhan");
> 
> String(char [] value)//根据指定的字符串数组创建对象
> 
> char []  arr ={'a','b','c};
> 
> String name=new String(arr);
> ```
>
> 

### String类的常用操作

#### 字符串的基本操作

> ```java
> name.length/()/字符串长度;
> 
> name.charAt(i)//字符串中第i个字符串
> 
> name.indexOf('A')//字符串第一次出现的位置
> 
> Name.lastIndexOf//字符串最后一次出现的位置
> ```
>
> 

#### 字符串的转换操作

> ```java
> System.out.printlm(name.toCharArray);//转换成字符数组
> 
> System.out.printlm(name.toUpperCase());//全转换成大写
> 
> System.out.println(String.valueof(12));//数值转换成String类型
> 
> System.out.println(name.tolowerCase())//转换成小写;
> ```
>
> 

#### 字符串的替换和去除空格操作

> ```java
> System.out.printlm(name.strim());//去除空格
> 
> System.out.printlm(name.replace(" ",""));//用空字符替换空格
> ```
>
> 

#### 字符串的判断操作

> ```java
> System.out.println(name.startWith('a'));//判断是否以a开头
> 
> System.out.println(name.endWith('a'));//是否以a结尾
> 
> System.out.println(name.contains("a"));//是否包含a
> 
> System.out.println(name.isEmpty());//是否为空
> 
> System.out.println(name.equals("wuhan"));//判断两个字符串是否相等
> ```
>
> 

#### 字符串的截取和分割

> ```java
> System.out.println(name.substring(i));//截取到第i个字符
> 
> System.out.println(name.split(","));//按照","进行分割，会分成几个部分
> ```
>
> 

### StringBuffer类

长度和内容都可变，而String长度和内容不可变

StringBuffer类常用操作

> ```java
> //增
> 
> System.out.println(name.append("and"));
> 
> //删
> 
> System.out.println(name.delete(0,2));//删除索引0-2
> 
> //改
> 
> System.out.println(name.set(1,'d'));//指定索引处内容改为目标内容
> 
> System.out.println(name.toString());//返回缓冲区的字符串对象
> ```
>
> 

## System类与Runtime类

### System类

#### getProperties()方法---获取系统属性

用于获取系统全部属性，该方法会返回一个Properties对象，所以要实例化对象

> ```java
> Properties p = System.out.getProperties();
> 
> System.out.println(p);
> ```
>
> 

#### currentTimeMillis()----返回时间戳

表示到19870年1月1日0点0分之间的时间差，单位时毫秒，也称为时间戳

返回的是一个long类型的值

> ```java
> long	time = System.currentTimeMillis();
> 
> System.out.println(time);
> ```
>
> 

#### arraycopy(name1,start1,name2,start2,length)----数组拷贝

源数组，源数组中开始拷贝元素的起始位置，目标数组，拷贝到目标数组的起始位置，拷贝元素的个数

> ```java
> name="wuhan";
> 
> wife="zhaoxin";
> 
> System.arraycopt(name,1,wife,0,5);
> ```
>
> 

#### gc()-----启动垃圾回收

> ```java
> System.gc();
> ```
>
> 

#### exit(i)---终止当前正在允许的虚拟机

i通常指定为0

### Runtime类

Runtime类表示Java虚拟机运行时的状态，用于封装Java虚拟进程

每次用java启动虚拟机都会对应一个实例，但是应用程序不能自己创建自己的Runtime实例，可通过getRuntime()方法获取：

> Runtime r = Runtime.getRuntime()

#### exec()，用于实现DOS命令

> ```java
> Runtime r = Runtime.getRuntime()
> 
> r.exec("qq.exe");//打开QQ
> 
> //exec()方法会产生一个Process对象，该对象表示操作系统的一个进程
> 
> Process p = r.exec("qq.exe");
> 
> p.destory();//关闭进程
> ```
>
> 



## Math类与Random类

### Math类

Math类构造方法被定义为pricate，所以无法创建Math类的对象。但是所以方法都是静态方法，可以直接用类名来调用他们。常量PI即圆周率,E即e

#### 绝对值Math.abs()

#### 正弦Math.sin()

#### 余弦Math.cos()

#### 正切Math.tan()

#### 平方根Math.sqrt()

#### 立方根Math.cbrt()

#### 乘法Math.pow()

#### 四舍五入Math.round()

#### 0-1的随机数Math.random()

---

### Random类

产生不同类型的随机数

> ```java
> Random r = new Random();
> 
> r.nextBoolean();//boolean类型
> 
> r.nextInt();//整型
> 
> r.nextDouble();double型
> 
> r.nextFloat();//float型
> 
> r.nextong()//log型
> ```
>
> 



## 包装类

很多类只接收引用类型的对象，基本数据类型无法传入

而通过包装类，将8种基本数据类型的值 包装为引用数据类型的对象

| 基本数据类型 |  包装类   |
| :----------: | :-------: |
|     int      |  Integer  |
|     byte     |   Byte    |
|     char     | character |
|    cshort    |   Short   |
|     long     |   Long    |
|    float     |   Float   |
|    double    |  Double   |
|   boolean    |  Boolean  |

​			

在基本数据类型和包装类进行转换的过程中，引入了自动装箱和自动拆箱的概念

自动装箱：

​	将基本数据类型数据包装成包装类

> ```java
> int	a =20;
> 
> Integer b =a;
> ```
>
> 

自动拆箱：

​	将包装类对象赋值给基本数据类型变量

```java
int c =b;
```



## 日期与时间类

### Date类

只有两个构造方法可以使用：

Date()------创建当前日期时间的Date对象

Date(long date)----创建指定日期的Date对象，其中date是指时间戳

> ```java
> Date date1 = new Date();
> 
> Date date2 = new Date(System.currentTimeMillis());
> ```
>
> 

### Calendar类

可用于读取时间的年、月、日、分、秒。

是一个抽象类，不能实例化

需要用其静态方法getInstance()来获得一个Calendar对象

> ```java
> Calendar c = Calendar.getCalendar();
> 
> //获取年月日
> 
> Int year = c.get(Calendar.YEAR);
> 
> Int month  = c.get(Calendar.MOUTH);
> 
> int date  = c.get(Calendar.DATE);
> 
> int hour  = c.get(Calendar.HOUR);
> 
> int minute  = c.get(Calendar.MINUTE);
> 
> int	second  = c.get(Calendar.SECEND);
> 
> //设定指定日期，并给日期增加时间
> 
> c.set(2021,6,8);
> 
> c.add(Calendar.DATE,100);
> ```
>
> 

### JDK8的日期与时间类

## 格式化类

### DateFormat类

输出中文格式的时间

是一个抽象类，不能被实例化，但是可通过静态方法来获取实例对象

> ```java
> Date date = new Date();
> 
> //完整格式
> 
> DateFormat full=DateFormat.getDateInstance(DateFormat.FULL);
> 
> System.out.println(full.format(date));
> 
> //Long格式
> 
> DateFormat Long=DateFormat.getDateInstance(DateFormat.LONG);
> 
> System.out.println(Long.format(date));
> 
> //MEDIUM格式
> 
> DateFormat medium=DateFormat.getDateInstance(DateFormat.MEDIUM);
> 
> System.out.println(medium.format(date));
> ```
>
> 

parse()将字符串解析为Date对象

> ```java
> //创建DateFormat对象
> 
> DateFormat d = DateFormat.getDateInstance();
> 
> String s = "2018-01-27";
> 
> System.out.println(d.parse(s));
> ```
>
> 

### SimpleDateFormat类

作为DateFormat子类，可以更好的格式化日期，解析字符串

可以使用new实例化对象，在创建对象时，需要接受一个考试日期格式模板的字符串参数

> ```java
> //创建一个SimpleDateFormat对象
> 
> SimpleDateFormat s = new SimpleDateFormat("Gyyyy年MM月dd日：今天是yyyy年的第D天，E");
> 
> //按SimpleDateFormat对象的日期模板格式对象
> 
> System.out.println(s.format(new Date());
> ```
>
> 

### DateTimeFormatter类

不仅可以将日期、时间对象格式化为字符串，也可以将发出解析成日期、时间

获取DateTimeFormatter的三种方式：

1.静态常量

2.不同风格的枚举值

3.根据模式字符串创建

完成日期格式化

> ```java
> //1.常量创建实例
> 
> DateTimeFormatter d= DateTimeFormatter.ISO_DATE_TIME;
> 
> d.format(date);
> 
> //2.medium风格
> 
> DateTimeFormatter d = DateTimeFormatter.ofLocalizedDateTime(FormatStyle.MEDIUM);
> 
> d.format(date);
> 
> //3.根据模式字符串
> 
> DateTimeFormatter d= DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
> 
> d.format(date);
> ```
>
> 

解析字符串

> ```java
> String  s= "2018-01-27 12:27:37";
> 
> //定义格式器：
> 
> DateTimeFormatter f = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
> 
> //使用LocalDateTime的parse()方法解析
> 
> LocalDateTime l = LocalDateTime.parse(s,f);
> 
> System.out.println(l);
> ```
>
> 

# 六、集合

## 集合概述

集合可存储任意类型的对象，并且长度可变

按存储结构可分为两大类：

单列集合Connection集合和双列集合Map集合

集合体系

| Connection                         | Map                    |
| ---------------------------------- | ---------------------- |
| Lists(ArrayList.LinkedList.Vector) | TreeMap                |
| Set(HashSet.TreeSet)               | Hashtable:Properties   |
| ((HashSet:LinkedHashSet)           | HashMap(LinkedHashMap) |



## Connection接口

Connection是所有单列集合根接口，定义的方法可用于所有单列集合

​	add()-----添加单个元素

​	addAll()-----添加集合中的全部元素

​	clear()----请客元素

​	remove()----删除指定元素

​	removeAll()-----删除指定集合中的所有元素

​	isEmpty()---判断集合是否为空

​	contains()-----判断集合是否包含某喝元素

​	containsAll()----判断集合是否包含指定集合的所有元素

​	iterator()-----返回迭代器，用于遍历集合

​	size()	-----获取集合大小	

## List接口

### List简介

​	List接口是Connection接口的分支，习惯将实现了List接口的集合称为List集合

List集合是以线性方式进行存储，允许出现重复的元素，可以通过索引进行访问，所以元素是有序的

​	add(index,elment)----在索引处添加元素

​	addAll(index,element)------在索引处添加某个集合的所有元素

​	get(index)-------获取指定索引的元素

​	remove(index)-----删除指定索引的元素

​	set(index,element)-----修改指定索引处元素，并返回元素

​	indexOf(element)-----获取指定元素的索引

​	lastIndexOf()-----获取最后一次出现的索引

### ArrayList接口

ArrayList接口封装长度可变的数组对象，可以看成是长度可变的数组

因为是数组结构，所以不适合做增删操作，但是可以通过索引来获取元素，遍历和查找的效率很高

> ```java
> import java.util.ArrayList
> 
> ArrayList list =new ArrayList();
> ```
>
> 

### LinkedList接口

LinkedList是一个双向循环的链表结构，有两个Node类型first和last属性指向元素的前一个元素和后一个元素

正因如此，LinkedList在增删操作效率很高，弥补了ArrayList接口的不足

​	offer()----尾部追加元素

​	push()------头部插入元素

​	remoFirst()-----删除头部元素

​	pollLast()------删除尾部元素

## Connection集合遍历

### Iterator遍历集合

Iterator是Connection集合的一员，主要用于迭代访问（即遍历）Connection集合在的元素

一次Iterator集合对象也被称为迭代器



> ```java
> import java.util.Iterator
> 
> import java.util.ArrayList
> 
> //获取Iterator对象
> 
> ArrayList list =new ArrayList();
> 
> Iterator it=list.iterator();
> 
> //判断集合中是否存在下一个元素
> 
> 	while(it.hasNext()){
> 
> 		Object obj = it.next();//取出ArrayList集合中的元素并输出
> 
> 		System.out.println(obj);
> 
> }
> ```
>
> 

Iterator 迭代器采用指针来访问集合元素，在索引指向第一个位置前，不指向任何元素，直到使用next方法，才指向第一个元素

### foreach遍历集合

foreach是一一种循环遍历，采用的更加简洁的for循环

> ```java
> for(容器中元素类型 临时变量：容器变量){
> 
> //执行语句
> 
> }
> 
> import java.util.ArrayList
> 
> ArrayList list =new ArrayList();
> 
> 	for(Object obj:list){
> 
> 		System.out.println(obj);
> 
> }
> ```
>
> 

foeach不用获取容器长度，也不需要通过索引来访问元素，但是会自动遍历容器中索引元素

所以只能访问元素，不能修改

### JDK8的forEach遍历集合

JDK8中增加了Lambda表达式迭代一个forEach（action）方法来遍历集合，该方法所需要的是一个函数式接口

> ```java
> import java.util.ArrayList
> 
> ArrayList list =new ArrayList();
> 
> //使用JDK8的forEach遍历集合
> 
> List.forEach(obj->System.out.print("迭代器集合元素:"+obj))
> ```
>
> 

JDK8的forEach在执行时，会自动遍历集合每个元素，并且将将元素逐个传递给Lambda表达式的形参

JDK8同样给Iterator迭代器对象提供了一个forEachRemaining()方法来遍历集合，该方法同样需要一个函数式接口

> ```java
> import java.util.Iterator
> 
> import java.util.ArrayList
> 
> //获取Iterator对象
> 
> ArrayList list =new ArrayList();
> 
> Iterator it=list.iterator();
> 
> //使用JDK8增加的orEachRemaining()方法来遍历迭代器对象
> 
> It.orEachRemaining(obj->System.out.print("迭代器集合元素:"+obj));
> ```
>
> 

## Set接口

### Set接口简介

同样作为Connection接口的子接口，与List接口不同的是，Set接口元素无序，且不会重复

Set主要有两个实现类:

​	HashSet+TreeSet

### HashSet集合

通过对象哈哈希值来确定元素在集合中的存储位置，具有良好的存储和查找性能

因为HashSet元素无序且不可重复

当添加一个元素时，会先调用该元素的hashCode()方法来确定元素的存储位置，然后再调用equals()方法来确定是否有重复元素

> ```java
> HashSet h=new HashSet();
> 
> s.forEach(o->System.out.println(o));
> ```
>
> 

### TreeSet集合

要保持存入TreeSet集合的元素都是同一种数据类型

是通过二叉树的方式来存储元素，可以实现元素的排序,左边 的元素总小于右边的元素

​	first()-----获取首元素

​	last()----后去尾元素

​	floor()---获取不超过某个元素的最大元素

​	higher()----获取大于某个元素的最小元素

TreeSet排序：

1. 自然排序

   自然排序要求向TreeSet集合存储的元素所在类必须实现Compareable接口并重写compareTo()方法，然后TreeSet集合就会对该类型元素使用compareTo()方法排序，并默认为升序

   > ```java
   > import java.util.TreeSet
   > 
   > //实现Compareable接口
   > 
   > class	T implements Compareable
   > 
   > ...
   > 
   > //重写Compareable的compareTo()方法
   > 
   > public int compareTo(Object obj){
   > 
   > T s = (T) obj;
   > 
   > }
   > 
   > ...
   > 
   > TreeSet ts= new TreeSet();
   > 
   > ts.add(new T("wuhan",20));
   > ```
   >
   > ​	

2. 定制排序	

   即自定义比较器来进行排序

## Map接口

### Map接口简介

Map是通过键(key)值(value)对的映射关系存储数据的，key不允许不允许重复，但是value可以重复

### HashMap集合

HashMap是Map的一个实现类，键和值允许为空，但不允许重复

HashMap底层是哈希表结构存储，所以增删查改效率都很高

哈希表结构中，水平方向数组的长度称为HashMap集合的容量（capacity默认为16）

竖直方向每个元素对于的链表结构称为一个桶，每个桶的位置在集合中都有对应的桶值，用于快速定位集合元素添加、查找时的位置

>```java
>import java.util.HashMap
>
>HashMap h =new HashMap();
>
>h.put("name","wuhan");//添加元素
>
>h.containKey("name");//判断是否有某个元素
>
>h.keySet();//获取键对象集合
>
>h.valueSet();//获取值对象集合
>
>replace("name","zhaoxin");//替换元素
>
>h.remove("name");//删除元素
>```
>
>

### Map集合遍历

#### Iterator迭代器遍历

​	先要讲Map集合转换为Iterator集合对象，然后进行遍历

因为Map集合有键和值两个属性，所以有两个方法转换对象：

keySet(). entrySet()

> ```java
> //keySet()
> 
> //Map--Set-Iterator-遍历键-根据键获取值
> 
> Map m =new HashMap();
> 
> Set keyset = m.keySet();
> 
> Iterator it = keyset.iterator();
> 
> while(it.hasNext()){
> 
> 		Object key = it.next();
> 
> 		Object value = m.get(key);
> 
> 		System.out.println(key+":"value);
> 
> }
> ```
>
> 

---

> ```java
> //entryKey()
> 
> Map m =new HashMap();
> 
> Set en = m.entryKey();
> 
> Iterator it = entrySet.iterator();//获取对象
> 
> while(it.hasNext()){
> 
> 	Map.Entry en = (Map.Entry)(it.next());/获取集合映射关系
> 
> 	Object key = en.getKey();	//获取键
> 
> 	Object value=en.getValue();//获取值
> 
> 		System.out.println(key+":"value);
> 
> }	
> ```
>
> 

#### forEach(acton)遍历

该方法的参数也是一个函数式接口

> ```java
> m.forEach((key.value)->System.out.println(key+":"+value))
> ```
>
> 

会自动遍历集合的键和值，并将结果返回给参数列表

### TreeMap集合

通过二叉树的原理保证键值的唯一性	

> ```java
> Map m = new TreeMap();
> ```
>
> 

也可以通过自定义比较器进行自定义排序

> ```java
> class A implements Comparator{
> 
> }
> 
> Map m = new TreeMap(new A);
> ```
>
> 

### Properties集合----Hashtable子类

Map还要一个实现类Hashtable，它的线程数安全的但是效率很低

Properties主要存储字符类型的键和值，经常用来存储应用的配置项

## 泛型

指定集合存储的数据类型，限定操作的数据类型

> ```java
> ArrayList<String> list=new ArrayList<String>;
> ```

## 常用工具类

### Connection工具类

添加、排序操作

> ```java
> ArrayList<String> list=new ArrayList<String>;
> 
> Connection.addAll()//添加元素
> 
> Connection.reverse(list)//反转元素
> 
> Connection.sort()//排序
> 
> Connection.swap()//交换
> ```
>
> 

查找、替换操作

​	binarySearcch(list, key)根据二分法查找

​	max()---返回最大值

​	min---返回最小值

### Array工具类

> ```java
> int [] arr = {1,2,3,};
> 
> printArray(arr)-----打印数组
> 
> Arrays.sort(arr)----排序
> 
> binarySearch(arr,3)---查找指定元素
> 
> Arrays.copyofRange(arr,1,7)----拷贝指定范围数组
> 
> Array.fill(arr,8)-----替换元素
> ```
>
> 

## 聚合操作

### 聚合操作简介

新增的Stream接口，可以把集合、数组的元素转换为Stream流(串形流)的形式，并结合Lambda表达式，进一步简化增删查改的操作

分为3步：

1.将原集合或数组对象转化为Stream对象

2.对流对象进行一系列的过滤、查找等中间操作，返回一个流对象

3.对流进行遍历、统计、收集等终结操作，获取想要的结果

#### 创建流对象

有三个方法：

> ```java
> Integer [] arr = {1,2,3};
> 
> //将数组转换为List集合
> 
> List<Integer> list= Arrays.asList(arr);
> 
> //1.使用集合对象的stream()静态方法创建流
> 
> Stream<Integer> stream =list.stream();
> 
> //2.使用集合接口of静态方法
> 
> Stream<String> stream2=Stream.of(arr);
> 
> //3.使用Arrays数组工具类的静态方法
> 
> Stream<String> stream3 = Arrays.steam(arr);
> ```
>
> 

#### Stream流常用方法

##### 遍历

​	stream.forEach(Lambda)

##### 过滤

​	stream.filter(Lambda)过滤

##### 映射

​	stream.map(Lambda)

##### 截取

​	stream.skip()跳过

​	stream.limit()截取

##### 收集

​	map.collect()

### 并行流（Parallel Stream)

所谓并行流，就是将员数据分成多个子流对象进行多线程操作，再将处理的结果汇聚为一个流对象

第一种创建方式：

​	Connection集合的parallelStream()方法直接转换

> ```java
> Stream<String> p = list.parallelStream();
> ```
>
> 

第二种创建方式：	

​	BaseStream接口的parallel()方法，还要isParallel()方法，判断是不是并行流

> ```java
> Stream<String> b = stream.parallel();
> ```

# 七、I/O流

## I/O流概述

在Java中，将不同输入输出设备之间的数据传输抽象表述为“流”

I/O流：即输入输出流，可以实现数据的输入输出

按不同的分类方式，分为三类：

1.字节流和字符流

2.输入流和输出流

3.节点流和处理流

I/O流顶级流的分类：

I/O流

| 字节流                 | 字符流            |
| ---------------------- | ----------------- |
| 字节输入  InputStream  | 字符输入流Reader  |
| 字节输出. OutputStream | 字符输出流 Writer |

## 字节流

### 字节流概述

所谓字节流，即对字节的输入输出

所有字节流输入都继承自 InputStream

​	read() close()

所有自己流输出都继承自  OutputStream

​	write() close() flush()刷新

I/O流的输入输出，都是相对程序而言的

在I/O结束后，应该调用close()方法关闭流，释放资源

### 字节流读写文件

读写文件的类:

FileInputStream.    FileOutputStream.都是InputStream的子类

读文件删重复的，需要循环：

> ```Java
> FileInputStream in = new FileInputStream("text.txt");
> 
> int b=0;
> 
> while(b=in.read()!=0){//循环读取文件，当返回-1时结束
> 
> 	System.out.println(b);
> 
> }
> 
> in.close();//关闭流
> ```
>
> 

写文件同样需要循环

> ```Java
> FileOutputStream out = new FileOutputStream("out.txt");
> 
> String s = "hello";
> 
> out.write(s.getBytes());//将字符串转换为字节数组进行写入
> 
> out.close();
> ```
>
> 

而为了逼main异常终止程序运行，抛出异常：

> ```Java
> finally{
> 
> try{
> 
> 	if(in!=null)
> 
> 		in.close();
> 
> }catch(Exception e){
> 
> 	e.printStackTrace();
> 
> }
> 
> try{
> 
> 	if(out!=null)
> 
> 		out.close();
> 
> }catch(Exception e){
> 
> 	e.printStackTrace();
> 
> }
> 
> }
> ```
>
> 

### 文件的拷贝

> ```Java
> FileInputStream in = new FileInputStream("text.txt");
> 
> FileOutputStream out = new FileOutputStream("out.txt");
> 
> int len=0;
> 
> //跳过循环将读取到的文件字节信息写入到写文件
> 
> while((len = in.read())!=-1){
> 
> ​	out.write(len);
> 
> }
> 
> in.close();
> 
> out.close();
> ```
>
> 

### 字节流的缓冲区

定义一个字符数组作为缓冲区，提高传输效率，即一次传输大量的字节流

> ```Java
> FileInputStream in = new FileInputStream("text.txt");
> 
> FileOutputStream out = new FileOutputStream("out.txt");
> 
> int len=0;
> 
> //定义一个长度为1024的字节数组
> 
> byte [] buffer =new byte[1024];
> 
> //跳过循环将读取到的文件字节信息写入到写文件
> 
> while((len = in.read(buffer))!=-1){
> 
> 	out.write(buffer,0len);
> 
> }
> 
> in.close();
> 
> out.close();
> ```
>
> 

使用缓冲区减少对文件的操作次数，提高效率

### 字节缓冲流

I/O包中有两个带缓冲带字节流：BufferedInputStream.   BufferedOutputStream，在它们的构造方法中分别接受InputStream、OutputStream类型大参数作为对象

应用程序通过缓冲流来读写数据，而缓冲流又通过底层的字节流与设备进行关联

源设备--字节流--缓冲流--应用程序--缓冲流--字节流--目标设备

> ```Java
> BufferedIonputStream bis=new BufferedIonputStream(new FileInputStream("test.txt"));
> 
> BufferedOutputStream bos = new BufferedOutputStream(new FileOutputStream(do.txt));
> 
> int len = 0;
> 
> while(bis.read()!=-1){
> 
> 	bos.write(len);
> 
> }
> 
> bis.close();
> 
> bos.close();
> ```
>
> 



## 字符流

### 字符流概述

用于操作字符

Reader()用于读取字符，Writer()用于写入字符。这两个类都是字符流顶级类，其他类都是它们的子类

### 字符流操作文件

操作做文件又FileReader()和FileWriter()类

> ```Java
> //读取文件：
> 
> FileReader() r =new FileReader();
> 
> Int len= o;
> 
> while(len=r.read()!=-1){
> 
> 	System.out.println((char(len)))
> 
> }
> 
> r.close();
> 
> //写文件:
> 
> FileWriter f = new FileWriter();
> 
> f.write("wuhan;\r\n");
> 
> f.write("zhaoxin;\r\n");
> ```
>
> 

写文件是，如果文件不存在，则会创建文件；如果文件存在，则会覆盖文件

当然还有字节缓冲区:

> ```Java
> //读取文件：
> 
> FileReader() r =new FileReader();
> 
> Int len= o;
> 
> char [] buff = new char[1024];
> 
> while(len=r.read(buffer)!=-1){
> 
> 	System.out.println((char(len)))
> 
> }
> 
> r.close();
> 
> //写文件:
> 
> FileWriter f = new FileWriter();
> 
> f.write("wuhan;\r\n");
> 
> f.write("zhaoxin;\r\n");
> ```
>
> 

字节缓冲流：

> ```Java
> BufferedReader br=new BufferReader(new FileReader('reader.txt'));
> 
> BufferedWriter bw=new BufferedWrite(new FileWriter("writer.txt"));
> 
> String s =null;
> 
> while(s =br.readLine()!=-null){//readLine()一次读取一行文本
> 
> 	bw.write(s);
> 
> 	bw.newLine();//写入换行符
> 
> }
> 
> br.close();
> 
> bw.close();
> ```
>
> 

### 转换类

将字节流转换为字符流：

InputStreamReader.OutputStreamWriter分别是Reader,Writer的子类

> ```Java
> FileInputStream in = new FileInputStream("text.txt");
> 
> //转换成字符输入对象
> 
> InputStreamReader sir = new InputStreamReader(in);
> ```
>
> 

## File类

该类封装了一个路径，并提供了一系列的方法用于操作改路径指向的文件

### File类常用方法

​	getpath()---获取相对路径

​	getAbsolutePath()----获取绝对路径

​	getParent()------获取父路径

​	canRead()----能读？

​	canWrite()----能写？

​	length()-----获取长度

### 遍历目录下文件

​	list()方法遍历目录下文件

### 删除文件以及目录

​	delete()方法删除目录文件，使用之前先要判断是否存在文件

## RandomAccessFile类

RandomAccessFile不时流，可以从文件的任意位置开始执行读写数据的操作

有指针来标识当前读写位置，seek()可以使指针向前向后移动，getFilePointer()获取文件当前记录指针的位置

> ```Java
> //创建RandomAccessFile对象，包并1⃣️读写模式打开文件：
> 
> RandomAccessFile raf = new RandomAccessFile("text.txt","rw);
> ```
>
> 

## 对象序列化

用来将对象上的数据保存到磁盘上

对象序列化是将一个对象转换成一个I/O流中字节序列的过程

将个I/O流中字节序列恢复为Java对象的过程，称为反序列化

可序列化的类必须实现以下两个接口之一：

​	Serializable    Externlizable(性能较好)

## NIO

### NIO概述

即new I/O，增入了新功能

采用内存映射文件的方式来处理输入输出，将文件映射到内存中，可以像访问内存一样访问文件

在标准I/O中，使用字节流和字符流，而NIO使用的是Buffer和Channel，数据从通道读入缓冲区，或从缓冲区写入通道

Buffer ->写入>Channel

Buffer --读入>--Channel

### Buffer(缓冲区)

子类没有构造方法，不能通过构造方法来创建对象

通常使用子类的XXXBuffered allocate(int capacity)方法来实现对象的创建

> CharBuffer buffer= CharBuffer.allocate(6)

put()写入数据

get()获取数据

capacity()容量：

​	Buffer最大数据容量

limit()界限：

​	表述不可被读取的一个位置的索引

position()位置：

​	指定下一个可被读取的缓冲区的索引

### Channel(通道)

Channel是一个接口对象，类似于流

可双向读写

只能与Buffer进行交互，不能直接读写Buffer中的数据

Channel也不是通过构造方法获取，而是通过传统的getChannel()方法

## NIO.2

新的NIO,最大大改进就是提供了全面的文件输入输出以及文件系统的访问与支持

以及异步Channel的输入输出

### Path接口

也在文件系统中定位文件的对象，通常表示为一个依赖系统的文件路径

还有Paths和Files工具类，其中Paths中两个静态方法可以创建Path对象，而Files提供了大量操作文件的静态方法

> ```Java
> //创建对象
> 
> Path path= Paths.get("文件路径");
> 
> path.getRoot()-----获取根路径
> 
> path.getParent()---获取父路径
> 
> path.getName()---获取路径名称
> ```
>
> 

### Files工具类

> ```Java
> //创建多集目录
> 
> Files.creatDirectories(name);
> 
> //创建文件
> 
> Files.createFile();
> ```
>
> 

# 八、GUI(图形用户接口)

GUI即用户图形接口，用来给用户提供操作界面的接口

基本图形用户接口开发工具：AWT，Swing，JavaFX

## Swing概述

AWT是重量级组件，很麻烦，逐渐被Swing替代

Swing以底层AWT为基础而开发

Swing所有类都继承自Container类

## Swing顶级容器

### JFrame

是一个独立存在的顶级容器，不能放置在其他容器中，支持窗口的所有基本功能



> ```Java
> //创建并设置JFrame窗口
> 
> JFrame j =new JFrame("JFrameTest");
> 
> //设置关闭窗口时的操作
> 
> f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
> 
> //设置窗口尺寸
> 
> f.setSize(250,150);
> 
> //设置展示窗口
> 
> f.setVisible(true);
> ```
>
> 
>

### JDialog

JDialog表示对话框窗口，分为模态对话框和非模态对话框

模态对话框和非模态对话框的设置，可以在创建JDialog对象时为构造方法传入参数来设置，也可以调用setModal()方法来设置

 在JFrame基础上：

> ```Java
> //创建并设置JFrame窗口
> 
> JFrame j =new JFrame("JFrameTest");
> 
> //设置关闭窗口时的操作
> 
> f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
> 
> //设置窗口尺寸
> 
> f.setSize(250,150);
> 
> //设置展示窗口
> 
> f.setVisible(true);
> 
> //创建JDialog
> 
> JDialog j = new JDialog(f,"JDialogtest",true);
> 
> j.setDefaultCloseOperation(JDialog.EXIT_ON_CLOSE);
> 
> j.setSize(100,200);
> 
> j.setVIsible(true);
> ```
>
> 

## 布局管理器

Swing组件不能单独存在，必须放在容器之中

而组件在容器中的位置和大小是有布局管理器来设置的

### BorderLaout边界管理器

BorderLaout将容器分为五个部分：页头(PAGE_START)、页尾(PAGE_END)、行首(LINE_START)、行尾(LINE_END)、中间(CENTER)

添加组件时，用add(component,area);指定组件类型和位置

> ```Java
> //创建一个名为BorderLaou的顶级窗口容器
> 
> JFrame. f =new JFrame("BorderLaout");
> 
> //设置窗体的布局管理器为BorderLaout
> 
> f.setLayout(new BorderLaout());
> 
> //设置窗口尺寸
> 
> f.setSize(250,150);
> 
> //添加按钮组件：
> 
> JButton bt1= new JButton("PAGE_START");
> 
> JButton bt2=new JButton("PAGE_END");
> 
> JButton bt3 =new JButton("LINE_START");
> 
> JButton bt4=new JButton("LINE_END");
> 
> JButton bt5=new JButton("CENTER");
> 
> //将按钮添加到窗体中
> 
> f.add(bt1,BorderLaout.PAGE_START);
> 
> f.add(bt2,BorderLaout.PAGE_END);
> 
> f.add(bt3,BorderLaout.LINE_START);
> 
> f.add(bt4,BorderLaout.LINE_END);
> 
> f.add(bt5,BorderLaout.CENTER);
> 
> //设置窗体可见，设置展示窗口
> 
> f.setVisible(true);
> 
> f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
> ```
>
> 

### FlowLayout流式布局管理器

即从左向右放置，当到边界时，会自动将组件放到下一行的开始位置

组件有三种对齐方式（右对齐FlowLayout.RIGHT，左对齐FlowLayout.LEFT，居中对齐FlowLayout.CENTER），默认为居中对齐

构造方法：

FlowLayout(align,sgap,vgap)

aligin：决定对齐方式

sgap：设置水平间距

vgap：设置垂直间距

> ```Java
> //创建一个名为FlowLayout的顶级窗口容器
> 
> JFrame. f =new JFrame("FlowLayout");
> 
> //设置窗体的布局管理器为FlowLayout
> 
> f.setLayout(new FlowLayout(FlowLayout.LEFT,20,30));
> 
> //设置窗体可见，设置展示窗口
> 
> f.setVisible(true);
> 
> f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
> ```
>
> 

### GirdLayout网格布局管理器

GirdLayout将容器分为n行m列大小相等的网格每个网格可添加一个组件，从上到下，每一行从左到右依次放值组件

特点是相对位置不随区域的缩放而改变，但组件大小会改变，组件始终占满整个区域

构造方法：

GirdLayout(rows, lines,sgap,vgap)

row指定行数

line指定列数

sgap水平间距

bgap垂直间距

> ```Java
> //创建一个名为GirdLayout的顶级窗口容器
> 
> JFrame. f =new JFrame("GirdLayout");
> 
> //设置窗体的布局管理器为GirdLayout
> 
> f.setLayout(new GirdLayout(3,3));
> 
> f.setSize(300,400);
> 
> f.Location(300,400);
> 
> //循环添加按钮
> 
> for(int i=1;i<=8;i++){
> 
> Button btn=new Button("btn"+i);
> 
> f.add(btn);
> 
> }
> 
> //设置窗体可见，设置展示窗口
> 
> f.setVisible(true);
> 
> f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
> ```
>
> 

## 事件处理

### 事件处理机制

涉及三类对象：

事件源（Event Source)

事件对象(Event)

监听器(Listener)

实现Swing时间处理的主要步骤：

1.创建事件源

2.自定义监听器-----必须实现xxxLintener接口

3.为事件源组册监听器-----使用xxxLintener方法

> ```Java
> //自定义事件监听器类
> 
> class Mylistened implements Actionlistener{
> 
> //实现监听器方法，对监听器事件进行处理
> 
> Public void action(ActionEvent e){
> 
> .....
> 
> }
> 
> }
> 
> JFrame. f =new JFrame("GirdLayout");
> 
> //创建按钮，作为事件源
> 
> JButon btn = new JButon("按钮");
> 
> //为按钮事件添加自定义监听器
> 
> btn.addActionLintener(new MyListener());
> ```
>
> 

### Swing常用事件处理

#### 窗体事件

​	Java提供了一个WindowEvent类用于窗体事件

对窗体事件进行处理时，首先要定义一个实现了WindoListener接口的类作为窗体监听器

然后通过addWindowListener()方法将窗体对象与窗体监听器进行绑定

> ```Java
> //内部类实现创建窗体事件实例
> 
> f.addWindowListener(new WindowListener(){
> 
> })
> ```
>
> 

#### 鼠标事件

 Java提供了MouseEvent类表示鼠标事件

处理鼠标事件需要通过实现MouseListener()接口实现监听器，也可以通过适配器MouseAdapter类来实现

然后调用addMouseListener()方法将监听器绑定到事件源对象

> ```Java
> //为按钮添加事件源对象
> 
> btn.addMouseLintener(new MouseListener(){
> 
> })
> ```
>
> 

#### 键盘事件

Java中提供了KeyEvent表示鼠标事件

需要实现，KeyListener接口，或继承KeyAdapter类，然后调用addKeyListener()方法将监听器绑定到事件源对象

> ```Java
> f.addKeyListener(new KeyListener{
> 
> })
> ```

#### 动作事件

用ActionEvent类表示

需要实现ActionListener接口

## Swing常用组件

组件也不能单独存在，只能放在顶级容器中

### 面板组件

#### JPanel

无边框，不能放缩不能移动

可以用setLayout()为其设置布局管理器，但是默认为流式管理器

#### JScrollPane

JScrollPane带滚动条的面板容器，只能添加一个组件

> ```Java
> setHorizontalBarPolicy()----指定水平滚动条策略
> 
> setVerticalBarPolicy()------指定垂直滚动条策略
> 
> setViewportView()-------设置在滚动面板显示的组件
> ```
>
> 

### 文本组件

都继承自JTextCompoment

#### JTextField文本框

只能输入单行

> ```Java
> JTextField(text, column)//指定列数，并显示初始字符串
> ```

#### JTextArea文本域

可以输入多行

> ```Java
> JTextArea(text, row,column)//显示初始字符串并且指定了行和列
> ```

### 标签组件

#### JLable

显示文本、图像，还可以设置垂直和水平的对齐方式

> ```Java
> JLable(text,icon,horizon);//指定文本、图像和水平对齐方式
> ```

### 按钮组件

都是抽象类AbstractButton类的子类

#### JButton

#### JCheckBox复选框

> ```Java
> JCheckBox(text, selected);//指定文本信息，指定初始状态
> ```

#### JRadioButton单选框

将多个JRadioButton按钮添加到同一个单选按钮中就能实现JRadioButton按钮的单选功能

> ```Java
> JRadioButton(text, selected);
> ```

### 下拉框组件JComBox

> ```Java
> addItem();//添加选项
> ```

### 菜单组件

#### 下拉式菜单

需要三个组件

JMenuBar(菜单栏)

​	使用顶级容器的setJMenuBar()设置在顶部

JMEenu(菜单)

​	使用JMEenu(text)构造函数创建JMEenu菜单

JMenuItem(菜单项)

​	使用JMenuItem(text为菜单项指定内容

#### 弹出式菜单

JPopuoMenu()

默认不可见

## JavaFX图形用户工具

### JavaFX概述

和Swing一样，也可以创建图形用户接口，但是更加强大

可以和Swing交互操作

# 九、JDBC

## 什么是JDBC

一套可以执行SQL语句的API

应用程序通过JDBC来和数据库进行交互，提高了效率

JDBC通过不同的数据库驱动来与其对应的数据库进行连接，连接后就可饮执行操作

## JDBC常用API

JDBC的API主要位于java.sql包中

在包内定义一系列访问数据库的接口和类

### Drive接口

是所有JDBC必须实现的接口，该接口专门通过给数据库厂商使用

### DriveManager类

DriveManager用于加载驱动并创建与数据库的连接

在加载数据库驱动时，常用Class类的静态方法forName()实现

### Connecion接口

Connecion接口代表Java程序和数据库的连接对象

之一获得连接对象后，才能访问数据库，操作数据库

### Statement接口

Statement接口是执行数据库操作的重要接口

用于执行静态的SQL语句，并返回一个对象

### PreparedStatement接口

PreparedStatement接口是Statement接口的子接口，解决了安全问题

用于执行预编译的SQL语句

### ResultSet接口

ResultSet接口用于保存JDBC执行查询是返回的结果，该结果封装在一个逻辑表中

在ResultSet接口内部有一个游标（指针）

在ResultSet对象初始化时，游标在表格的第一行前，调用next()方法可将游标移动道下一行

## JDBC编程

### 1.加载数据库驱动

使用Class类的静态方法forName()

>```Java
>Class.forName("DriverName");
>```

其中，DriverName是数据库驱动类所对应的字符串

加载的并不是真正使用的数据库的驱动类，而是数据库驱动类名的字符串

> ```Java
> //比如驱动MySQL数据库的驱动就可以使用
> 
> Class.forName("com.mysql.jdbc.Driver")
> 
> //加载Oracle数据库驱动：
> 
> Class.forName("oracle.jdbc.driver.OracleDriver")
> ```
>
> 
>

### 2.通过DriveManager类获取数据库连接

DriveManager提供了一个getConnection()方法来获取数据库连接：

> ```Java
> Connection conn = DriveManage.getConnection(url, user,pwd)
> 
> 要接收三个参数，分别是连接数据库的URL、用户名和密码
> 
> URL格式：以MySQL为例：
> 
> 	jdbc:mysql://hostname:port/datebasename
> 
> hostname是主机名，如果连接本机的数据库，可以写127.0.0.1,
> 
> 如果是其他主机，这要写IP地址
> 
> port是连接数据库的端口号，MySQL默认端口是3306
> 
> datebasename是数据库名称
> ```
>
> 

### 3.通过Connection对象获取Statement对象

Connection创建Statements有三种方式：

1. creatStatement():

   ​	创建基本的Statement对象

2. prepareStatement(sql)

   根据传递的SQL语句创刊PreparedStatement对象

3. prepareCall(sql)

    根据传入的SQL语句创建CallStatement对象

比如：

> ```Java
> Statement stm = conn.createStatement();
> ```

### 4.使用Statement执行SQL语句

所有的Statement执行SQL语句都有三种方法：

 1. execute(sql):

    用于执行任意的SQL语句

 2. executeQuery(sql):

    用于执行查询语句，返回一个ResultSet结果集对象

 3. executeUpdate(sql):

    用于操作DDL和DML语句

比如

> ```Java
> 执行SQL，获取结果集ResultSet
> 
> ResultSet rs = stm.execute(sql)
> ```

### 5.操作ResultSet结果集

如果执行的是查询语句，执行结果会返回一个ResultSet对象

该对象里保存了SQL语句查询的结果、

程序可以通过该ResultSet对象取出查询结果

### 6.关闭连接，释放资源

关闭顺序和打开顺序相反

顺序是ResultSet、  Statement(PreparedStatement)和Connection

为保证发生异常也能进行关闭

可在try....catch的finnaly中统一关闭  

## 第一个JDBC程序

(1)搭建数据库环境

MySQL数据中中创建名为jdbcd的数据库，在数据库中创建一个表tb_user:

> ```sql
> CREATE DATABASE jdbc;
> 
> USE jbbc;
> 
> CREATE TABLE tb_user(
> 
> 	id INT PRIMARY KEY AUTO_INCREMNET;
> 
> 	NAME VARCHAR(40);
> 
> 	sex VARCHAR(60);
> 
> 	email VARCHAR(60);
> 
> 	birthday DATE
> 
> )
> ```
>
> 

在插入三条数据:

> ```sql
> INSERT INTO tb_user(NAME,sex,email,birthday)
> 
> 	VALUES('jack','男','jack@126.com','1980-01-04');
> 
> 		('wuhan','男','wuhan@126.com','2001-05-05);
> 
> 		('zhaoxin','女','zhaoxin@126.com','2001-06-06');
> ```
>
> 

(2)编写数据库程序

> ```java
> Connection conn = null;
> 
> Statment stm =null;
> 
> ResultSet  rs = null;
> 
> try{
> 
> 	//1.加载数据库驱动
> 
> 	Class.forName("com.mysql.jdbc.Driver");
> 
> 	//2.通过DriverManager获取数据库连接
> 
> 	String url="jdbc:mysql://hostname:3306/jdbc";
> 
> 	String username = "root";
> 
> 	String pwd="root";
> 
> 	conn = DriverManager.getConnection(url, username.pwd);
> 
> 	//3.通过Connection对象换取Statement对象
> 
> 	stm = conn.createStatement();
> 
> 	4.使用Statement执行数据库语句
> 
> 	String sql ="select * from tb_user";
> 
> 	rs = stm.executeQuery(sql);
> 
> 	//5.操作ResultSet结果集
> 
> 	System.out.println("id		|	name	sex"+"	|	email	|	birthday");	
> 
> 	while(rs.next()){
> 
> 		int id = rs.getInt("id");
> 
> 		Stringa name = rs.getString("name");
> 
> 		String sex  = rs.getString("sex");
> 
> 		String email = rs.getString("email");
> 
> 		String birthday = rs.getDate("birthday");
> 
> 		System.out.println("id		|	name	sex"+"	|	email	|	birthday");		
> 
> }
> 
> }catch(Exception e){
> 
> e.printStcakTrace();
> 
> }finally{
> 
> 	6.关闭连接，释放资源
> 
> 	if(rs!=null){rs.close();}
> 
> 	if(stm!=null){stm.close();}
> 
> 	if(conn!=null){conn.close()}
> 
> }
> ```
>
> 

# 十、多线程

## 线程概述

### 进程

​	每个独立运行的程序为一个进程

cpu很快，能在几个进程之间快速切换，是的好像是几个进程同时进行一样

### 线程

​	一个进程有很多个执行单元来共同执行程序

这些细分的执行单元称为线程

在Java程序启动时，便会产生一个进程

该进程默认会产生一个线程

这个线程会运行main()方法中的代码

## 线程创建

### 1.Thread类实现多线程

Thread类是java,lang下的一个线程类，用来实现多线程

通过继承Thread类来实现多线程步骤：

(1)创建一个Thread类线程的子类，同时重写Thread类类的run()方法

(2)创建该子类的实例对象，并通过start()方法启动线程

> ```java
> //1.定义一个继承Thread类的子类
> 
> class MyThread extends Thread类{
> 
> 	//创建子类线程有参构造方法
> 
> 	public MyThread(String name){
> 
> 	super(name);
> 
> }
> 
> 	//2.重写Thread类run()方法
> 
> 	public void run(){
> 
> 	int i = 0;
> 
> 	while(i++<5){
> 
> 		System.out.println(Thread.currentThread().getName()+"还在运行");
> 
> }
> 
> }
> 
> }
> 
> //创建实例对象
> 
> MyThread thread1 = new MyThread("thread1");
> 
> //调用启动方法
> 
> thread1.start()
> 
> MyThread thread2 = new MyThread("thread2");
> 
> //调用启动方法
> 
> thread2.start()
> ```
>
> 

### 2.Runnable接口实现多线程

​	Thread类实现的多线程，因为已经继承了Thread，无法再继承，存在很大局限性

Runnable是接口，就弥补了这一缺陷

主要步骤如下：

1.创建一个Runnable实现类，并重写run()方法

2.创建Runnable接口的实现类对象

3.使用Thread类的有参构造方法创建实例，并将Runnable接口的实现类的实例对象作为参数传入

4.调用线程实例的start()方法启动线程

> ```java
> 1.//定义一个实现Runnable接口的实现类
> 
> class Mythread2 implements Runnable{
> 
> //2.重写run()方法
> 
> 	public void run(){
> 
> 	int i = 0;
> 
> 	while(i++<5){
> 
> 		System.out.println(Thread.currentThread().getName()+"还在运行");	
> 
> }
> 
> }
> 
> //3.创建Runnable接口的实例对象
> 
> MyThread2 mythread2 =new MyThread2();
> 
> //3.使用Thread(Runnable target,String name)构造方法创建线程实例
> 
> Thread thread1 = new Thread(mythread2,"thread1");
> 
> //4.调用start()方法启动线程
> 
> thread1.start()
> 
> //另一个线程
> 
> Thread thread2 = new Thread(mythread2,"thread2");
> 
> thread2.start()
> ```
>
> 

### 3.Callable接口实现多线程

Callable接口技能创建多线程，又能有返回值

也是通过有参的构造方法传入Runnable接口类型的参数来实现多线程

但是在这里传入的是Runnable接口子类的FutureTask对象作为参数

而FutureTask对象中则封装了Callable接口的返回值

步骤：

1.创建一个Callable接口的实现类，同时重写Callable接口的call()方法

2.创建Callable接口的实现类对象

3.通过FutureTask线程结果处理类的有参构造方法来封装Callable接口实现类对象

4.使用参数为FutureTask类对象的Thread有参数n构造方法创建Thread线程实例

5.调用线程start()方法，启动线程

> ```java
> //1.定义一个Callable接口的实现类
> 
> class Mythread3 implements Callable<Object>{
> 
> //重写run()方法
> 
> 	public Objet call() throws Exception{
> 
> 		nt i = 0;
> 
> 	while(i++<5){
> 
> 		System.out.println(Thread.currentThread().getName()+"还在运行");	
> 
> 
> 
> }
> 
> 	return 1;
> 
> }
> 
> /2.创建Callable接口的实现类对象
> 
> Mythread myThread3 = new Mythread();
> 
> //3.使用FutureTask封装Callable接口
> 
> FutureTask<Object> ft1=new FutureTask<>(mythread3);
> 
> //4.使用Thread(Runnable target,String name)构造方法创建线程实例
> 
> Thread thread1 = new Thread(ft1,"thread1");
> 
> //5.启动线程
> 
> thread1.start();
> 
> //另外一个线程
> 
> FutureTask<Object> ft2=new FutureTask<>(mythread2);
> 
> Thread thread2 = new Thread(ft2,"thread2");
> 
> thread1.start();
> 
> //获取返回值
> 
> System.out.println("ft1.get()");
> 
> System.out.println("ft2.get()");
> ```
>
> 

### 后台线程

前台和后台是相对概念

当一个线程调用了setDaemen(true)方法后，九变成了一个后台线程

当一个程序只有后台线程时就会结束

而setDaemen(true)方法必须在start()之前使用，否则就没有作用

## 线程的生命周期及状态转换

官方将线程生命周期分为6个部分：

NEW--新建状态

​	线程刚创建，但是还不能运行

RUNNABLE--可运行状态

​	调用了start()方法九加入RUNNABLE状态

​	又分为：

​				就绪：等待cpu调度

​				运行状态：获得调度

BLOCKED--阻塞状态

​		失去cpu执行权。只会加入就绪状态

​		两个原因：

​				同步锁被其他线程获取

​				运行时发出I/O请求

WAITING---等待状态

​			当调用了无参数时间限制的方法时就会进入WAITING状态

​			wait()方法导致必须等待notify()或nofifyAll()来唤醒

​			join()方法导致则必须等待其他线程的终止

TIME_WAITING-----定时等待状态

​		运行了有时间限制的参数方法，必须等待时间结束

TERMINATED-----终止状态

​	run() call()方法执行完毕或抛出异常就加入终止

​	生命周期结束

## 线程的调度

有两种调度模型：

分时调度模型和抢占式调度模型

Java默认采用抢占调度模型

### 线程的优先级

和路由一样，可以通过优先级(1-10)来进行调度

优先级越高被cpu调度可能性越大

调用setPriority()来设置

既可以时数字，也可以是Thread类的静态常量

Thread类有三个静态常量：

MAX_PRIORITY			10 优先级最高

MIN_PRIORITY				1

NORM_PRIORITY			5

### 线程睡眠

人为的让正在执行的程序休眠，让那个CPU调度其他线程

使用静态方法sleep(long mills)让线程进入阻塞状态

等待休眠时间结束后，线程才会继续进行

### 线程让步

调用yield()方法，只是让线程加入就绪状态

而优先级不低与该线程的则会被调度

### 线程插队

调用join()方法，让线程进入阻塞，直到其他线程调度完毕

## 多线程同步

### 线程安全

多个线程同时处理共享资源时会出现的错误

### 同步代码块

要解决线程安全问题，就要保证处理共享资源的代码在任意时刻只有一个线程访问

于是Java出现了线程同步机制

即把代码放在synchronized关键字来修饰的代码块中

被称为同步代码块

> ```java
> synchronized(lock){
> 
> }
> ```
>
> 

lock是一个锁对象，是同步代码块的关键

当一个线程执行该代码块是，lock由1变为0

其他线程执行到这段代码时，lock为o，于是被阻塞

直到原线程执行完毕，lock变为1，才让新线程执行

### 同步方法

> [修饰符] synchronized 返回值类型 方法名 [参数]

也是为了解决安全问题

同步方法也有锁，他的锁就是调用该方法的对象

### 同步锁(Lock锁)

Lock锁可以让某个线程在持续获取同步锁失败后返回

不再继续等待

> ```java
> //定义一个锁对象
> 
> private final Lock() lock = new ReentrantLock();
> 
> //开启锁
> 
> lock.lock;
> 
> //关闭锁
> 
> lock.unlock();
> ```
>
> 

### 死锁问题

两个线程都在等待对方的锁，就会让程序停滞

即进入死锁

## 多线程通信

相当于流水线的各个部分需要相互协作

多线程之间也需要通信，来彼此协作

Java在Obect类中引入了	

​	wait()-----让当前线程放弃同步锁，进入等待

​	notify()-----唤醒同步锁上第一个调用wait()的线程

​	notifyAll()----唤醒所有同步锁上调用wait()的线程

这三个方法的调用者都是同步锁对象

## 线程池

用线程池来创建多线程，进一步优化线程管理

### Executor实现线程池管理

通过Executor实现线程池管理主要步骤如下：

1.创建一个实现Runnable接口或Callable接口的实现类

2.创建接口的实现类对象

3.使用Executor线程执行器创建线程池

4.使用Executor线程执行器的submit()方法将接口实现类对象提交到线程池进行管理

5.线程池执行完毕后，调用shutdown()关闭线程池

> ```java
> //1.Callable接口的实现类
> 
> class Mythread4  extends Callable{
> 
> 	//重写call()方法
> 
> 	public voic call() throws Exception{
> 
> 		int i = 0;
> 
> 		while(i++<5){
> 
> 		System.out.println(Thread.currentThread().getName()+"还在运行");	
> 
> 
> 
> }
> 
> return	 i;
> 
> }
> 
> //2.Callable接口的实现类对象
> 
> Mythread4 mythread4 = new Mythread4();
> 
> //3.使用Executor线程执行器创建线程池
> 
> ExecutortoServises excutor = ExecutortoServises .newCachedThreadPool();
> 
> //4.将.Callable接口的实现类对象提交到线程池进行管理
> 
> Future<Object> result1 = executor.submit(mythread4);
> 
> Future<Object> result1 = executor.submit(mythread4);
> 
> //5.关闭线程池
> 
> executor.shutdown();
> 
> //获取执行结果
> 
> System.out.println(result.get(i));
> 
> System.out.println(result.get(i));
> ```
>
> 

### CompletableFuture类实现线程池管理

为改进FutureTask，JDK8提出了CompletableFuture类

该类同时实现了Future接口和CompletionStage接口

简化了异步编程的复杂性。

# 十一、网络编程

## 网络编程基础

### 网络通信协议

主要是TCP/IP协议和UDP协议

TCP/IP协议是一组实现网络互联的通信协议

名称来自于两个重要协议TCP协议和IP协议

基于TCP/IP协议的网络结构分为四层

应用层

传输层

网络层

链路层

### IP地址和端口号

#### IP地址

为了使计算机之间能进行通信，为每台计算机指定一个标示号

用这个标识号来指定接收和发送数据的计算机、

TCP/IP协议协议中，这个标识就是IP地址，唯一标识一台计算机

IP地址采用IPv4，由4个字节大小的二进制数来表示

但通常会写成十进制（0-255）数字键用符号.隔开，分开表示4段数字

如10.0.0.1

随后产生了IPv6，用16个字节表示，扩大了表示范围

分为A B C D E类

还有一个本地回环地址127.0.0.1，指本机地址

#### 端口号

通过IP地址可以连接到指定的计算机

但是要访问计算机中的程序，需要指定端口号

计算机中不同程序数通过端口号区分的

端口号是用两个字节（16位的二进制数）表示，0-65535

用户的平台应用程序需要使用1024以上的端口号，避免被服务占用

### InetAddress

JDK中提供了一个与IP地址相关的InetAddress类，用于封装一个IP地址

​	getByName(host)----获取给的主机的IP地址

​	getLocalHost()------获取本机IP地址

​	getHostName()------获取IP地址的主机名

​	getHostAddress()----获取字符串格式的原始IP地址

> InetAddress ia =InetAddress.getLocalHost();

### UDP与TCP协议

UDP是User Dategram Protocal用户数据报协议

​	是无连接的通信协议，在数据传输数时，数据的发生端和接收端之间不建立逻辑连接

​	所以不能保证数据的完整性

​	视频音频可采用UDP传输

TCP是Transmission Control Protocal传输控制协议

​	是面向连接的通信协议，在数据传输数时，数据的发生端和接收端之间要建立逻辑连接

​	保证了两台计算机之间可靠无差错的数据传输

​	因为要建立连接，必须要指明客户端与服务器端：

​		先由客户端向服务器端发出连接请求，每次连接的创建都需要三次握手

​		1.客户端向服务器端发出连接请求，等待服务器确认

​		2.服务器向客户端返回一个相应，通知客户端收到了连接请求

​		3.客户端再次向服务器发送确认信息，确认连接

所以TCP传输数据比较慢，但是可靠

下载文件必须采用TCP

## UDP通信

### UDP通信简介

UDP时无连接的通信协议。通信过程就类似于用集装箱在码头之间运输一样

引入DategramPacket，该类时实例对象就相当于一个集装箱。用来封装数据

DategramSocket，该类的实例对象就相当于码头，用来发送和接收数据

### DatagramPacket--封装数据

接收端的构造方法只需要接收一个字节数组来存放接收到的数据

而发生端的构造方法则不但要接收存放了发送数据的字节数组，还需要指定发生端IP地址和端口号

### DatagramSocket--创建发生端和接收端对象

构造方法要指定IP地址和端口号

### UDP网络程序

要实现UDP通信，需要创建一个发生端程序和一个接收端程序

在通信时，只有接收端程序先运行，才能避免发生端的数据无法接受

接收端程序

> ```java
> //定义一个端口号位8900的接收端DatagramSocket对象
> 
> DatagramSocket server = new DatagramSocket(8900);
> 
> //定义一个长度为1024字节的字节数组，用于接收数据
> 
> byte [ ] buf = byte [1024];
> 
> //定义一个DatagramPacket封装数据报对象，用于封装接收的数据
> 
> DatagramPacket packet =new DatagramPacket(buf,buf.length);
> 
> while(true){
> 
> 	//等待接收数据包服务，没有接收之前处于阻塞
> 
> 	server.receive(packet);
> 
> //调用DatagramPacket的方法获取接收到的信息，并转换为字符串形式
> 
> 	String s= new String(packet.getData(),0,packet.getLength());
> 
> 	System.out.println(packet.getAddress()+":"+packet.gatPort()+“发送消息"+s);
> 
> }
> ```
>
> 

发生端程序：

> ```java
> //对一个指定端口位3000的发生端DatagramSocket对象
> 
> DatagramSocket client = new DatagramSocket(3000);
> 
> //定义要发生的数据
> 
> String s = "hello world";
> 
> //定义一个DatagramPacket数据报对象，封装发生端信息以及发送数据
> 
> DatagramPacket packet = new DatagramPacket(s.getBytes(),s.getBytes().lengtg(),
> 
> 																					InetAddress.getByName("localhost"),8900);
> 
> //发送数据
> 
> client.send(packet);
> 
> //释放资源
> 
> client.close()
> ```
>
> 

## TCP通信

### TCP通信简介

和UDP的一个主要区别是，TCP是严格区服务器和客户端的

在通信时，必须客户端先去连接服务器才能实现通信，服务器不能主动连接客户端

ServerSocket实现服务器端

Socket实现客户端

先要创建服务器对象，再创建客户端对象

### ServerSocket

首先创建服务器程序

在java.net包中提供了一个ServerSocket类来实现服务器程序

构造方法可以指定端口号、IP地址和等待客户端数量（默认为50）

### Socket

创建客户端程序

构造方法可以指定端口号、IP地址和主机地址

在建立连接后，客户端和服务器端时以I/O流的形式进行交互实现通信的

### 简单的TCP网络程序

先要创建服务器程序

> ```java
> //创建指定端口为7788的ServerSocket对象
> 
> ServerSocket serverSocket = new ServerSocket(7788);
> 
> 	while(true){
> 
> 	//调用ServerSocket的accept()方法开始接收数据
> 
> 	Socket client  = serverSocket.accpt();
> 
> 	//获取客户端的输出流对象
> 
> 	OutputSttream os = client.getOutputStream();
> 
> 	//当客户端连接到服务器时，向客户端输出数据
> 
> 	os.write(("服务器向客户度做出相应：").getBytes());
> 
> 	//模拟与客户端交互耗时
> 
> 	Thread.sleep(5000);
> 
> 	//关闭流和Socket接口
> 
> 	os.close();
> 
> 	client.close();
> 
> }
> ```
>
> 

创建客户端程序

> ```java
> //创建一个Socket并连接到指定的服务器端
> 
> Socket client =new Socket(InetAddress.getLocalHost(),7788);
> 
> //获取服务队返回的输入流对象并打印
> 
> InputStream is = client.getInputStream();
> 
> byte [] buf = new byte[1024];
> 
> int len = is.read(buf);
> 
> while(len !=-1){
> 
> 	System.out.println(new String(buf,0,len));
> 
> 	len = is.read(buf);
> 
> }	
> 
> //关闭流和Socket接口
> 
> 	os.close();
> 
> 	client.close();
> ```

### 多线程的TCP网络程序

### TCP案例-文件上传