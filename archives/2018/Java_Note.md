# Java学习笔记 - 数据类型与运算符<上>
---

## 2.1 注释 
为了方便程序的阅读，Java语言允许程序员在程序中写上一些说明性的文字，用来提高程序的可读性，这些文字性的说明就称为注释。 注释不会出现在字节码文件中，即Java编译器编译时会跳过注释语句。 在Java中根据注释的功能不同，主要分为单行注释、多行注释和文档注释。

* 单行注释：  使用“//”开头，“//”后面的单行内容均为注释。

* 多行注释：   以“/*”开头以“*/”结尾，在“/*”和“*/”之间的内容为注释，我们也可以使用多行注释作为行内注释。但是在使用时要注意，多行注释不能嵌套使用。

* 文档注释：   以“/**”开头以“*/”结尾，注释中包含一些说明性的文字及一些JavaDoc标签(后期写项目时，可以生成项目的API)

【示例2-1】认识Java的三种注释类型

    /**  
     * Welcome类（我是文档注释）  
     * @author 高淇  
     * @version 1.0  
     */  
    public class Welcome {  
    	//我是单行注释  
    	public static void main(String[] args/*我是行内注释 */) {  
    		System.out.println("Hello World!");  
    	}  
    	/*  
    	 	我是多行注释！  
    	 	我是多行注释！  
    	 */  
    }

## 2.2 标识符

标识符是用来给变量、类、方法以及包进行命名的，如Welcome、main、System、age、name、gender等。标识符需要遵守一定的规则：

标识符必须以**字母**、**下划线_**、**美元符号$**开头。  

标识符其它部分可以是**字母**、**下划线“_”**、**美元符“$”**和**数字**的任意组合。

Java 标识符**大小写敏感**，且**长度无限制**。

标识符不可以是Java的关键字。

###标识符的使用规范

**表示类名的标识符**：每个单词的首字母大写，如Man, GoodMan

**表示方法和变量的标识符**：第一个单词小写，从第二个单词开始首字母大写，我们称之为“**驼峰原则**”，如eat(), eatFood()

    【注意】：Java不采用通常语言使用的ASCII字符集，而是采用Unicode这样标准的国际字符集。因此，这里字母的含义不仅仅是英文，还包括汉字等等。但是不建议大家使用汉字来定义标识符！

【示例2-2】合法的标识符

    int  a = 3;
    int  _123 = 3;
    int  $12aa = 3;
    int  变量1 = 55;  //合法，但是不建议使用中文命名的标识符

【示例2-3】不合法的标识符

    int  1a = 3;   //不能用数字开头
    int  a# = 3;   //不能包含#这样的特殊字符
    int  int = 3;  //不能使用关键字

课堂测试代码：

    /**
     * 测试标识符的用法
     * @author 高淇
     *
     */
    public class TestIdentifer {
         
        //能力是练出来的，不是看书看出来的。对于初学者来说，再简单的代码也一定要敲一下！
        public static void main(String[] args) {
            int  a123 = 1;
            //int  123abc = 2;        //数字不能开头
            int  $a = 3;
            int  _abc = 4;
            //int  #abc = 5;
             
            int  年龄 = 18;        //可以使用汉字，但是一般不建议
             
            //int class = 2;        //关键字不能作为标识符
             
        }
    }

## 2.3 Java中的关键字/保留字

Java关键字是Java语言保留供内部使用的，如class用于定义类。 关键字也可以称为保留字，它们的意思是一样的，我们不能使用关键字作为变量名或方法名。

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-uys7{border-color:inherit;text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-uys7" colspan="6">表2-1 Java中的关键字/保留字<br></th>
  </tr>
  <tr>
    <td class="tg-uys7">abstract</td>
    <td class="tg-uys7">assert</td>
    <td class="tg-uys7">boolean</td>
    <td class="tg-uys7">break</td>
    <td class="tg-uys7">byte</td>
    <td class="tg-uys7">case</td>
  </tr>
  <tr>
    <td class="tg-c3ow">catch</td>
    <td class="tg-c3ow">char</td>
    <td class="tg-c3ow">class</td>
    <td class="tg-c3ow">const</td>
    <td class="tg-c3ow">continue</td>
    <td class="tg-c3ow">default</td>
  </tr>
  <tr>
    <td class="tg-c3ow">do</td>
    <td class="tg-c3ow">double</td>
    <td class="tg-c3ow">else</td>
    <td class="tg-c3ow">extends</td>
    <td class="tg-c3ow">final</td>
    <td class="tg-c3ow">finally</td>
  </tr>
  <tr>
    <td class="tg-c3ow">float</td>
    <td class="tg-c3ow">for</td>
    <td class="tg-c3ow">goto</td>
    <td class="tg-c3ow">if</td>
    <td class="tg-c3ow">implements</td>
    <td class="tg-c3ow">import</td>
  </tr>
  <tr>
    <td class="tg-c3ow">instanceof</td>
    <td class="tg-c3ow">int</td>
    <td class="tg-c3ow">interface</td>
    <td class="tg-c3ow">long</td>
    <td class="tg-c3ow">native</td>
    <td class="tg-c3ow">new</td>
  </tr>
  <tr>
    <td class="tg-c3ow">null</td>
    <td class="tg-c3ow">package</td>
    <td class="tg-c3ow">private</td>
    <td class="tg-c3ow">protected</td>
    <td class="tg-c3ow">public</td>
    <td class="tg-c3ow">return</td>
  </tr>
  <tr>
    <td class="tg-c3ow">short</td>
    <td class="tg-c3ow">static</td>
    <td class="tg-c3ow">strictfp</td>
    <td class="tg-c3ow">super</td>
    <td class="tg-c3ow">switch</td>
    <td class="tg-c3ow">synchronized</td>
  </tr>
  <tr>
    <td class="tg-c3ow">this</td>
    <td class="tg-c3ow">throw</td>
    <td class="tg-c3ow">throws</td>
    <td class="tg-c3ow">transient</td>
    <td class="tg-c3ow">try</td>
    <td class="tg-c3ow">void</td>
  </tr>
  <tr>
    <td class="tg-c3ow">volatile</td>
    <td class="tg-c3ow">while</td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
    <td class="tg-c3ow"></td>
  </tr>
</table>

## 2.4.1 变量的本质

变量本质上就是代表一个”可操作的存储空间”，空间位置是确定的，但是里面放置什么值不确定。我们可通过变量名来访问“对应的存储空间”，从而操纵这个“存储空间”存储的值。

Java是一种强类型语言，每个变量都必须声明其数据类型。变量的数据类型决定了变量占据存储空间的大小。 比如，int a=3; 表示a变量的空间大小为4个字节。

变量作为程序中最基本的存储单元，其要素包括变量名，变量类型和作用域。变量在使用前必须对其声明, 只有在变量声明以后，才能为其分配相应长度的存储空间。

### 变量的声明

格式为：

    type  varName [=value][,varName[=value]...]; 
    //[]中的内容为可选项，即可有可无
    数据类型  变量名  [=初始值] [,变量名  [=初始值]…];

【示例2-4】 声明变量：

    double  salary;
    long  earthPopulation;
    int  age;

不同数据类型的常量会在内存中分配不同的空间，如图2-1所示。

1.png

图2-1 声明变量的内存示意图

**注意事项**

* 每个变量都有类型，类型可以是基本类型，也可以是引用类型。

* 变量名必须是合法的标识符

* 变量声明是一条完整的语句，因此每一个声明都必须以分号结束

【示例2-5】在一行中声明多个变量

    int  i ,j; // 两个变量的数据类型都是int

>**老鸟建议**
    
>不提倡这种"一行声明多个变量"风格，逐一声明每一个变量可以提高程序可读性。

【示例2-6】可以将变量的声明和初始化放在同一行中

    int  age = 18;    
    double  e = 2.718281828;

## 2.4.2 变量的分类

  从整体上可将变量划分为局部变量、成员变量(也称为实例变量)和静态变量。

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-s6z2{text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-s6z2" colspan="4">表2-2 局部变量、成员变量、静态变量的区别</th>
  </tr>
  <tr>
    <td class="tg-s6z2">类型</td>
    <td class="tg-s6z2">声明位置</td>
    <td class="tg-s6z2">从属于</td>
    <td class="tg-s6z2">生命周期</td>
  </tr>
  <tr>
    <td class="tg-s6z2">局部变量</td>
    <td class="tg-s6z2">方法或语句块内部</td>
    <td class="tg-s6z2">方法/语句块</td>
    <td class="tg-s6z2">从声明位置开始，直到方法或语句块执行完毕，局部变量消失</td>
  </tr>
  <tr>
    <td class="tg-s6z2">成员变量<br>(实例变量)<br></td>
    <td class="tg-s6z2">类内部，方法外部</td>
    <td class="tg-s6z2">对象</td>
    <td class="tg-s6z2">对象创建，成员变量也跟着创建。对象消失，成员变量也跟着消失</td>
  </tr>
  <tr>
    <td class="tg-s6z2">静态变量</td>
    <td class="tg-s6z2">(类变量)</td>
    <td class="tg-s6z2">类内部，static修饰类</td>
    <td class="tg-s6z2">类被加载，静态变量就有效；类被卸载，静态变量消失</td>
  </tr>
</table>

>**老鸟建议**

>成员变量和静态变量不是目前重点，不要过多纠结理解与否。我们学习面向对象时，再重点讲解成员变量和静态变量

### 局部变量(local  variable)

方法或语句块内部定义的变量。生命周期是从声明位置开始到到方法或语句块执行完毕为止。局部变量在使用前必须先声明、初始化(赋初值)再使用。

【示例2-7】局部变量

    public void test() {
       int i;
       int j = i+5 ; // 编译出错，变量i还未被初始化 
    } 
     
    public void test() {
       int i;
       i=10;
       int j = i+5 ; // 编译正确
    }

### 成员变量（也叫实例变量  member variable）

方法外部、类的内部定义的变量。从属于对象，生命周期伴随对象始终。如果不自行初始化，它会自动初始化成该类型的默认初始值。

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-s6z2{text-align:center}
.tg .tg-baqh{text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-s6z2" colspan="2">表2-3 实例变量的默认初始值</th>
  </tr>
  <tr>
    <td class="tg-s6z2">数据类型</td>
    <td class="tg-s6z2">实始值</td>
  </tr>
  <tr>
    <td class="tg-s6z2">int</td>
    <td class="tg-s6z2">0</td>
  </tr>
  <tr>
    <td class="tg-s6z2">double</td>
    <td class="tg-s6z2">0.0</td>
  </tr>
  <tr>
    <td class="tg-s6z2">char</td>
    <td class="tg-s6z2">‘\u0000’</td>
  </tr>
  <tr>
    <td class="tg-baqh">boolean</td>
    <td class="tg-baqh">false</td>
  </tr>
</table>

【示例2-8】实例变量的声明

    public class Test {
    	int i;
    }

### 静态变量（类变量 static variable）

使用static定义。 从属于类，生命周期伴随类始终，从类加载到卸载。 (注：讲完内存分析后我们再深入！先放一放这个概念！)如果不自行初始化，与成员变量相同会自动初始化成该类型的默认初始值，如表 2-3所示。

课堂练习1：变量的声明并赋值

    public class LocalVariableTest {
      public static void main(String[ ] args) {
          boolean flag = true;  // 声明boolean型变量并赋值
           char c1, c2;   // 声明char型变量
           c1 = '\u0041';   // 为char型变量赋值
          c2 = 'B';   // 为char型变量赋值
          int x;   // 声明int型变量
          x = 9;  //为int型变量赋值  
           int y = x;  // 声明并初始化int型变量
           float f = 3.15f;   // 声明float型变量并赋值
          double d = 3.1415926;  //声明double型变量并赋值
             }
    }
课堂代码：

    /**
     * 测试变量
     * 
     * @author 高淇
     *
     */
    public class TestVariable {
    
        int a;            //成员变量, 从属于对象； 成员变量会自动被初始化
        static  int  size;   //静态变量，从属于类
        
        public static void main(String[] args) {
    
            {
                int age;        //局部变量，从属于语句块；
                age = 18;
            }
            
            int salary = 3000;    //局部变量，从属于方法
    
            int gao = 13;
            System.out.println(gao);
    
            int i;
        //    int j = i + 5; // 编译出错，变量i还未被初始化
            
        }
    }

## 2.5 常量(Constant)

常量通常指的是一个固定的值，例如：1、2、3、’a’、’b’、true、false、”helloWorld”等。

在Java语言中，主要是利用关键字final来定义一个常量。 常量一旦被初始化后不能再更改其值。

声明格式为：

    final  type  varName = value;

【示例2-9】常量的声明及使用

    public class TestConstants {
    	public static void main(String[] args) {
    		final double PI = 3.14;
    		// PI = 3.15; //编译错误，不能再被赋值！ 
    		double r = 4;
    		double area = PI * r * r;
    		double circle = 2 * PI * r;
    		System.out.println("area = " + area);
    		System.out.println("circle = " + circle);
    	}
    }
为了更好的区分和表述，一般将1、2、3、’a’、’b’、true、false、”helloWorld”等称为**字面常量**，而使用final修饰的PI等称为**符号常量**。

>**老鸟建议**

>* 变量和常量命名规范（规范是程序员的基本准则，不规范会直接损害你的个人形象）：

>* 所有变量、方法、类名：见名知意

>* 类成员变量：首字母小写和驼峰原则:  monthSalary

>* 局部变量：首字母小写和驼峰原则

>* 常量：大写字母和下划线：MAX_VALUE

>* 类名：首字母大写和驼峰原则:  Man, GoodMan

>* 方法名：首字母小写和驼峰原则: run(), runRun()