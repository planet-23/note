### IDEA快捷键

> sout：System.out.println()
> 	main（或 psvm）：public static void main(String[] args)
> 	array.for ：for each 语句
> 	Alt+? 代码提示
> 	Ctr+? 单行注释
> 	Ctr+Shift+? 多行注释
> 	Alt+Enter 代码语法错误解决
> 	Alt+Insert 插入代码：setter getter等
> 	End：光标移到行尾
> 	Home：光标移到行首
> 	Ctrl+Alt+L：格式化代码
> 	Ctrl+]：快速跳转至诸如{}围起来的代码块的结尾处
> 	Ctrl+[：快速跳转至诸如{}围起来的代码块的开头处
> 	Ctrl+向左箭头：将光标移至前一个单词
> 	Ctrl+向右箭头：将光标移至后一个单词
> 	Ctrl+向上箭头：向上滚动一行
> 	Ctrl+向下箭头：向下滚动一行
> 	Ctrl+W：选中整个单词
> 	Ctrl+Shift+U：切换大小写

### 注意事项

> \1. 字符串不是基本类型，而是引用类型。
>
> \2. 浮点型可能只是一个近似值，并非精确的值。
>
> \3. 数据范围与字节数不一定相关，例如float数据范围比long更加广泛，但是float是4字节，long是8字节。
>
> \4. 浮点数当中默认类型是double。如果一定要使用float类型，需要加上一个后缀F。
>
> 如果是整数，默认为int类型，如果一定要使用long类型，需要加上一个后缀L。推荐使用大写字母后缀。
>
> \5. byte short int 可以发生数学运算，但会首先提升为int类型，然后再计算，因此计算结果应该进行强制类型转换为 byte short int
>
> \6. boolean类型不能进行数据类型转换



### Java内存划分

#### Java内存区域（运行时数据区域）和内存模型（JMM）

Java 内存区域和内存模型是不一样的东西，内存区域是指 Jvm 运行时将数据分区域存储，强调对内存空间的划分。

而内存模型（Java Memory Model，简称 JMM ）是定义了线程和主内存之间的抽象关系，即 JMM 定义了 JVM 在计算机内存(RAM)中的工作方式，如果我们要想深入了解Java并发编程，就要先理解好Java内存模型。



#### java执行过程

首先Java源代码文件(.java后缀)会被Java编译器编译为字节码文件(.class后缀)，然后由JVM中的类加载器加载各个类的字节码文件，加载完毕之后，交由JVM执行引擎执行。在整个程序执行过程中，JVM会用一段空间来存储程序执行期间需要用到的数据和相关信息，这段空间一般被称作为Runtime Data Area（运行时数据区），也就是我们常说的JVM内存。因此，在Java中我们常常说到的内存管理就是针对这段空间进行管理（如何分配和回收内存空间）。

#### Java运行时数据区域

![å¾æèªãç åºé«æã](https://upload-images.jianshu.io/upload_images/14923529-c0cbbccaa6858ca1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 寄存器：JVM内部虚拟寄存器，存取速度非常快，程序不可控制。
- 栈:保存局部变量的值：包括1.基本数据类型的值。2.保存类的实例，即堆区对象的引用（指针）。3.保存加载方法时的帧。
- 堆：用来存放动态产生的数据，比如new出来的对象。注意创建出来的对象只包含属于各自的成员变量，并不包括成员方法。因为同一个类拥有各自的成员变量，存储在堆中的不同位置，但是同一个类不同实例的他们共享该类的方法，并不是每创建一个对象就把成员方法复制一次。
- 常量池：JVM为每个加载的类型维护一个常量池，常量池是这个类型用到的常量的集合。包括直接常量(基本类型，String)和对其他类型、方法、字段的符号引用(1)。池中的数据和数组一样通过索引访问。由于常量池包含了一个类型所有的对其他类型、方法、字段的符号引用，所以常量池在Java的动态链接中起了核心作用。常量池存在于方法区中，而方法区存在于堆中。

![img](https://img-blog.csdn.net/20161110172317173)

> 1.一个Java文件，只要有main入口方法，我们就认为这是一个Java程序，可以单独编译运行。 
> 2.无论是普通类型的变量还是引用类型的变量(俗称实例)，都可以作为局部变量，他们都可以出现在栈中。只不过普通类型的变量在栈中直接保存它所对应的值，而引用类型的变量保存的是一个指向堆区的指针，通过这个指针，就可以找到这个实例在堆区对应的对象。因此，普通类型变量只在栈区占用一块内存，而引用类型变量要在栈区和堆区各占一块内存。 
> 3.在方法的参数传递中，基本数据类型，String类是按值传递，即拷贝了一个副本！引用数据类型是按引用传递，即把栈中的地址传入！

- 以上就是Java程序运行时内存分配的大致情况。其实也没什么，掌握了思想就很简单了。无非就是两种类型的变量：基本类型和引用类型。二者作为局部变量，都放在栈中，基本类型直接在栈中保存值，引用类型只保存一个指向堆区的指针，真正的对象在堆里。作为参数时基本类型就直接传值，引用类型传指针。

#### 小结

1.分清什么是实例什么是对象。Class a= new Class();此时a叫实例，而不能说a是对象。实例在栈中，对象在堆中，操作实例实际上是通过实例的指针间接操作对象。多个实例可以指向同一个对象。 
2.栈中的数据和堆中的数据销毁并不是同步的。方法一旦结束，栈中的局部变量立即销毁，但是堆中对象不一定销毁。因为可能有其他变量也指向了这个对象，直到栈中没有变量指向堆中的对象时，它才销毁，而且还不是马上销毁，要等垃圾回收扫描时才可以被销毁。 
3.以上的栈、堆、代码段、数据段等等都是相对于应用程序而言的。每一个应用程序都对应唯一的一个JVM实例，每一个JVM实例都有自己的内存区域，互不影响。并且这些内存区域是所有线程共享的。这里提到的栈和堆都是整体上的概念，这些堆栈还可以细分。 
4.类的成员变量在不同对象中各不相同，都有自己的存储空间(成员变量在堆中的对象中)。而类的方法却是该类的所有对象共享的，只有一套，对象使用方法的时候方法才被压入栈，方法不使用则不占用内存。 
以上分析只涉及了栈和堆，还有一个非常重要的内存区域：常量池，这个地方往往出现一些莫名其妙的问题。常量池是干嘛的上边已经说明了，也没必要理解多么深刻，只要记住它维护了一个已加载类的常量就可以了。接下来结合一些例子说明常量池的特性。

- 基本类型和基本类型的包装类。基本类型有：byte、short、char、int、long、boolean。基本类型的包装类分别是：Byte、Short、Character、Integer、Long、Boolean。注意区分大小写。二者的区别是：基本类型体现在程序中是普通变量，基本类型的包装类是类，体现在程序中是引用变量。因此二者在内存中的存储位置不同：基本类型存储在栈中，而基本类型包装类存储在堆中。上边提到的这些包装类都实现了常量池技术，另外两种浮点数类型的包装类则没有实现。另外，String类型也实现了常量池技术。



### 常用类

#### ArrayList

数组的缺点：创建后长度不可以改变，但ArrayList长度可以改变

import java.util.ArrayList;

// ArrayList有一个尖括号<>代表泛型，尖括号里是什么类型，就只能添加什么类型

// 泛型：也就是装在集合当中的所有元素，全都是统一的什么类型

// 泛型只能是引用类型，不能是基本类型

// ArrayList直接打印不是地址值，而是内容，因为经过toString()处理了

~~~java
	public class ArrayListTest {
		public static void main(String[] args) {
			/*
			* add(E e) 向集合中添加元素，参数类型和泛型一致
			* get(int index) 根据索引获得元素,索引从0开始
			* remove(int index) 删除并返回被删除的元素
			* size() 集合中元素的个数
			* */
			ArrayList<String> list = new ArrayList<>();
			System.out.println(list);
			list.add("赵丽颖");
			list.add("古力娜扎");
			list.add("马尔扎哈");
			System.out.println(list);
			int num = list.size();
			System.out.println(num);
			System.out.println(list.get(2));
			System.out.println(list.remove(1));
			System.out.println(list.get(1));
			for (int i = 0; i < list.size(); i++) {
				System.out.println(list.get(i));
			}
		}
	}
	 //基本类型如果要使用ArrayList，要使用相应的包装类
        /*
        * byte Byte
        * short Short
        * int Integer
        * long Long
        * float Float
        * double Double
        * char Character
        * boolean Boolean
        * */
//从JDK1.5开始，支持自动装箱（基本类型-->包装类），拆箱
        ArrayList<Integer> list = new ArrayList<>();
        list.add(499);
        list.add(0);
        System.out.println(list);
	ArrayList作为参数和返回值
	public static ArrayList<Integer> function1(ArrayList<Integer> list){
        ArrayList<Integer> listNew = new ArrayList<>();
        for (int i = 0; i < list.size(); i++) {
            if (list.get(i) % 2 == 0){
                listNew.add(list.get(i));
            }
        }
        return listNew;
    }
~~~



#### String

java.lang.String

程序中所有的双引号的字符串，都是String类的对象，就算没有new照样也是

字符串的内容永不可变

~~~java
//String的三种构造函数，底层是通过byte[]方式实现的
        // 空内容的字符串
        String str1 = new String();
        System.out.println("第一个 " + str1);

        char[] charArray = {'a','b','c'};
        String str2 = new String(charArray);
        System.out.println("第二个 " + str2);

        byte[] byteArray = {97,98,99};
        String str3 = new String(byteArray);
        System.out.println("第三个 " + str3);
        //直接创建
        String str4 = "hello";
        System.out.println(str4);
	//字符串常量池：直接双引号创建的字符串就在字符串常量池中,但new出来的不在字符串常量池
        str1 = "abc";
        str2 = "abc";
        char[] charArray1 = {'a','b','c'};
        str3 = new String(charArray1);
        System.out.println(str1 == str2); //true
        System.out.println(str1 == str3); //false
        System.out.println(str2 == str3); //false
~~~

对于引用类型来说，==进行的地址值得比较

对内容进行比较

```java
		//public boolean equals(Object anObject)
		System.out.println(str1.equals(str3)); //true
		String str4 = null;
		str4.equals("abc");//报错，空指针异常
```

推荐使用 "abc".equals(str4);

```java
		//忽略大小写比较内容
		System.out.println("ABc".equalsIgnoreCase("abc")); //true
```

字符串获取的相关方法：

```java
		public int length() //字符串长度
		public String concat(String str) // 将当前字符串和str拼接
		public char charAt(int index) //获得指定索引index位置的单个字符
		public int indexOf(String str) // 查找str在当前字符串中首次出现出现的位置，如果没有返回-1
```

字符串截取：

```java
		public String substring(int beginIndex)  //默认取到结尾
		public String substring(int beginIndex, int endIndex) //指定开头结尾 左闭右开[begin,end)
```

字符串转换：

将当前字符串拆分为字符数组作为返回值

public char[] toCharArray()

获得当前字符串底层的字节数组

public byte[] getBytes()

将所有出现的老字符串替换为新字符串(old,new)

```java
			public String replace(CharSequence target, CharSequence replacement)
			"how do you do".replace("do","**"); 
```

字符串切割

```java
		//public String[] split(String regex)
		String str5 = "aaa,bbb,ccc";
                String[] array = str5.split(",");
```

split方法的参数其实是一个正则表达式，如果按照英文句点"."来切分，需要使用"\\."



#### static关键字

如果一个成员变量使用了static关键字，那么该变量就不再属于对象自己，而是属于所在的类

static String room;

如果一个成员方法使用了static关键字，那么该方法就变成了类方法，使用类名称访问（也可以使用对象访问，不推荐）

static static void methodStatic()

成员方法可以访问成员变量和静态变量

但静态方法不能直接访问非静态变量，因为内存中先有的静态内容，后有的非静态内容

静态方法中不能使用this关键字

静态代码块

static {//内容}

当第一次使用到本类时，静态代码块只执行唯一的一次

静态内容总是优先于非静态，所以静态代码块比构造函数先执行

用途：用来一次性地对静态成员变量进行赋值



#### Arrays 数组工具类

// java.util.Arrays 里面提供了大量的静态方法。用来实现数组的相关操作，是一个与数组相关的工具类

public static String toString(int[] a)

将参数数组编程字符串，返回默认格式 [元素1,元素2 ...]

public static void sort(int[] a)

按照默认升序对数组进行排序



#### Math 工具类

java.lang.Math 里面提供了大量的静态方法，完成数学相关运算

向上取整：

Math.ceil(11.3)的值是12 ; Math.ceil.(-11.6)的结果是-11;

向下取整：

Math.floor(11.6)的结果就是11 ;Math.floor(-11.4);的结果就是-12

四舍五入：

Math.round(11.5);也就是 Math.floor(11.5+0.5)= Math.floor(12)=12;

同理: Math.round(-11.5)= Math.floor(-11.5+0.5)=Math.floor(-11.0)= -11;