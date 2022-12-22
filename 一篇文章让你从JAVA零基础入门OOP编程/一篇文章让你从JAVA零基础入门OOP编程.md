![202212221409881](https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221413207.jpg)











# 一篇文章让你从JAVA零基础入门`OOP`编程



> 前言：
>
> 此文为玄子，复习`ACCP-S1`课程后，整理的文章，文中对知识点的解释仅为个人理解。
>
> 配套PPT，站点源码，等学习资料
>



# 一、预科



## 1.1 JAVA 介绍

Java 是 Sun Microsystems 于1995年推出的高级编程语言

### 1.1.1 JAVA 之父

詹姆斯·高斯林（James Gosling）是一名软件专家，1955年5月19日出生于加拿大，Java编程语言的共同创始人之一，一般公认他为“Java之父”。

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221410520.jpg" alt="Java之父" style="zoom:80%;" />                <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221410485.jpg" alt="Java之父" style="zoom: 50%;" />                                

### 1.1.2 JAVA 的核心优势

跨平台是 Java 语言的核心优势，赶上最初互联网的发展，并随着互联网的发展而发展，建立了强大的生态体系，目前已经覆盖 IT 各行业的“第一大语言”，是计算机界的“英语”。

### 1.1.3 JAVA 各版本的含义

​	JavaSE（Java Standard Edition）：标准版，定位在个人计算机上的应用

​	JavaEE（Java Enterprise Edition）：企业版，定位在服务器端的应用

​	JavaME（Java Micro Edition）：微型版，定位在消费性电子产品的应用上

### 1.1.4 JAVA 运行机制

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415480.png" alt="1.1.4 JAVA 运行机制" style="zoom:80%;" />

计算机高级语言的类型主要有编译型和解释型两种，而Java 语言是两种类型的结合。

### 1.1.4 JVM、JRE 和 JDK

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415085.jpg" alt="1.1.4 JVM、JRE 和JDK" style="zoom:80%;" />

​	Java Virtual Machine (JVM) ：用于执行字节码的”虚拟计算机”。不同的操作系统有不同版本 JVM，屏蔽了底层运行平台的差别，是实现跨平台的核心。

​	Java Runtime Environment (JRE) 包含：Java 虚拟机、库函数等。

​	Java Development Kit (JDK)包含：JRE，编译器和调试器等。

---



## 1.2  JAVA 开发环境搭建

### 1.2.1 下载 JDK

1. [ORACLE官网](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html)

   ![1.2.1 下载 JDKORACLE官网](https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415811.png)

下滑找到 Windows x64 安装程序，点击后方链接下载安装包。

### 1.2.2 安装 JDK

1. 按照图中指引一直下一步就可以了

2. ！！！中间可以更改安装位置，但不建议更改，为了方便后期配置环境变量。

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415273.png" alt="1.2.2安装JDK-1" style="zoom: 50%;" />

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415671.png" alt="1.2.2安装JDK-2" style="zoom: 50%;" />

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415799.png" alt="1.2.2安装JDK-3" style="zoom: 50%;" />
   
   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415164.png" alt="1.2.2安装JDK-4" style="zoom: 50%;" />
   
   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415790.png" alt="1.2.2安装JDK-5" style="zoom: 50%;" />

### 1.2.3 配置环境变量

1. 右键此电脑属性

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221424152.png" alt="1.2.3 配置环境变量-1" style="zoom:50%;" />

2. 高级系统设置

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415422.png" alt="1.2.3 配置环境变量-2" style="zoom: 50%;" />

3. 点击右下角环境变量

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415419.png" alt="1.2.3 配置环境变量-3" style="zoom: 50%;" />

4. 新建环境变量

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415690.png" alt="1.2.3 配置环境变量-4" style="zoom: 50%;" />

5. 变量名：

   > JAVA_HOME

   变量值：java JDK 安装路径 

   默认为：

   > C:\Program Files\Java\jdk1.8.0_341

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415265.png" alt="1.2.3 配置环境变量-5" style="zoom:50%;" />

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415047.png" alt="1.2.3 配置环境变量-6" style="zoom:50%;" />

   设置完成后点击确定

6. 再次点击新建

   变量名：

   > CLASSPATH

   变量值：

   > .;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;

   ！！！变量值是固定的，注意开头为英文字符点

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415860.png" alt="1.2.3 配置环境变量-7" style="zoom:50%;" />

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221415959.png" alt="1.2.3 配置环境变量-8" style="zoom:50%;" />

7. 下滑找到`Path`双击变量值进入设置

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416639.png" alt="1.2.3 配置环境变量-9" style="zoom:50%;" />

   然后点击右上角新建，值为 JDK 安装的`bin`目录

   默认为：

   > C:\Program Files\Java\jdk1.8.0_341\bin

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416443.png" alt="1.2.3 配置环境变量-10" style="zoom:50%;" />

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416268.png" alt="1.2.3 配置环境变量-11" style="zoom:50%;" />

   ！！！请注意这个值和 JAVA_HOME 是不一样的，要进入到`bin`目录的路径后在复制

8. 然后继续添加两条变量

   变量固定分别为：

   > %JAVA_HOME%\bin 
   >
   > %JAVA_HOME%\jre\bin

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416287.png" alt="1.2.3 配置环境变量-12" style="zoom:50%;" />

9. 这里直接点击编辑本文，在变量尾部一次添加完效果是一样的

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416848.png" alt="1.2.3 配置环境变量-14" style="zoom:50%;" />

   变量值：

   > C:\Program Files\Java\jdk1.8.0_341\bin;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;

### 1.2.4 检验环境变量

1. 键盘按下`Win + R`输入`cmd`后按回车

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221423889.png" alt="1.2.3 配置环境变量-16" style="zoom:50%;" />

2. 在窗体输入：

   > Java -version

！！！java 后面有一个空格

3. 显示 java version “1.8.0_341” 即为环境变量配置成功

   后面的 1.8.0_341 就是所安装 java 的 JDK 版本

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221420715.png" alt="1.2.3 配置环境变量-17" style="zoom:50%;" />

4. 恭喜你！到这里 JDK 的下载、安装、配置环境变量就已经全部完成了

---



## 1.3 编写第一个 JAVA 程序

### 1.3.1 编写 JAVA 代码

1. 在桌面上右键新建文本文档

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416031.png" alt="1.3编写第一个Java程序-1" style="zoom: 67%;" />

2. 将新建的文本文档更名为`ChangeTheWorld`

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416120.png" alt="1.3编写第一个Java程序-2" style="zoom:150%;" />

3. 如果你新建的文本文档没有显示`.txt`后缀的话需要在文件资源管理器中设置显示

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416871.png" alt="1.3编写第一个Java程序-3" style="zoom:50%;" />

4. 鼠标双击打开文本文档输入以下代码

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416040.png" alt="1.3编写第一个Java程序-4" style="zoom:50%;" />

```java
public class ChangeTheWorld {
    public static void main(String[] args) {
        
        System.out.println("Change The World!");

    }
}
```

> class 后面的代码要和文件名一致
>
> ！！！全文都是在英文输入法下编写

### 1.3.2 执行 JAVA 程序

1. 将文件名后缀修改为`.java`例如：`ChangeTheWorld.java`

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416019.png" alt="1.3编写第一个Java程序-5" style="zoom:150%;" />

2. 将修改后的 Java 文件复制到任意磁盘根目录

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416913.png" alt="1.3编写第一个Java程序-6" style="zoom:50%;" />

3. 点击文件地址栏输入`cmd`回车

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416573.png" alt="1.3编写第一个Java程序-7" style="zoom:50%;" />

4. 分别输入`javac`和`java`代码执行编译，下面显示的`Change The World`即为我们编写的 Java 输出语句所输出的代码

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416704.png" alt="1.3编写第一个Java程序-8" style="zoom: 67%;" />

   > javac ChangeTheWorld.java
   >
   > java ChangeTheWorld

   > javac 后面跟文件全名，需要带`.java`后缀
   >
   > java 后直接写文件名即可

5. 到这里你已经可以独立编写，编译 Java 代码了，后面我们会在学习一些计算基础知识。

---



## 1.4 电脑常用快捷键

熟练的使用电脑快捷键，可以让我们的工作效率事半功倍。

| 按键               | 说明       |
| :----------------- | ---------- |
| Ctrl + A           | 全选       |
| Ctrl + C           | 复制       |
| Ctrl + V           | 粘贴       |
| Ctrl + X           | 剪切       |
| Ctrl + Z           | 撤销       |
| Ctrl + Y           | 撤回       |
| Ctrl + S           | 保存       |
| Alt + F4           | 关闭窗体   |
| Windows + R        | 运行       |
| Windows + L        | 快速锁屏   |
| Windows + E        | 资源管理器 |
| Ctrl + Shift + ESC | 任务管理器 |

---



## 1.5 DOS 命令

### 1.5.1 打开 CMD 的方法

1. 开始 > 系统 > 命令提示符

2. 按下 Win + R 输入 cmd 打开控制台（推荐使用）

3. 在任意的文件夹下面，按住 Shift + 鼠标右键点击，在此处打开命令行窗口

4. 资源管理器的地址栏前面加上 cmd 路径

   >  管理员方式运行：选择以管理员方式运行

### 1.5.2 常用 DOS 命令

| 命令                           | 说明                     | 备注                         |
| ------------------------------ | ------------------------ | ---------------------------- |
| C:                             | 选择盘符                 | 盘符名称加冒号               |
| dir                            | 查看当前目录下的所有文件 |                              |
| cd /d  C:                      | 盘符切换                 | Change Directory             |
| cd  文件名\文件名              | 目录切换                 |                              |
| cd..                           | 返回上一级目录           |                              |
| cls                            | 清理屏幕                 | Clear Screen                 |
| exit                           | 退出                     |                              |
| ipconfig                       | 查看电脑 IP 地址         |                              |
| clac<br />mspaint<br />notepad | 打开本地程序             | 计算器<br />画图<br />记事本 |
| ping 网址                      | ping命令                 |                              |
| md 文件名                      | 创建文件夹               | Make Directory               |
| cd> a.txt                      | 创建文件                 | 注意文件后缀                 |
| del  a.txt                     | 删除文件                 | 注意文件后缀                 |
| rd 文件名                      | 移除目录                 | Remove Directory             |

---



## 1.6 计算机语言发展史

### 1.6.1 一代语言

机器语言：

- 我们都知道计算机的基本计算方式都是基于二进制的方式。

- 二进制：010111001010110010110100

- 这种代码是直接输入给计算机使用的，不经过任何的转换！

| 十进制 | 二进制 |
| :----: | :----: |
|   1    |   1    |
|   2    |   10   |
|   3    |   11   |
|   4    |  100   |
|   5    |  101   |
|   6    |  110   |
|   7    |  111   |
|   8    |  1000  |
|   16   | 10000  |
|   32   | 100000 |

### 1.6.2 二代语言

汇编语言

- 解决人类无法读懂机器语言的问题

- 指令代替二进制


目前应用：

- 逆向工程
- 机器人
- 病毒

### 1.6.3 三代语言

- 高级语言

- 大体上分为：**面向过程**和**面向对象**两大类

- C语言是典型的面向过程的语言。C++、JAVA是典型的面向对象的语言

高级语言：

- C 

- C++ 

- JAVA

- C#  

- Python

  > 先有`C`语言，经改良后为`C++`面向对象语言，再有`JAVA`，`C#`是微软基于`JAVA`研发的`.NET`平台软件
  >

---



## 1.7 安装 JAVA 开发工具

### 1.7.1 Intellij IDEA 开发工具

Intellij IDEA 是目前主流的Java 开发工具，但是由于版权原因这里不过多介绍。

[Intellij IDEA官网](https://www.jetbrains.com/idea/)

### 1.7.2 初始化设置 IDEA 2022.3

工欲善其事比先利其器，Idea 有许多使用的插件和设置，可以让我们更加舒服的编写代码。

1. 汉化，分别点击左上角 fill >  Settings

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416154.png" alt="1.7初始化IDEA-1" style="zoom: 67%;" />

2. 按照下图点击 Plugins 搜索`Chinese`下载汉化包后点击右下角 Apply 应用安装

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221416856.png" alt="1.7初始化IDEA-2" style="zoom: 67%;" />

3. 还有一些实用插件分享，从上到下分别是：代码规范，UI美化，汉化包，快捷键提示，彩虹括号，代码补全提示。

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221417987.png" alt="1.7初始化IDEA-3" style="zoom: 67%;" />

4. 以及保存代码时自动格式化代码。

   <img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221417424.png" alt="1.7初始化IDEA-4" style="zoom: 67%;" />

---



# 二、JAVA 基础

## 2.1 使用 IDEA 编写 JAVA 程序

### 2.1.1 Change The World

```java
package CH01_JAVABase;
//Change The World!
public class XZ01_ChangeTheWorld {
    public static void main(String[] args) {
        System.out.println("Change The World!");
        //Change The World!
    }
}
```

```java
public class XZ01_ChangeTheWorld {}
// public 关键字
// XZ01_ChangeTheWorld 类名与文件名要完全一样
```

```java
public static void main(String[] args) {}
// main( )方法四要素必不可少 public static void main
// main( )方法是 Java 程序执行的入口点
```

```java
System.out.println("Change The World!");
// 从控制台输出信息
```

| 代码语句                                    | 说明                 | 快捷语句  |
| ------------------------------------------- | -------------------- | --------- |
| public static void main(String[] args) {  } | Main函数，程序主入口 | main/psvm |
| System.out.println( );                      | 输出语句             | sout      |

---



## 2.2 注释

注释不会出现在字节码文件中，即Java 编译器编译时会跳过注释语句。

### 2.2.1 单行注释

单行注释使用` // `开头。

### 2.2.2 多行注释

多行注释以` /* `开头以` */ `结尾。注意，多行注释不能嵌套使用。

### 2.2.3 文档注释

文档注释以`/** `开头以` */`结尾，注释中包含一些说明性的文字及一些 JavaDoc 标签（后期写项目时，可以生成项目的API）

### 2.2.4 演示案例

```java
package CH01_JAVABase;
//注释

/**
 * XZ04_Annotate 类（我是文档注释）
 *
 * @author 玄子 （作者）
 * @version 1.0 （版本）
 */
public class XZ04_Annotate {
    //我是单行注释
    public static void main(String[] args) {
        System.out.println("Change The World!");
    /*
        System.out.println("Change The World!");
        System.out.println("我是多行注释！");
    */
    }
}
```

| 注释语法 | 注释名称 | 快捷键   |
| -------- | -------- | -------- |
| //       | 单行注释 | Ctrl + / |
| /*  */   | 多行注释 |          |
| /** */   | 文档注释 |          |

| 文档注释参数 | 描述                      |
| ------------ | ------------------------- |
| @author      | 作者名                    |
| @version     | 版本号                    |
| @since       | 指明需要最早使用的jdk版本 |
| @param       | 参数名                    |
| @return      | 返回值情况                |
| @throws      | 异常抛出情况              |

> JavaDoc命令是用来生成自己API文档的
>
> [JavaAPI帮助文档](https://docs.oracle.com/en/java/javase/)
>
> [Java8API帮助文档](https://docs.oracle.com/javase/8/docs/api/index.html)

---



## 2.3 数据类型

Java 数据类型分为两大类：基本数据类型（primitive data type）和引用数据类型（reference data type）。

<img src="https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221417217.jpg" alt="2.3 基本数据类型-1"  />

### 2.3.1 整型（byte、short、int、long）

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {
        int num1 = 1;
        byte num2 = 1;
        short num3 = 1;
        long num4 = 1L;
        // long 的数值后面需要加大写字母 L
        //整型
    }
}
```

| 类型  | 占用存储空间 |                     表数范围                      |
| :---: | :----------: | :-----------------------------------------------: |
| byte  |    1 字节    |            -2^7^ ~ 2^7^-1（-128~127）             |
| short |    2 字节    |         -2^15^ ~ 2^15^-1 （-32768~32767）         |
|  int  |    4 字节    | -2^31^ ~ 2^31^-1 (-2147483648~2147483647) 约21 亿 |
| long  |    8 字节    |                  -2^63^~ 2^63^-1                  |

### 2.3.2 浮点型（double、float）

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {
        double num5 = 1.1;
        float num6 = 1.2F;
        // float 的数值后面需要加大写字母 F
        //浮点型
    }
}
```

|  类型  | 占用存储空间 |       表数范围       |
| :----: | :----------: | :------------------: |
| float  |    4 字节    |  -3.403E38~3.403E38  |
| double |    8 字节    | -1.798E308~1.798E308 |

### 2.3.3 字符型（char）

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {
        char ch = 'a';
        char ch = '玄';
        //单字符
    }
}
```

> 字符型在内存中占 2 个字节，在 Java 中使用单引号来表示字符常量。例如`'A'`是一个字符，它与`"A"`是不同的，`"A"`表示含有一个字符的字符串。
>
> char 类型用来表示在 Unicode 编码表中的字符。Unicode 编码被设计用来处理各种语言的文字，它占 2 个字节，可允许有 65536 个字符。

### 2.3.4 布尔型（boolean）

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {
        boolean is = false;
        boolean is = true;
        // 只有两个结果 true false
        //布尔型
    }
}
```

### 2.5 引用型（String）

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {
        String string = "Change The World!";
        //引用型，不属于基本数据类型
    }
}
```

---



## 2.4 数据类型转换

八种基本数据类型，除了boolean 类型之外的七种类型是可以自动转化的。

自动类型转换指的是容量小的数据类型可以自动转换为容量大的数据类型。如图下所
示，的实线表示无数据丢失的自动类型转换，而虚线表示在转换时可能会有精度的损失。

![2.4 数据类型转换-1](https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221417346.jpg)

### 2.4.1 隐式类型转换（自动类型转换）

可以将整型常量直接赋值给byte、short、char 等类型变量，而不需要进行强制类
型转换，只要不超出其表数范围即可。

```java
package CH01_JAVABase;

//数据类型转换
public class XZ03_TypeConversion {
    public static void main(String[] args) {
        int a = 1;
        double b = a;
        System.out.println(b);
        // b = 1.0
        //隐式数据类型转换，自动转换
    }
}
```

### 2.4.2 显示类型转换（强制类型转换）

```java
package CH01_JAVABase;

//数据类型转换
public class XZ03_TypeConversion {
    public static void main(String[] args) {
        double c = 1.2;
        int d = (int) c;
        System.out.println(d);
        // d = 1
        //显式数据类型转换转换变量前加 (转换类型)
    }
}
```

### 2.4.3 数据类型转换拓展

```java
package CH01_JAVABase;

//数据类型转换
public class XZ03_TypeConversion {
    public static void main(String[] args) {
        char e = 'a';
        int f = e + 1;
        System.out.println((int) e);
        // 97
        System.out.println(f);
        // 98
        System.out.println((char) f);
        // b
    }
}
```

注意点：

1. 不能对布尔值进行转换
2. 不能把对象类型转换为不相干的类型
3. 在把高容量转换到低容量的时候，强制转换
4. 转换的时候可能存在内存溢出，或者精度问题！
5. 这里的数据类型转换就证明了 char 类型的值本质上还是数字。
6. [ASCII编码表](https://baike.so.com/doc/7103239-7326232.html)

---



## 2.5 变量

### 2.5.1 变量介绍

```java
package CH01_JAVABase;

//变量
public class XZ05_Variable {
    static String str = "XuanZi";  //类变量
    //成员变量
    int age;  //默认值 0
    String Sex = "男";  //默认值null
    boolean IsNull; //默认值false

    public static void main(String[] args) {
        //局部变量
        int value = 1;
        String name = "玄子";

        //创建类的对象调用方法
        XZ05_Variable variable = new XZ05_Variable();
        System.out.println(name);
        //输出局部变量
        variable.set();
        //调用类方法
        System.out.println(variable.IsNull);
        //实例变量需要创建对象后才能调用
        System.out.println(str);
        //类变量可直接调用
    }

    public void set() {
        String conn = "XuanZiShare";  //局部变量
        System.out.println(age);
        System.out.println(Sex);
        System.out.println(conn);
    }
}
```

变量（variable）：
- 变量本质上就是代表一个”可操作的存储空间”，空间位置是确定的，但是里面放置什么值不确定
- Java 是一种强类型语言，每个变量都必须声明其数据类型。变量的数据类型决定了变量占据存储空间的大小
- 可通过变量名来访问“对应的存储空间”，从而操纵这个“存储空间”存储的值。

注意事项：
- 每个变量都有类型，类型可以是基本类型，也可以是引用类型
- 变量名必须是合法的标识符
- 变量声明是一条完整的语句，因此每一个声明都必须以分号结束

### 2.5.2 类变量具有默认值，声明时可不对其赋值

| 变量类型                             | 默认值 |
| ------------------------------------ | ------ |
| 整型（int，byte，short，long）       | 0      |
| 单精度浮点型（float）                | 0.0f   |
| 双精度浮点型（double）               | 0.0d   |
| 字符型（char）                       | /u0000 |
| 布尔型（boolean）                    | false  |
| 引用类型（array，String，class，……） | null   |

### 2.5.3 变量的分类和作用域

变量有三种类型：局部变量、成员变量(实例变量)和静态变量(类变量)

|   类型   |      声明位置       |   从属于    |                      生命周期（作用域）                      |
| :------: | :-----------------: | :---------: | :----------------------------------------------------------: |
| 局部变量 |  方法或语句块内部   | 方法/语句块 | 从声明位置开始，直到方法或语<br/>句块执行完毕，局部变量消失  |
| 成员变量 |  类内部，方法外部   |    对象     | 对象创建，成员变量也跟着创建<br/>对象消失，成员变量也跟着消失 |
| 静态变量 | 类内部，static 修饰 |     类      |    类被加载，静态变量就有效<br />类被卸载，静态变量消失。    |

---



## 2.6 常量

```java
package CH01_JAVABase;

//常量
public class XZ06_Constant {
    //            final 数据类型 常量名 = 值；
    public static final double PI = 3.14;
    // public static 修饰符，不存在先后顺序
    public static void main(String[] args) {
        System.out.println(PI);
    }
}
```

常量（Constant）：
- 初始化(initialization)后不能再改变值！不会变动的值
- 所谓常量可以理解成一种特殊的变量，它的值被设定后，在程序运行过程中不允许被改变
- 常量名一般使用大写字符

---



## 2.7 运算符

计算机的基本用途就是执行数学运算，Java 提供了一套丰富的运算符来操作变量。

### 2.7.1 一元运算符

```java
int num1 = 1;
double num2 = 2.5;
System.out.println(num1+num2);// 1
// mum1 + 1   上一句输出后才+1   2
// 1 + mum1   下一句输出前就+1   3
System.out.println(num2 % num1); //0.5
//  +    -   *  /   %
//  加   减  乘  除  余
```

> 加、减 、乘、除。与正常数学运算用法一致，余（%）在 Java 中表示求余数 例如`2.5 % 1`的余数就是`0.5`。如果两个数都为`int`型的话，余数会舍去尾数，取整数。

### 2.7.2 二元运算符

```java
int num1 = 1;
System.out.println(num1++);
// ++ 写在变量后面等于 mum1 + 1   输出后才 +1 =  2
System.out.println(++num1);
// ++ 写在变量前面等于 1 + mum1   输出前就 +1 = 2 + 1 = 3
System.out.println(num1 + 1); // 4
// 二元运算符，是改变，变量实际值进行运算，值会随着运算而改变
//   ++   --
//  自增  自减
```

### 2.7.3 赋值运算符

```java
int num1 = 1;
System.out.println(num1);
//  =
// 赋值
```

### 2.7.4 扩展运算符

```java
int a = 10;
int b = 20;
System.out.println(a += b); 
//  a = a + b = 10 + 20 = 30
System.out.println(a); // 30
//和二元运算符一样，运算时，是改变自身实际值运算
//  +=    -=    *=    /=   %
// 加等  减等   乘等   除等 余等
```

### 2.7.5 关系运算符

```java
int num1 = 1;
double num2 = 2.5;
System.out.println(num1 <= num2); 
// 结果是布尔型 true 或 false
//  >     <     >=       <=       !=      ==
// 大于   小于  大于等于  小于等于  不等于  等等于
```

### 2.7.6 逻辑运算符

```java
int num1 = 1;
double num2 = 2.5;
System.out.println(num1 > num2 || num2 > num1);
//两个条件一个为真就返回true
//如果第一个条件就为假直接返回 false，不再判断第二个条件
System.out.println(num1 > num2 && num2 > num1);
//两个条件均为真才返回 true
System.out.println(!(num1 > num2 && num2 > num1));
//判断结果取反
//  结果是布尔型 true 或 false
//  &&  ||  !
//  与  或  非
```

### 2.7.7 位辑运运算符

```java
char A = 'A';
char B = 'B';
System.out.println("A:" + (int) A);
System.out.println("B:" + (int) B);
System.out.println(A ^ B);
//        -------二进制---------
//        A = 0011 1100
//        B = 0000 1101
//        --------判断--------
//        A&B = 0000 1100  不同为0相同为1
//        A|B = 0011 1101  有1即为1
//        A^B = 0011 0001  相同为0不同为1
//        ~B  = 1111 0010  1为0 0为1
System.out.println(2 << 3);
//        -------二进制---------
//        0000 0000  0
//        0000 0001  1
//        0000 0010  2
//        0000 0011  3
//        0000 0100  4
//        0000 1000  8
//        0001 0000  16
//  &   |   ^       ~           <<        >>
//  与  或  非  异或(按位取反)   左移(*)  右移(/)
```

### 2.7.8 条件运算符

```java
int score = 60;
String type = score >= 60 ? "及格" : "不及格";
System.out.println(type);
//     ?       :
// 布尔 ? 条件1 : 条件2
// 如果布尔结果为 true 那么结果为条件1，否则结果为条件2
```

### 2.7.9 字符串连接符

```java
System.out.println("" + 10 + 20);   // 1020 
System.out.println(10 + 20 + "");   // 30
// String写在前后的区别
System.out.println("" + (10 + 20)); // 30
// ()加强运算优先级
```

### 2.7.10 算术方法

```java
System.out.println("Math.pow(2, 3) = " + Math.pow(2, 3));
// 2的三次方   8.0 
System.out.println("Math.pow(3, 2) = " + Math.pow(3, 2));
// 3的二次方   9.0
// Math.方法
```

### 2.7.11 常用运算符表

| 运算符种类         | 符号                             | 描述                                                         |
| ------------------ | -------------------------------- | ------------------------------------------------------------ |
| 算术运算符（一元） | +，-，*，/，%                    | 加，减，乘，除，余                                           |
| 算术运算符（二元） | ++，--                           | 自增，自增                                                   |
| 赋值运算符         | =                                | 赋值                                                         |
| 扩展运算符         | +=，-=，*=，/=，%=               | 加等，减等，乘等，除等，余等                                 |
| 关系运算符         | >，<，>=，<=，==，!=，instanceof | 大于，小于，大于等于，小于等于，等等于，不等于，实例判断     |
| 逻辑运算符         | &&，\|\|，!，^                   | 与，或，非，按位                                             |
| 位辑运运算符       | &，\|，^，~ ， >>，<<            | 与，或，非，异或(按位取反)，左移(*)，右移(/)                 |
| 条件运算符（三目） | ? :                              | 布尔 ? 条件1 : 条件2<br />如果布尔结果为 true 那么结果为条件1，否则结果为条件2 |
| 字符串连接符       | +                                | 拼接两个字符串                                               |

---



## 2.8 转义符

### 2.8.1 println() 与 print() 的区别

```java
System.out.println("Change The World!");
// 打印完引号中的信息后会自动换行
```

```java
System.out.println("Change The World!");
// 打印输出信息后不会自动换行 
```

### 2.8.2 转义符 \n 与 \t

```java
package CH01_JAVABase;

//转义符
public class XZ08_EscapeCharacter {
    public static void main(String[] args) {
        System.out.println("人生若只如初见，何事秋风悲画扇。");
        System.out.println("============================");
        System.out.print("人生若只如初见，");
        //这里的输 print 加上ln同样表示换行
        System.out.println("何事秋风悲画扇。");
        System.out.println("============================");
        System.out.println("人生若只如初见，\n何事秋风悲画扇。");
        System.out.println("============================");
        System.out.println("人生若只如初见，\t何事秋风悲画扇。");
        //\n 换行
        //\t 占位符
    }
}
```

### 2.8.3 常用转义符表

| 转义字符 | 意义                                | ASCII码值(十进制) |
| -------- | ----------------------------------- | ----------------- |
| \a       | 响铃(BEL)                           | 007               |
| \b       | 退格(BS) ，将当前位置移到前一列     | 008               |
| \f       | 换页(FF)，将当前位置移到下页开头    | 012               |
| \n       | 换行(LF) ，将当前位置移到下一行开头 | 010               |
| \r       | 回车(CR) ，将当前位置移到本行开头   | 013               |
| \t       | 水平制表(HT) (跳到下一个TAB位置)    | 009               |
| \v       | 垂直制表(VT)                        | 011               |
| \\       | 代表一个反斜线字符'\'               | 092               |
| \'       | 代表一个单引号(撇号)字符            | 039               |
| \"       | 代表一个双引号字符                  | 034               |
| \?       | 代表一个问号                        | 063               |
| \0       | 空字符(NULL)                        | 000               |
| \ooo     | 1到3位八进制数所代表的任意字符      | 三位八进制        |
| \xhh     | 十六进制所代表的任意字符            | 十六进制          |

---



## 2.9 命名规范与关键字

```java
package CH01_JAVABase;

//命名规范
public class XZ09_NamingSpecification {
    public static void main(String[] args) {
        // Java 所有的组成部分都需要名字。
        // 类名、变量名以及方法名都被称为标识符。
        String name;
        int num;
        double value;
        boolean is;
        //尽量使用英语单词作为标识符

        //常用命名法
        String studentName = "玄子";
        //驼峰命名法：以小写字母开头，第二个及以后单词首字母大写
        String StudentName = "玄子";
        //帕斯卡命名法：以大写字母开头，第二个及以后单词首字母大写
    }
}
```

### 2.9.1 JAVA 常用关键字

|    ———     |    ———     |   ———   |    ———    |     ———      |
| :--------: | :--------: | :-----: | :-------: | :----------: |
|  abstract  |   assert   | boolean |   break   |     byte     |
|    case    |   catch    |  char   |   class   |   continue   |
|  default   |     do     | double  |   else    |     enum     |
|  extends   |   final    | finally |   float   |     for      |
|     if     | implements | import  |    int    |  interface   |
| instanceof |    long    | native  |    new    |   package    |
|  private   | protected  | public  |  return   |    short     |
|   static   |  strictfp  |  super  |  switch   | synchronized |
|    this    |   throw    | throws  | transient |     try      |
|    void    |  volatile  |  while  |           |              |

### 2.9.2 识符命名规范

- 所有标识符应具有实际意义，尽量不要使用 a、b 这样的无意义命名
- 所有的标识符都应该以字母（A-Z或者a-z），美元符（$）、或者下划线（_）开始
- 首字符之后可以是字母（A-Z或者a-z），美元符（$）、下划线（_）或数字的任何字符组合
- 不能使用关键字作为变量名或方法名
- 识符是大小写敏感的
- 合法标识符举例：age、$salary、_value、_1_value
- 非法标识符举例：123abc、-salary、#abc
- 可以使用中文命名，但是一般不建议这样去使用，也不建议使用拼音，很Low

### 2.9.3 常用命名法

- 所有变量、方法、类名：见名知意，具有实际意义
- 类成员变量：驼峰命名法：studentName
- 局部变量：驼峰命名法：studentAge
- 常量：以大写字母命名，下划线拼接：MAX_VALUE
- 类名：帕斯卡命名法：StudentName
- 方法名：帕斯卡命名法：StudentAge( )
- 所有方法都带有( )

---



## 2.10 包机制

```java
package CH01_JAVABase;

//包机制
public class XZ10_PackageMechanism {
    public static void main(String[] args) {
//        为了更好地组织类，Java提供了包机制，用于区别类名的命名空间。
//        包语句的语法格式为：
//        package pkg1[. pkg2[. pkg3...]];

//        一般利用公司域名倒置作为包名；com.XuanZiShare.www
//        为了能够使用某一个包的成员，我们需要在Java程序中明确导入该包。
//        使用“import”语句可完成此功能
//        import package1[.package2...].(classname|*);
//        *通配符  所有
    }
}
```

---



# 三、流程控制语句

## 3.1 Scanner 用户交互

Scanner 类是在 jdk1.5 版本引入的，它在 java 的 util 工具包下，主要用于扫描用户从控制台输入的文本。当我们需要通过控制台输入数据时，只需要事先导入 java.util 包中的 Scanner 类，然后调用 Scanner 类，我们的程序就能获取我们在控制台所输入的数据了。

### 3.1.1 导包

```java 
import java.util.Scanner;
```

在 IDEA 中可直接创建 Scanner 对象 IDEA 会自动帮我们导包

### 3.1.2 基本用法

```java
package CH02_JAVAProcessControl;
//基础Scanner

import java.util.Scanner;

//导包
public class XZ01_UserInteraction {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        // 创建Scanner对象
        // input 是对象名称，在符合命名规范前提下，可随意命名
        System.out.println("请输入：");
        if (input.hasNext()) {
            //  判断用户是否输入数据
            String i = input.next();
            //  声明变量接收用户输入数据，例如
            //  input.nextDouble();
            //  input.nextInt();
            System.out.println(i);
            //  输出接收用户输入数据的变量
        }
        input.close();
        //  关闭Scanner对象
    }
}
```

> 通过 Scanner 类的 next() 与 nextLine() 方法获取输入的字符串，在读取前我们一般需要使用 hasNext() 与 hasNextLine() 判断是否还有输入的数据。

> 使用完Scanner后，我们一定要记得将它关闭，因为使用Scanner本质上是打开了一个 IO 流，如果不关闭的话，它将会一直占用系统资源。注意一旦你关闭后，就算在`input.close();`这行代码后你再重新创建 Scanner 对象也不能重新再打开一个扫描器了，如果继续使用程序会报错，所以一定要在用不到扫描器之后再关闭，即把`input.close();`放到代码的最后。

### 3.1.3 next() 与 nextLine() 的区别

```java
package CH02_JAVAProcessControl;
//基础Scanner

import java.util.Scanner;

public class XZ01_UserInteraction2 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("next() 与 nextLine() 的区别");
        String i2 = input.nextLine();
        // String i2 = input.next();
        System.out.println(i2);
        // NextLine与Next的区别：
        // NextLine会记录用户输入直到按下回车键的所有数据
        // Next遇到空格就自动停止
        input.close();
    }
}
```

next() 用法总结：

- 一定要读取到有效字符后才可以结束输入
- 对输入的有效字符之前所遇到的空白，会自动将其去除
- 只有输入的有效字符后才将其后面输入的空白作为结束符
- next()不能得到带有空格的字符串

nextLine() 用法总结：

- 以回车符作为结束标识符，获取到的是回车符前输入的所有字符串（包括空格）

### 3.1.4 案例

```java
package CH02_JAVAProcessControl;
//基础Scanner

import java.util.Scanner;

public class XZ01_UserInteraction3 {
    public static void main(String[] args) {
        //我们可以输入多个数字，并求其总和与平均数，每输入一个数字用回车确认，
        //通过输入非数字来结束输入并输出执行结果：
        Scanner input = new Scanner(System.in);
        double sum = 0;
        // 声明变量记录用户输入数据和
        int count = 0;
        // 声明变量记录用户输入数据次数
        System.out.println("请输入数字(输入字母停止)");
        while (input.hasNextDouble()) {
            // 只有用户输入Double类型数据才会执行
            sum += input.nextDouble();
            // 记录和的变量，加上用户当前输入数据
            count++;
            // 用户输入数据次数+1
        }
        System.out.println(count + "个数的和为：" + sum);
        input.close();
    }
}
```

### 3.1.5 顺序结构

- JAVA的基本结构就是顺序结构，除非特别指明，否则就按照顺序一句一句执行。
- 顺序结构是最简单的算法结构。
- 语句与语句之间，框与框之间是按从上到下的顺序进行的，它是由若干个依次执行的处理步骤组成的，它是**任何一个算法都离不开的一种基本算法结构。**

---



## 3.2 If 选择结构

### 3.2.1 单层 if 选择结构

```java
package CH02_JAVAProcessControl;

//单层 if 选择结构
public class XZ02_SelectStructure {
    public static void main(String[] args) {
        int i = 60;

        if (i >= 60) {
            System.out.println("及格");
            //当结果为true执行
        } else {
            System.out.println("不及格");
            //当结果为false执行
        }

    }
}
```

### 3.2.2 多重 if 选择结构

```java
package CH02_JAVAProcessControl;
//多重 if 选择结构

import java.util.Scanner;

public class XZ02_SelectStructure2 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        //      判断用户输入数据，对数据进行分区
        System.out.println("请输入成绩");
        double score = input.nextDouble();

        if (score > 100) {
            System.out.println("数据非法");
        } else if (score <= 100 && score >= 90) {
            System.out.println("A级");
        } else if (score >= 80) {
            System.out.println("B级");
        } else if (score >= 70) {
            System.out.println("C级");
        } else if (score >= 60) {
            System.out.println("D级");
        } else {
            System.out.println("不及格");
        }

        input.close();
    }
}
```

### 3.2.3 嵌套 if 选择结构

```java
package CH02_JAVAProcessControl;
//嵌套if

import java.util.Scanner;

public class XZ02_SelectStructure3 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        // 判断用户输入数据，对数据进行分区
        System.out.println("请输入成绩");

        if (input.hasNextDouble()) {
            double score = input.nextDouble();
            // if判断用户输入数据是否为double类型
            // 然后在进行分级判断
            if (score > 100) {
                System.out.println("数据非法");
            } else if (score <= 100 && score >= 90) {
                System.out.println("A级");
            } else if (score >= 80) {
                System.out.println("B级");
            } else if (score >= 70) {
                System.out.println("C级");
            } else if (score >= 60) {
                System.out.println("D级");
            } else {
                System.out.println("不及格");
            }
        }

        input.close();
    }
}
```

### 3.2.4 if 语句执行条件

- 如果第一条 if 语句执行结果就为true则下方的所有if语句都不会在执行
- 也就是如果 if 能进入下一句判断则，他一定不满足上一个 if 的条件

---



## 3.3 Switch 选择结构

### 3.3.1 switch 选择结构

```java
package CH02_JAVAProcessControl;
//switch判断整数

import java.util.Scanner;

public class XZ02_SelectStructure4 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("请输入数字");
        int var = input.nextInt();

        switch (var) {
            case 0:
                System.out.println("值1");
                break;
            case 1:
                System.out.println("值2");
                break;
            case 2:
                System.out.println("值3");
                break;
            default:
                System.out.println("默认值");

        }

        input.close();

    }
}
```

选择结构：

- 多选择结构还有一个实现方式就是switch case 语句

- switch case 语句判断一个变量与一系列值中某个值是否相等，每个值称为一个分支

### 3.3.2 switch 选择结构进阶

```java
package CH02_JAVAProcessControl;
//switch判断字符串

import java.util.Scanner;

public class XZ02_SelectStructure5 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("请输入值");
        String var = input.next();

        switch (var) {
            case "玄子":
                System.out.println("玄子");
                break;
            case "XuanZiShaer":
                System.out.println("XuanZiShaer");
                break;
            default:
                System.out.println("默认值");
        }

        input.close();

    }
}
```

switch 语句中的变量类型可以是：

- byte、short、int 或者 char
- 从 Java SE 7 开始 switch 支持字符串 String 类型了
- 同时 case 标签必须为字符串常量或字面量

### 3.3.3 switch 选择结构案例

```java
package CH02_JAVAProcessControl;
//     输入一个日期判断这个日期已经过了多少天

import java.util.Scanner;

public class XZ02_SelectStructure6 {
    public static void main(String[] args) {

        // 普通闰年:公历年份是4的倍数，且不是100的倍数的，为闰年。
        // 能被4整除，且不能被100整除
        // 世纪闰年:公历年份是整百数的，必须是400的倍数才是闰年)。
        // 能被100整除且被400整除

        Scanner input = new Scanner(System.in);
        System.out.println("请输入日期年：");
        int year = input.nextInt();
        System.out.println("请输入日期月：");
        int month = input.nextInt();
        System.out.println("请输入日期日：");
        int day = input.nextInt();

        switch (month - 1) {
            case 11:
                day += 30;
            case 10:
                day += 31;
            case 9:
                day += 30;
            case 8:
                day += 31;
            case 7:
                day += 31;
            case 6:
                day += 30;
            case 5:
                day += 31;
            case 4:
                day += 30;
            case 3:
                day += 31;
            case 2:
                if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) 				{
                    System.out.println("闰年");
                    day += 29;
                } else {
                    System.out.println("平年");
                    day += 28;
                }
            case 1:
                day += 31;
                break;
        }
        System.out.println(day);
        input.close();
    }
}
```

---



## 3.4 While 循环结构

### 3.4.1 while 循环语句

```java
package CH02_JAVAProcessControl;

//while输出100以内的和
public class XZ03_CirculateStructure {
    public static void main(String[] args) {
        int sum = 0;
        int i = 0;
        while (i <= 100) {

            sum += i;
            i++;
        }
        System.out.println(sum);
    }
}
```

while 是最基本的循环，它的结构为：

- 只要布尔表达式为 true，循环就会一直执行下去
- 大多数情况是会让循环停止下来的，我们需要一个让表达式失效的方式来结束循环
- 少部分情况需要循环一直执行，比如服务器的请求响应监听等
- 循环条件一直为true就会造成无限循环**死循环**，我们正常的业务编程中应该尽量避免死循环。会影响程序性能或者造成程序卡死奔溃

---



## 3.5 Do…While 循环结构

### 3.5.1 do...while 循环语句

```java
package CH02_JAVAProcessControl;

//do while 和while的区别
public class XZ03_CirculateStructure2 {
    public static void main(String[] args) {
        int i = 0;

        while (i < 0) {
            i++;
            System.out.println(i);
        }
        System.out.println("=====================");
        do {
            i++;
            System.out.println(i);
        } while (i < 0);
    }
}
```

do...while 循环：

- 对于while语句而言，如果不满足条件，则不能进入循环。但有时候我们需要即使不满足条件，也至少执行一次
- do...while 循环和 while 循环相似，不同的是 do..while 循环至少会执行一次

### 3.5.2 while 和 do...while 的区别

- while 先判断后执行
- dowhile 是先执行后判断
- Do...while 总是保证循环体会被至少执行一次

---



## 3.6 For 循环结构

### 3.6.1 for 循环语句

```java
package CH02_JAVAProcessControl;

//for循环输出100以内的和
public class XZ03_CirculateStructure3 {
    public static void main(String[] args) {

        int a = 0;
        //初始化    //条件判断 //迭代
        for (int i = 0; i <= 100; i++) {

            a += i;
        }
        System.out.println(a);

    }
}
```

for 循环：

- 虽然所有循环结构都可以用 while 或者 do...while 表示，但 Java 提供了另一种语句 for 循环，使一些循环结构变得更加简单
- for 循环语句是支持迭代的一种通用结构，是最有效、最灵活的循环结构
- for 循环执行的次数是在执行前就确定的

### 3.6.2 for 循环执行步骤

1. 最先执行初始化步骤。可以声明一种类型，但可初始化一个或多个循环控制变量，也可以是空语句
2. 然后，检测布尔表达式的值。如果为true，循环体被执行。如果为false，循环终止，开始执行循环体后面的语句
3. 执行一次循环后，更新循环控制变量（迭代因子控制循环变量的增减）
4. 再次检测布尔表达式。循环执行上面的过程

---



## 3.7 Foreach 循环结构

###  3.7.1 增强 for 语句

```java
package CH02_JAVAProcessControl;

//增强for
public class XZ03_CirculateStructure7 {
    public static void main(String[] args) {
        //遍历数组中的值
        int[] a = new int[]{10, 20, 30, 40, 50, 60};
        for (int x : a) {
            System.out.println(x);
        }
    }
}
```

增强 for：

- Java5 引入了一种主要用于数组或集合的增强型 for 循环
- 声明语句：声明新的局部变量，该变量的类型必须和数组元素的类型匹配。其作用域限定在循环语句块，其值与此时数组元素的值相等
- 表达式：表达式是要访问的数组名，或者是返回值为数组的方法

---



## 3.8 Break 和 Continue

```java
package CH02_JAVAProcessControl;

//break和continue的区别
public class XZ03_CirculateStructure1_break_continue {
    public static void main(String[] args) {
        int i = 0;
        while (i < 100) {
            i++;
            System.out.print(i + "  ");
            if (i == 30) {
                break;
            }
        }
        System.out.println();
        System.out.println("========================");
        int j = 0;
        while (j < 100) {
            j++;
            if (j % 10 == 0) {
                System.out.println();
                continue;
            }
            System.out.print(j);
        }

    }
}
```

### 3.8.1 break 和 continue 的区别

- **break** 在任何循环语句的主体部分，均可用break控制循环的流程。**break用于强行退出循环**，不执行循环中剩余的语句。（break语句也在switch语句中使用）
- **continue** 语句用在循环语句体中，**用于终止某次循环过程**，即跳过循环体中尚未执行的语句，接着进行下一次是否执行循环的判定

---



## 3.9 go to 关键字

```java
package CH02_JAVAProcessControl;

public class XZ04_GoToKeyWord {
    public static void main(String[] args) {
        // 打印101-159之间所有的质数
        // 质数是指在大于1的自然数中，除了1和它本身以外不再有其他因数的自然数。

        int count = 0;
        outer:
        for (int i = 101; i < 150; i++) {
            for (int j = 2; j < i / 2; j++) {
                if (i % j == 0) {
                    continue outer;
                }
            }
            System.out.print(i + " ");
        }

    }
}
```

go to关键字：

- 关于 go to 关键字 go to 关键字很早就在程序设计语言中出现
- 尽管 go to 仍是 Java 的一个保留字，但并未在语言中得到正式使用；Java 没有go to
- 然而，在 break 和 continue 这两个关键字的身上，我们仍然能看出一些 go to 的影子像是带标签的 break 和continue
- “标签”是指后面跟一个冒号的标识符，例如：label：
- 对 Java 来说唯一用到标签的地方是在循环语句之前。而在循环之前设置标签的唯一理由是：我们希望在其中嵌套另个循环，由于 break 和 continue 关键字通常只中断当前循环，但若随同标签使用，它们就会中断到存在标签的地方

---



## 3.10 循环结构案例

### 3.10.1 二进制转换十进制

```java
package LearnJava.进制转换;

import java.util.Scanner;

public class 二进制转换十进制 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        //先判断有几位数
        //输入数*输入位数减去1的平方
        //转换后数值相加
        //输出最终结果
        System.out.println("请输入二进制数字：");
        int erjinzhi = input.nextInt();

        int shijinzhi = 0, p = 0;
        while (erjinzhi != 0) {
            shijinzhi += ((erjinzhi % 10) * Math.pow(2, p));
            erjinzhi = erjinzhi / 10;
            p++;
        }
        System.out.println(shijinzhi);
    }
}
```

### 3.10.2 十进制转换二进制

```java
package LearnJava.进制转换;

import java.util.Scanner;

public class 十进制转换二进制 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("请输入十进制数字");
        int n = input.nextInt();
        int t = 0;
        //用来记录位数
        int bin = 0;
        //用来记录最后的二进制数
        int r = 0;
        //用来存储余数
        while (n != 0) {
            r = n % 2;
            n = n / 2;
            bin += r * Math.pow(10, t);
            t++;
        }
        System.out.println(bin);
    }
}
```

### 3.10.3 打印 100 以内的奇数与偶数和

```java
package CH02_JAVAProcessControl;

//for循环输出100以内的奇数与偶数和
public class XZ03_CirculateStructure4 {
    public static void main(String[] args) {

        int ji = 0;
        int oh = 0;
        for (int i = 0; i <= 100; i++) {
            if (i % 2 == 0) {
                oh += i;
            } else {
                ji += i;
            }
        }
        System.out.println(ji);
        System.out.println(oh);
        System.out.println(ji + oh);

    }
}
```

### 3.10.4  打印 1-1000 之间能被 5 整除的数，并且每行输出 3 个

```java
package CH02_JAVAProcessControl;

//用while或for循环输出1-1000之间能被5整除的数，并且每行输出3个
public class XZ03_CirculateStructure5 {
    public static void main(String[] args) {

        for (int i = 1; i < 1000; i++) {
            if (i % 5 == 0) {
                System.out.print(i + "\t");

            }
            if (i % (3 * 5) == 0) {
                System.out.println();
            }
        }
    }
}
```

### 3.10.5 打印正反 99 乘法表

```java
package CH02_JAVAProcessControl;

//打印正反99乘法表
public class XZ03_CirculateStructure6 {
    public static void main(String[] args) {

        //      1.我们先打印第一列，这个大家应该都会
        //      2.我们把固定的1再用一个循环包起来
        //      3.去掉重复项，i<=j
        //      4.调整样式

        for (int j = 1; j <= 9; j++) {
            for (int i = 1; i <= j; i++) {
                System.out.print(j + "*" + i + "=" + (j * i) + "\t");
            }
            System.out.println();

        }
        System.out.println("===========================");

        for (int j = 9; j >= 0; j--) {
            for (int i = 1; i <= j; i++) {
                System.out.print(j + "*" + i + "=" + (j * i) + "\t");
            }
            System.out.println();

        }

    }
}
```

### 3.10.6 打印等腰三角形

```java
package CH02_JAVAProcessControl;

//打印三角形
public class XZ03_CirculateStructure8 {
    public static void main(String[] args) {
        // 空白与实体之间的关系  2*i-1
        for (int i = 0; i <= 5; i++) {
            for (int j = 5; j >= i; j--) {
                System.out.print(" ");
            }
            for (int j = 1; j <= 2 * i - 1; j++) {
                System.out.print("*");
            }
            System.out.println();
        }

        System.out.println("===========================");

        for (int i = 1; i <= 5; i++) {
            for (int j = 5; j >= i; j--) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            for (int j = 1; j < i; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

---



# 四、方法

## 4.1 方法的定义

```java
package CH03_JAVAMethod;

import java.util.Scanner;

//方法的定义
public class XZ01_DefinitionOfMethod {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("请输入第一个数字：");
        int x = input.nextInt();
        System.out.println("请输入第二个数字：");
        int y = input.nextInt();
        //      声明变量x和y接收用户输入变量
        int result = sum(x, y);
        //      调用方法获取返回值
        System.out.println("大数是：" + result);
        //        输出返回值
        input.close();
    }

    public static int sum(int x, int y) {
        //      修饰符     返回值类型 方法名（参数类型 参数名）{
        int result = 0;
        //        声明变量返回结果
        if (x == y) {
            return 0;
        }
        if (x > y) {
            result = x;
        } else {
            result = y;
        }
        //        方法体
        return result;
        //      return 返回值；
    }

}
```

Java方法是语句的集合：

- 它们在一起执行一个功能
- 方法是解决一类问题的步骤的有序组合
- 方法包含于类或对象中
- 方法在程序中被创建，在其他地方被引用

设计方法的原则：

- 方法的本意是功能块，就是实现某个功能的语句块的集合
- 我们设计方法的时候，最好保持方法的原子性
- **就是一个方法只完成1个功能，样利于后期代码的扩展。**

### 4.1.2 方法的定义元素

- Java的方法类似于其它语言的函数，是一段用来完成特定功能的代码片段
- 一个方法包括：一个方法头和一个方法体
- 方法头一般有一下内容：
- **修饰符**：修饰符是可选的，告诉编译器如何调用该方法。定义了该方法的访问类型
- **返回值类型**：方法可能会返回值。returnValueType 是方法返回值的数据类型。有些方法执行所需的操作，但没有返回值，returnValueType 就是关键字 void
- **方法名**：是方法的实际名称。方法名和参数表共同构成方法签名
- **参数类型**：参数像是一个占位符。当方法被调用时，传递值给参数。这个值被称为实参或变量。参数列表是指方法的参数类型、顺序和参数的个数。参数是可选的，方法可以不包含任何参数
  - **形式参数**：在方法被调用时用于接收外界输入的数据
  - **实参**：调用方法时实际传给方法的数据
- **方法体**：方法体包含具体的语句，定义该方法的功能

---



## 4.2 方法的重载

```java
package CH03_JAVAMethod;

//方法的重载
public class XZ02_OverloadingOfMethod {
    public static void main(String[] args) {
        //      声明变量x和y接收用户输入变量
        int result = add(10, 20, 30);
        int result2 = add(10, 20);
        double result3 = add(10, 20, 30.6, 40);
        //      方法名相同，根据传递参数数量，类型不同自动判断
        System.out.println("和为：" + result);
        System.out.println("和为：" + result2);
        System.out.println("和为：" + result3);
        //        输出返回值
    }

    public static int add(int x, int y) {
        //      修饰符     返回值类型 方法名（参数类型 参数名）{
        int result = 0;
        //        声明变量返回结果
        result = x + y;
        //        方法体
        return result;
        //      return 返回值；
    }

    public static int add(int x, int y, int z) {
        //      修饰符     返回值类型 方法名（参数类型 参数名）{
        int result = 0;
        //        声明变量返回结果
        result = x + y + z;
        //        方法体
        return result;
        //      return 返回值；
    }

    public static double add(double x, double y, double z, double n) {
        //      修饰符     返回值类型 方法名（参数类型 参数名）{
        double result = 0;
        //        声明变量返回结果
        result = x + y + z + n;
        //        方法体
        return result;
        //      return 返回值；
    }

}
```

> 方法的重载重载就是在一个类中，有相同的函数名称，但形参不同的函数。
>
> 方法名称相同时，编译器会根据调用方法的参数个数、参数类型等去逐个匹配，以选择对应的方法，如果匹配失败，则编译器报错。

### 4.2.1 方法的重载规则

- 方法名称必须相同。
- 参数列表必须不同（个数不同、或类型不同、参数排列顺序不同等）。
- 方法的返回类型可以相同也可以不相同。
- 仅仅返回类型不同不足以成为方法的重载。

---



## 4.3 命令行传参

```java
package CH03_JAVAMethod;

//传参
public class XZ03_ChuanshenOfMethod {
    public static void main(String[] args) {
        for (int i = 0; i < args.length; i++) {
            System.out.println("args[" + i + "]: " + args[i]);
        }
    }
}
```

> 命令行传参有时候你希望运行一个程序时候再传递给它消息。这要靠传递命令行参数 给main( ) 函数实现。

1. 通过cmd窗体编译 java 文件传递参数

2. 编译文件`javac XZ03_ChuanshenOfMethod.java`

3. cd../ 回退到 src 目录下

4. 书写全路径`java CH03_JAVAMethod/XZ03_ChuanshenOfMethod`

5. 加上传递参数`java CH03_JAVAMethod.XZ03_ChuanshenOfMethod XuanZi XuanZiShaer`

   >  !!! 注释可能无法编译，导致编译失败

---



## 4.4 可变参数

```java
package CH03_JAVAMethod;

//可变参数
public class XZ04_VariableParameterOfMethod {
    public static void main(String[] args) {
        printMax(312, 22.2, 3213, 32131);
    }

    public static void printMax(int a, double... numbers) {
        if (numbers.length == 0) {
            System.out.println("No argument passed");
            return;
        }
        double result = numbers[0];
        //排序！
        for (int i = 1; i < numbers.length; i++) {
            if (numbers[i] > result) {
                result = numbers[i];
            }
        }
        System.out.println("The max value is " + result);
    }

}
```

可变参数：

- JDK1.5 开始，Java 支持传递同类型的可变参数给一个方法
- 在方法声明中，在指定参数类型后加一个省略号(...)
- 一个方法中只能指定一个可变参数，它必须是方法的最后一个参数。任何普通的参数必须在它之前声明

---



## 4.5 递归

```java
package CH03_JAVAMethod;

//递归
public class XZ05_RecursionOfMethod {
    public static void main(String[] args) {
        System.out.println(f(25));
    }

    public static long f(long n) {
        if (n == 1) {
            return 1;
        } else {
            return n * f(n - 1);
        }
    }
}
```

递归：

- A方法调用B方法，我们很容易理解
- 递归就是：A方法调用A方法！就是自己调用自己调用
- 递归可以用简单的程序来解决一些复杂的问题。它通常把一个大型复杂的问题层层转化为一个与原问题相似的规模较小的问题来求解，递归策略只需少量的程序就可描述出解题过程所需要的多次重复计算，大大地减少了程序的代码量。递归的能力在于用有限的语句来定义对象的无限集合。
- 递归结构包括两个部分：
  - **递归头**：什么时候不调用自身方法。如果没有头，将陷入死循环
  - **递归体**：什么时候需要调用自身方法

---



# 五、数组

## 5.1 数组的定义

```java
package CH04_JAVAArrays;

//数组的定义
public class XZ01_DefinitionOfArray {
    public static void main(String[] args) {

        int[] nums;
        //        声明数组
        nums = new int[10];
        //        定义数组空间

        nums[0] = 1;
        nums[1] = 2;
        nums[2] = 3;
        nums[3] = 4;
        nums[4] = 5;
        nums[5] = 6;
        nums[6] = 7;
        nums[7] = 8;
        nums[8] = 9;
        nums[9] = 10;
        //        对数组进行赋值
        //        nums[10] = 11;
        //        数组素引超出范围
        int sum = 0;
        for (int i = 0; i < nums.length; i++) {
            sum += nums[i];
        }
        System.out.println("和为：" + sum);

    }
}
```

数组的定义：

- 数组是相同类型数据的有序集合
- 数组描述的是相同类型的若干个数据，按照一定的先后次序排列组合而成
- 其中，每一个数据称作一个数组元素，每个数组元素可以通过一个下标来访问它们

---



## 5.2 数组状态

```java
package CH04_JAVAArrays;

//数组状态
public class XZ02_ArrayState {
    public static void main(String[] args) {
        int[] nums = new int[10];
        nums[0] = 1;
        //        动态状态
        int[] nums2 = {10, 20, 30, 40, 50};
        //        静态状态
        System.out.println(nums[0]);
        System.out.println(nums[1]);
        System.out.println(nums2[0]);
    }
}
```

数组的默认初始化：

- 数组是引用类型，它的元素相当于类的实例变量，因此数组一经分配空间，其中的每个元素也被按照实例变量同样的方式被隐式初始化。

---



## 5.3 数组下标越界

```java
package CH04_JAVAArrays;

//数组下标越界
public class XZ03_ArraySubscriptOutOfBounds {

    public static void main(String[] args) {
        int[] nums = new int[10];

        System.out.println(nums[10]);
        //打印数组下标超过数组存储就会报错： 数组下标越界
    }
}
```

- 数组是相同数据类型(数据类型可以为任意类型)的有序集合
- 数组也是对象。数组元素相当于对象的成员变量
- 数组长度的确定的，不可变的。如果越界，则报错：**ArraylndexOutofBounds**

### 5.3.1 数组的基本特点

- 其长度是确定的。数组一旦被创建，它的大小就是不可以改变的。其元素必须是相同类型,不允许出现混合类型
- 数组中的元素可以是任何数据类型，包括基本类型和引用类型
- 数组变量属引用类型，数组也可以看成是对象，数组中的每个元素相当于该对象的成员变量
- 数组本身就是对象，Java中对象是在堆中的，因此数组无论保存原始类型还是其他对象类型，数组对象本身是在堆中的

---



## 5.4 数组基础案例

```java
package CH04_JAVAArrays;

//数组基础案例
public class XZ04_ArrayBasicCase {
    public static void main(String[] args) {
        int[] nums = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

        System.out.println("=========遍历数组============");
        for (int i = 0; i < nums.length; i++) {
            System.out.print(nums[i] + "\t");
        }
        System.out.println();
        System.out.println("==========遍历数组============");
        for (int num : nums) {
            System.out.print(num + "\t");
        }
        System.out.println();
        System.out.println("==========计算和============");
        int sum = 0;
        for (int i = 0; i < nums.length; i++) {
            sum += nums[i];
        }
        System.out.print("和为：" + sum);
        System.out.println();
        System.out.println("==========计算最大数============");
        int max = nums[0];
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] > max) {
                max = nums[i];
            }
        }
        System.out.print("最大数为：" + max);
        System.out.println();
        System.out.println("==========反转数组============");
        for (int i = 0; i < reverse(nums).length; i++) {
            System.out.print(reverse(nums)[i] + "\t");
        }
    }

    public static int[] reverse(int[] nums) {
        //        反转数组
        int[] result = new int[nums.length];
        for (int i = 0, j = result.length - 1; i < nums.length; i++, j--) {
            result[i] = nums[j];
        }
        return result;
    }

}
```

### 5.4.1 数组插入

```java
package XuanZi.CH08.数组;
//数组插入

import java.util.Arrays;

public class XuanZi06 {
    public static void main(String[] args) {
        int[] lao = {18, 17, 55, 19, 51, 45};
        //老数组
        int num = 52;
        //插入数
        int[] xin = new int[lao.length + 1];
        //新数组长度等于老数组长度加一
        //新数组的i位成语老数组的i位
        System.arraycopy(lao, 0, xin, 0, lao.length);
        xin[lao.length] = num;
        //新数组最后一位等于插入数

        Arrays.sort(xin);
        for (int i = 0; i < xin.length; i++) {
            System.out.println(xin[i]);
            //排序输出
        }

    }
}
```

### 5.4.2 数组合并

```java
package XuanZi.CH08.数组;

public class XUanZi07 {
    public static void main(String[] args) {
        int[] a = new int[]{10, 20, 30};
        int[] b = new int[]{40, 50, 60};
        int[] xin = new int[a.length + b.length];
        int c = 0;
        System.out.print("第一个数组中的元素:");
        for (int i = 0; i < a.length; i++) {
            System.out.print(a[i]);
            if (i < a.length - 1) {
                System.out.print(",");
            }
        }
        System.out.println();
        System.out.print("第二个数组中的元素:");
        for (int i = 0; i < a.length; i++) {
            System.out.print(b[i]);
            if (i < b.length - 1) {
                System.out.print(",");
            }
        }
        System.out.println();
        for (int i = 0; i < xin.length; i++) {
            if (i < a.length) {
                xin[i] = a[i];

            } else {
                xin[i] = b[c];
                c++;
            }

        }
        System.out.print("两个数组合并后:");
        for (int i = 0; i < xin.length; i++) {
            System.out.print(xin[i]);
            if (i < xin.length - 1) {
                System.out.print(",");
            }
        }

        System.out.println();

        System.out.print("逆序后:");
        for (int i = 0; i < xin.length; i++) {

            System.out.print((xin[xin.length - i - 1]));
            if (i < xin.length - 1) {
                System.out.print(",");
            }
        }
    }
}
```

---



## 5.5 多维数组

```java
package CH04_JAVAArrays;

//多维数组
public class XZ05_multidimensionalArray {
    public static void main(String[] args) {
        int[] nums = {1, 2, 3, 4, 5};
        int[][] ages = {{1, 2}, {2, 3}, {3, 4}, {4, 5}};

        for (int i = 0; i < nums.length; i++) {
            System.out.print(nums[i] + "\t");
        }
        System.out.println();
        System.out.println("==========打印多维数组======");
        for (int i = 0; i < ages.length; i++) {
            for (int j = 0; j < ages[i].length; j++) {
                System.out.print(ages[i][j] + "\t");
            }
        }
    }
}
```

> 多维数组可以看成是数组的数组，比如二维数组就是一个特殊的一维数组，其每一个元素都是一个一维数组

---



## 5.6 Arrays 类

```java
package CH04_JAVAArrays;
//Arrays类

import java.util.Arrays;

public class XZ06_ArrayClass {
    public static void main(String[] args) {
        int[] nums = {2, 4, 6, 7, 5};

        Arrays.sort(nums);
        //数组排序
        System.out.println(Arrays.toString(nums));
        //打印数组
        Arrays.fill(nums, 2, 4, 0);
        //          填充数组         起始下标        填充值
        System.out.println(Arrays.toString(nums));

    }
}
```

Arrays 类：
- 数组的工具类`java.util.Arrays`
- 由于数组对象本身并没有什么方法可以供我们调用，但API中提供了一个工具类Arrays供我们使用，从而可以对数据对象进行一些基本的操作
- Arrays类中的方法都是static修饰的静态方法，在使用的时候可以直接使用类名进行调用,而"不用“使用对象来调用（注意：是”不用”而不是“不能”）

### 5.6.1 常用功能

- 给数组赋值：通过`fill`方法
- 对数组排序：通过`sort`方法，按升序
- 比较数组：通过`equals`方法比较数组中元素值是否相等
- 查找数组元素：通过`binarySearch`方法能对排序好的数组进行二分查找法操作

---



## 5.7 冒泡排序

```java
package CH04_JAVAArrays;

import java.util.Arrays;

//冒泡排序
public class XZ07_bubbleSort {
    public static void main(String[] args) {
        // 比较数组中，两个相邻的元素，如果第一个数比第二个数大
        // 我们就交换他们的位置
        // 每一次比较，都会产生出一个最大，或者最小的数字
        // 下一轮则可以少一次排序
        // 依次循环，直到结束
        int[] a = {1, 4, 5, 6, 72, 2, 2, 2, 25, 6, 7};
        int[] sort = sort(a);
        //调用完我们自己写的排序方法以后，返回一个排序后的数组
        System.out.println(Arrays.toString(sort));

    }

    public static int[] sort(int[] array) {
        //临时变量
        int temp = 0;
        //外层循环，判断我们这个要走多少次；
        for (int i = 0; i < array.length - 1; i++) {

            boolean flag = false;//减少没有意义的比较

            //内层循环，比价判断两个数，如果第一个数，比第二个数大，则交换位置
            for (int j = 0; j < array.length - 1 - i; j++) {
                if (array[j + 1] > array[j]) {
                    temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                    flag = true;
                }
            }
            if (!flag) {
                break;
            }
        }
        return array;
    }
}
```

- 冒泡排序无疑是最为出名的排序算法之一，总共有八大排序
- 冒泡的代码还是相当简单的，两层循环，外层冒泡轮数，里层依次比较，江湖中人人尽皆知
- 我们看到嵌套循环，应该立马就可以得出这个算法的时间复杂度为O(n2)

### 5.7.1 冒泡排序口诀

1. 外层循环 n-1   ,控制比较轮数
2. 内层循环 n-1-i ,控制每一轮比较次数
3. 两两比较做交换 ,判断大小交换位置

![冒泡](https://gitee.com/XuanZiShare/xuan-zi-picture/raw/master/Java/202212221417638.gif)

---



# 六、面向对象编程

## 6.1 JAVA 的核心思想就是`OOP`

### 6.1.1 面向过程与面向对象

面向过程思想

- 步骤清晰简单，第一步做什么，第二步做什么……

- 面对过程适合处理一些较为简单的问题

面向对象思想

- 物以类聚，**分类**的思维模式，思考问题首先会解决问题需要哪些分类
- 然后对这些分类进行单独思考。最后，才对某个分类下的细节进行面向过程的思索
- 面向对象适合处理复杂的问题，适合处理需要多人协作的问题

> 对于描述复杂的事物，为了从宏观上把握、从整体上合理分析，我们需要使用面向对象的思路来分析整个系统。但是，具体到微观操作，仍然需要面向过程的思路去处理。

### 6.1.2 面向对象的定义

面向对象编程：(Object-Oriented Programming)；简称`OOP`

面向对象编程的本质就是：**以类的方式组织代码，以对象的组织（封装)数据。**

### 6.1.3 三大特征

- **封装**
- **继承**
- **多态**

### 6.1.4 面向对象的优点

- 与人类的思维习惯一致
- 隐藏信息，提高了程序的可维护性和安全性
- 提高了程序的可重用性
- 易维护，易重用，易拓展，安全性

---



## 6.2 类和对象

### 6.2.1 类与对象的定义

- 类是现实世界或思维世界中的实体在计算机中的反映，它将数据以及这些数据上的操作封装在一起

- 对象是具有类，类型的变量。类和对象是面向对象编程技术中的最基本的概念

### 6.2.2 类与对象的关系

- 类是对象的抽象，而对象是类的具体实例
- 类是抽象的，不占用内存，而对象是具体的，占用存储空间
- 类是用于创建对象的蓝图，它是一个定义包括在特定类型的对象中的方法和变量的软件模板

> 类是对象的类型，对象是类的实例

---



## 6.3 创建对象与初始化

```java
package CH05_JAVAObjectOriented;

//类与对象的创建
public class XZ01_Student {
    // 学生类
    String name;
    // 默认值 null
    int age;
    // 默认值 0

    public void study() {
        System.out.println(this.name + "在学习");
        // this 代表当前类的属性

    }
}
```

```java
package CH05_JAVAObjectOriented;

//一个项目应该只存在一个 Main 方法
public class XZ01_Main {
    public static void main(String[] args) {
        //类：抽象的，实例化
        //类实例化后会返回一个自己的对象！
        XZ01_Student xiaoMing = new XZ01_Student();
        //				使用new关键字创建对象
        System.out.println(xiaoMing.name);
        System.out.println(xiaoMing.age);
        xiaoMing.study();
        XZ01_Student xiaoHong = new XZ01_Student();
        System.out.println("------------------------");
        xiaoHong.name = "小红";
       	// 对属性进行赋值
        xiaoHong.age = 16;
        System.out.println(xiaoHong.name);
        System.out.println(xiaoHong.age);
        xiaoHong.study();
        //xiaoHong,xiaoHong就是一个Student类的具体实例！

    }
}
```

---



## 6.4 构造器

类中的构造器也称为构造方法，是在进行创建对象的时候必须要调用的。并且构造器有以下俩个特点：

1. 必须和类的名字相同
2. 必须没有返回类型，也不能写void

```java
package CH05_JAVAObjectOriented;

public class XZ02_Constructors {
    //一个类即使什么都不写，它也会存在一个方法
    //显示的定义构造器

    String name;

    public XZ02_Constructors(String name) {
        //有参构造：一旦定义了有参构造，无参就必须显示定义
        //只要定义了有参构造就也定义个无参构造
        this.name = name;
    }

    public XZ02_Constructors() {
        this.name = "玄子";
    }
}
```

```java
package CH05_JAVAObjectOriented;

public class XZ02_Main {
    public static void main(String[] args) {
        XZ02_Constructors constructors = new XZ02_Constructors("玉玉诏");
        System.out.println(constructors.name);
        // 这里看不懂可尝试 Debug 一下
    }
}
```

### 6.4.1 快捷生成

> 快捷键： Alt + Instant 
>
> 笔记本用户根据自己机型考虑加上 Shift 
>
> 即同时按下 Alt + Shift + Instant 

---



## 6.5 封装

---



## 6.6 继承

---



## 6.7 多态

---



## 6.8 抽象类和接口

---



# 七、异常

---

# 八、集合框架

---

# 九、常用类

---

# 十、IO流

---

# 十一、多线程

---

# 十二、综合案例

---

>  暂停更新 玄子:2022年12月21日
