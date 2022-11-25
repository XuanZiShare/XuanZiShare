# 玄子JAVA基础笔记



## 编写第一个JAVA代码

```java
package CH01_JAVABase;

//hange The World!
public class XZ01_ChangeTheWorld {
    public static void main(String[] args) {

        System.out.println("Change The World!");
        //Change The World!
    }
}
```

| 语句                                        | 说明               | 快捷语句  |
| ------------------------------------------- | ------------------ | --------- |
| public static void main(String[] args) {  } | Main函数程序主入口 | main/psvm |
| System.out.println();                       | 输出语句           | sout      |

---



## JAVA八大基本数据类型

```java
package CH01_JAVABase;

//八大数据类型
public class XZ02_DataType {
    public static void main(String[] args) {

        int num1 = 1;
        byte num2 = 1;
        short num3 = 1;
        long num4 = 1L;
        //整数型
        double num5 = 1.1;
        float num6 = 1f;
        //浮点型
        char ch = 'a';
        //单字符
        boolean is = false;
        //布尔型

        //八大基本数据类型

        String string = "hello world";
        //引用型，不属于基本数据类型

        System.out.println("num1:" + num1);
        System.out.println("num2:" + num2);
        System.out.println("num3:" + num3);
        System.out.println("num4:" + num4);
        System.out.println("num5:" + num5);
        System.out.println("num6:" + num6);
        System.out.println("ch:" + ch);
        System.out.println("is:" + is);
        System.out.println("string:" + string);
    }

}
```

---



## 数据类型转换

```java
package CH01_JAVABase;

//数据类型转换
public class XZ03_TypeConversion {
    public static void main(String[] args) {

        int a = 1;
        double b = a;
        System.out.println(b);
        //隐式数据类型转换，自动转换

        char c = 'a';
        int d = c;
        System.out.println(d);
        //显式数据类型转换转换变量前加 (转换类型)


        System.out.println("================");
        char e = 'a';
        int f = c + 1;
        System.out.println(f);
        System.out.println((char) f);


    }
}
```

注意点：

1. 不能对布尔值进行转换
2. 不能把对象类型转换为不相干的类型
3. 在把高容量转换到低容量的时候，强制转换
4. 转换的时候可能存在内存溢出，或者精度问题！

---



## 注释

```java
package CH01_JAVABase;

//注释
public class XZ04_Annotate {
    public static void main(String[] args) {
        //System.out.println(1);

        //单行注释 只能注释一行

        //被注释掉的代码不会执行

        /*
        System.out.println(1);
        System.out.println(2);
        System.out.println(3);
         */

        /*
        多行
        注释
         */

        /**
         *JavaDoc
         *文档注释
         */
    }

    /**
     * @author XuanZi  (作者)
     */
    public void test() {

    }
}
```

> Javadoc命令是用来生成自己API文档的
> JavaAPI帮助文档：https://docs.oracle.com/en/java/javase/
> Java8API帮助文档：https://docs.oracle.com/javase/8/docs/api/index.html

参数信息

| 参数     | 描述                      |
| -------- | ------------------------- |
| @author  | 作者名                    |
| @version | 版本号                    |
| @since   | 指明需要最早使用的jdk版本 |
| @param   | 参数名                    |
| @return  | 返回值情况                |
| @throws  | 异常抛出情况              |

---



## 变量

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

-  变量是什么：
  - 就是可以变化的量
  - Java是一种强类型语言，每个变量都必须声明其类型
  - Java变量是程序中最基本的存储单元，其要素包括变量名，变量类型和作用域
- 注意事项：
  - 每个变量都有类型，类型可以是基本类型，也可以是引用类型
  -  变量名必须是合法的标识符
  - 变量声明是一条完整的语句，因此每一个声明都必须以分号结束

---

## 常量

```java
package CH01_JAVABase;

//常量
public class XZ06_Constant {
    //      final 数据类型 常量名 = 值；
    public static final double PI = 3.14;
    //修饰符，不存在先后顺序
    public static void main(String[] args) {
        System.out.println(PI);
    }
}
```

- 常量（Constant)：
  - 初始化(initialization)后不能再改变值！不会变动的值。
  - 所谓常量可以理解成一种特殊的变量，它的值被设定后，在程序运行过程中不允许被改变。
  - 常量名一般使用大写字符。

---



## 运算符

```java
package CH01_JAVABase;

//运算符
public class XZ07_OperationalCharacter {
    public static void main(String[] args) {
        int num1 = 1;
        int a = 10;
        int b = 20;
        double num2 = 2.5;
        char A = 'A';
        char B = 'B';
        System.out.println("=========赋值运算符===========");
        System.out.println(num1 - num2);
        System.out.println(a += b);
        System.out.println(a);
        //自身改变
        // =     +=    -=    *=    /=    %=
        // 赋值   加等  减等   乘等   除等  余等
        //赋值运算符
        System.out.println("=======算数运算符=============");
        System.out.println(num1++);// 1
        // mum1 + 1   上一句输出后才+1   2
        // 1 + mum1   下一句输出前就+1   3
        System.out.println(++num1);// 3
        //  +    -   *  /   %   ++   --
        //  加   减  乘  除  余  自增  自减
        //算数运算符
        System.out.println("============比较运算符============");
        System.out.println(num1 <= num2);
        //  >     <     >=       <=      !=     ==
        // 大于   小于  大于等于  小于等于  不等于  等等于
        //比较运算符
        System.out.println("===========逻辑运算符===============");
        System.out.println(num1 > num2 || num2 > num1);
        //两个条件一个为真就返回true
        //如果第一个条件就为假直接返回false，不再判断第二个条件
        System.out.println(num1 > num2 && num2 > num1);
        //两个条件均为真才返回true
        System.out.println(!(num1 > num2 && num2 > num1));
        //条件结果结果取反
        //  &&  ||  !
        //  与  或  非
        //逻辑运算符
        System.out.println("============位逻辑运算符==============");
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
//        ~B = 1111 0010   1为0 0为1

        System.out.println(2 << 3);
//        -------二进制---------
//        0000 0000  0
//        0000 0001  1
//        0000 0010  2
//        0000 0011  3
//        0000 0100  4
//        0000 1000  8
//        0001 0000  16
        //  &   |   ^   ~               <<      >>
        //  与  或  非  异或(按位取反)   左移(*)  右移(/)
        //位逻辑运算符
        System.out.println("===========条件运算符==============");
        int score = 60;
        String type = score >= 60 ? "及格" : "不及格";
        System.out.println(type);
        //  ?   :
        //× ? y : z
        //如果x==true，则结果为y，否则结果为z
        System.out.println("===========算数方法===========");
        System.out.println("Math.pow(2, 3) = " + Math.pow(2, 3));
        System.out.println("Math.pow(3, 2) = " + Math.pow(3, 2));
        //Math.方法
        System.out.println("===========字符串连接符  +  String==========");
        System.out.println("" + 10 + 20);
        System.out.println(10 + 20 + "");
        //String写在前后的区别
        System.out.println("" + (10 + 20));
        //()加强优先级

    }
}
```

- 算数运算符

| 符号 | 描述 |
| :--- | ---- |
| +    | 加   |
| -    | 减   |
| *    | 乘   |
| /    | 除   |
| %    | 余   |
| ++   | 自增 |
| --   | 自减 |

- 赋值运算符

| 符号 | 描述 |
| ---- | ---- |
| =    | 赋值 |
| +=   | 加等 |
| -=   | 减等 |
| *=   | 乘等 |
| /=   | 除等 |
| %=   | 余等 |

- 比较运算符

| 符号 | 描述     |
| ---- | -------- |
| >    | 大于     |
| <    | 小于     |
| >=   | 大于等于 |
| <=   | 小于等于 |
| !=   | 不等于   |
| ==   | 等等于   |

- 逻辑运算符

| 符号 | 描述 |
| ---- | ---- |
| &&   | 与   |
| \|\| | 或   |
| !    | 非   |

- 位逻辑运算符

| 符号 | 描述           |
| ---- | -------------- |
| &    | 与             |
| \|   | 或             |
| ^    | 非             |
| ~    | 异或(按位取反) |
| <<   | 左移(*)        |
| >>   | 右移(/)        |

- 条件运算符

| 符号  | 描述           |
| ----- | -------------- |
| ?   : | 如果为true那么 |

---



## 转义符

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

注意:

1. 区分，斜杠:"/" 与 反斜杠:"\" ,此处不可互换

2. \xhh 十六进制转义不限制字符个数 '\x000000000000F' == '\xF'

---



## 命名规范

```java
package CH01_JAVABase;

//命名规范
public class XZ09_NamingSpecification {
    public static void main(String[] args) {
//		Java 所有的组成部分都需要名字。类名、变量名以及方法名都被称为标识符。
        String name;
        int num;
        double value;
        boolean is;

        String 玄子 = "XuanZi";

        //尽量使用英语单词作为标识符

        //常用命名法
        String studentName = "玄子";
        //驼峰命名法：以小写字母开头，第二个及以后单词首字母大写
        String StudentName = "玄子";
        //帕斯卡命名法：以大写字母开头，第二个及以后单词首字母大写
    }
}
```

- 标识符命名规范:
  - 所有标识符应具有实际意义，尽量不要使用 a、b 这样的无意义命名
  - 所有的标识符都应该以字母（A-Z或者a-z），美元符（$）、或者下划线（_）开始
  - 首字符之后可以是字母（A-Z或者a-z），美元符（$）、下划线（_）或数字的任何字符组合
  - 不能使用关键字作为变量名或方法名
  - 识符是大小写敏感的
  - 合法标识符举例：age、$salary、_value、_1_value
  - 非法标识符举例：123abc、-salary、#abc
  - 可以使用中文命名，但是一般不建议这样去使用，也不建议使用拼音，很Low

- 常用命名法
  - 所有变量、方法、类名：见名知意，具有实际意义
  - 类成员变量：驼峰命名法：studentName
  - 局部变量：驼峰命名法：studentAge
  - 常量：以大写字母命名，下划线拼接：MAX_VALUE
  - 类名：帕斯卡命名法：StudentName
  - 方法名：帕斯卡命名法：StudentAge()
    - 所有方法都带有()

---



## 包机制

```java
package CH01_JAVABase;

//包机制
public class XZ10_PackageMechanism {
    public static void main(String[] args) {
//        为了更好地组织类，Java提供了包机制，用于区别类名的命名空间。
//        包语句的语法格式为：
//        package pkg1[. pkg2[. pkg3...]];

//        一般利用公司域名倒置作为包名；com.XuanZiShare.www
//        为了能够使用某一个包的成员，我们需要在Java程序中明确导入该包。使用“import”语句可完成此功能
//        import package1[.package2...].(classname|*);
//        *通配符  所有

    }
}
```

---



>  玄子2022年11月26日