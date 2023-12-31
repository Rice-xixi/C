# 第一个程序-HelloWorld

## 1-Hello World的历史

学习编程语言的第一件事,自然是先从标准的输入输出开始学习.作为学习各个编程语言编写的第一个程序,Hello World也有一个小历史：

Hello World的起源可以追溯到1972年，当时贝尔实验室的著名研究员Brian Kernighan(布莱恩·克尼哈尔)在他撰写的“B语言教程与指导 (Tutorial Introduction to the Language B)”中首次使用了这个程序。这是目前已知最早的在计算机著作中将Hello和World一起使用的记录。之后，在1978年，他在他和Dennis Ritchie(丹尼斯·里奇)合作撰写的C语言圣经“The C Programming Language”中，延用了“Hello,World”句式，作为开篇第一个程序。虽然之后几乎没能流传下来这个最初的格式，但从此用Hello World向世界打招呼成为惯例。

## 2-程序的编写

```c
#include <stdio.h>	//引入头文件

int main()	//程序主函数
{
    printf("Hello World");	//输出字符串
    return 0;	//程序结束
}
```

## 3-代码解析

```c
#include <stdio.h>
```

首先带#号的命令我们叫做`预处理命令`,预处理命令是不需要加分号(;)的,后面的<stdio.h>是一个以.h的文件,在C语言中我们把.h结尾的文件称为`头文件(或库文件)`.c结尾的叫`源文件`...所以第一句的含义就是引入<stdio.h>这个头文件

-   头(库)文件:	头文件是主要存放函数声明与宏定义的地方,其作用是导入到源文件中,给源文件调用的作用.
-   源文件:    放的是程序的源代码文件所以叫源文件.

关于函数的声明与宏定义,等学到了后面大家就都会有所了解.而stdio.h这个文件是编写了关于`标准输入输出函数的头文件`,所以我们需要通过他来调用输出函数printf...
另外#include 后面也是可以跟圆括号()的,到底放哪一种也是有规范的:

-   圆括号():	一般是引入一些自己编写的库文件(从源文件同一目录下查找库文件)
-   尖括号<>:    主要用来包含编译器内部自带的库文件

常见的库文件如下:

-   stdio.h	**标准输入输出(standard input & output)**
-   string.h      **主要是一些操作字符串的函数**
-   math.h       **一些常用的数学运算函数**
-   time.h        **各种操作日期和时间的函数**
-   limits.h      **整型数据类型的取值范围**
-   float.h      **浮点型数据类型的取值范围**

具体函数等大家学到了后面再去查找与使用...

```c
int main()
{
    //代码块(函数体)
}
```

首先是 int ,这个词是一个关键字(系统保留拥有其特殊作用的一个词)也代表了整型这个数据类型,而main()这样的格式我们称为函数,mian是函数名,括号的含义我们先卖个关子.main意为主要,所以这句话意思就是一个返回值为整型的主函数,在C语言底层代码中已经写好了,程序开始运行时会先找到main函数并执行里面的代码,所以可以说main函数是程序的入口,是不是一下子就可以理解为什么被称作主函数了呢!!!

-   关键字:        关键字就是设计者在设计此语言时使用的一些词,都有带有其特定的含义,通常都说有32个关键字,C99,C11标准中有新增
-   数据类型:     就是描述一个数据的类型,无非就是整数,浮点数(小数),指针...

接着后面是一个大括号(`{}`)大括号中就是函数具体的实现方法啦.

```c
printf("Hello World");
```

知道的人肯定知道 :) print的意思是打印,也就是输出,这个函数是来自上面引入的<stdio.h>,没有这个头文件,我们的代码会报错哦!
printf函数的作用就是输出括号里面的值,当然想要输出字符串,我们就需要写在双引号中(`" "`),这是规定,但如果是想输出数字就没有这个规定

-   字符串: 一个`字母`,`数字`,`特殊符号`我们都叫字符(可参考ASCII码),那么一串字符我们当然就叫字符串咯,另外如果想输出一个字符我们就约定好放在单引号中哟(`' '`)!

```c
return 0;
```

来到了代码块的最后一句**return**了,也没什么其他意思就是前面写的int,需要一个整型的返回值,我们返回一个0(虽然可以写任何值,但不建议这么做,一般用于检查程序错误才会返回负数),执行完return 0,main函数结束 程序也就结束了...

至此我们学会了C语言的第一个程序,虽然说的东西不少可能有点啰嗦,但也不需要记住,有个了解即可,自己也可以试着输出一些其他的值,理工科不动手就不算学会,快去试试吧,你一定可以!!!

