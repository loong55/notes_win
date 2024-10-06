# 基本语法

```c
#include <stdio.h>   // 头文件包含

#define PI 3.14159    // 宏定义

// 函数声明
int add(int a, int b);

int main() {         // 主函数
    // 变量声明
    int num1, num2, sum;

    // 用户输入
    printf("Enter two integers: ");
    scanf("%d %d", &num1, &num2);

    // 函数调用
    sum = add(num1, num2);

    // 输出结果
    printf("Sum: %d\n", sum);

    return 0;        // 返回 0 表示程序成功执行
}

// 函数定义
int add(int a, int b) {
    return a + b;
}
```

**标识符**：变量、函数、数组等的名字，由字母、数字和下划线组成，第一个字符不能是数字。

**常量**：固定值，在程序执行期间不会改变。

```c
const int MAX = 100;  // 整型常量
const float PI = 3.14;  // 浮点型常量
const char NEWLINE = '\n';  // 字符常量
```

**字符串字面量**:由双引号括起来的字符序列,末尾会自动添加一个空字符 **\0**。

```c
char greeting[] = "Hello, World!";
```

**关键字**:不能作为常量名、变量名

```c
int	char for ...
```

**空格**:让编译器能识别语句中的某个元素（比如 int）在哪里结束，下一个元素在哪里开始。

```c
int age;
```

```
fruit = apples + oranges;   // 获取水果的总数
//fruit 和 =，或者 = 和 apples 之间的空格字符不是必需的，但为了增强可读性
```

# 数据类型

| 序号 | 类型与描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | **基本数据类型** 它们是算术类型，包括整型（int）、字符型（char）、浮点型（float）和双精度浮点型（double）。 |
| 2    | **枚举类型：** 它们也是算术类型，被用来定义在程序中只能赋予其一定的离散整数值的变量。 |
| 3    | **void 类型：** 类型说明符 *void* 表示没有值的数据类型，通常用于函数返回值。 |
| 4    | **派生类型：** 包括数组类型、指针类型和结构体类型。          |

**整数类型**

存储大小：

==一个字节（Byte）==是计算机数据的基本单位，它等于==8比特（bits）==。每个比特可以是0或1，因此一个字节可以表示256（2的8次方）种不同的状态(0~255)

4个字节等于 4 × 8 比特 = 32 比特(0~2^32-1)

在数据存储和传输中，通常使用以下单位来表示字节的大小：

- 1 千字节（KB） = 1,024 字节
- 1 兆字节（MB） = 1,024 KB = 1,048,576 字节
- 1 吉字节（GB） = 1,024 MB = 1,073,741,824 字节

| 类型          | 存储大小                            | 值范围                                               |
| :------------ | :---------------------------------- | :--------------------------------------------------- |
| ==char==      | ==1 字节==                          | ==-128 到 127 或 0 到 255==                          |
| unsigned char | 1 字节                              | 0 到 255                                             |
| signed char   | 1 字节                              | -128 到 127                                          |
| ==int==       | ==2(32位系统）或 4 字节(64位系统)== | -32,768 到 32,767 或 -2,147,483,648 到 2,147,483,647 |
| unsigned int  | 2 或 4 字节                         | 0 到 65,535 或 0 到 4,294,967,295                    |
| short         | 2 字节                              | -32,768 到 32,767                                    |

```c
//获取储存大小
#include <stdio.h>
int main()
{
   printf("int 存储大小 : %d \n", sizeof(int));  
   return 0;
}
```

```c
int 存储大小 : 4 
```

**浮点类型**

| 类型        | 存储大小   | 值范围                 | 精度           |
| :---------- | :--------- | :--------------------- | :------------- |
| ==float==   | ==4 字节== | 1.2E-38 到 3.4E+38     | ==6 位有效位== |
| double      | 8 字节     | 2.3E-308 到 1.7E+308   | 15 位有效位    |
| long double | 16 字节    | 3.4E-4932 到 1.1E+4932 | 19 位有效位    |

**void类型**

**函数返回为空**： **void exit (int status);**

**函数参数为空**： **int rand(void);**

**指针指向 void**：类型为 void * 的指针代表对象的地址，而不是类型。
例如，内存分配函数 **void \*malloc( size_t size );** 
返回指向 void 的指针，可以转换为任何数据类型。



**类型转换**

隐式类型转换

```c
int i = 10;
float f = 3.14;
double d = i + f; // 隐式将int类型转换为double类型
```

显式类型转换

```c
double d = 3.14159;
int i = (int)d; // 显式将double类型转换为int类型
```

# 变量

程序可操作的存储区的名称，数据类型决定了变量存储的大小和布局

变量定义

```c
int age;
float salary;
char grade;
int *ptr;
int    i, j, k;
```

变量初始化

```c
int x = 10;         // 整型变量 x 初始化为 10
float pi = 3.14;    // 浮点型变量 pi 初始化为 3.14
char ch = 'A';      // 字符型变量 ch 初始化为字符 'A'
int d = 3, f = 5;           // 定义并初始化 d 和 f
byte z = 22;                // 定义并初始化 z
```

**全局变量**：函数外部定义的变量，全局起作用，默认初始值为零，程序结束释放内存

```c
int globalVar = 10; // 这是一个全局变量

void function() {
    // 在这个函数内部可以访问 globalVar
}

int main() {
    // 在 main 函数内部也可以访问 globalVar
    return 0;
}
```

**静态变量：**变量声明前加上`static`关键字来定义，静态变量的值在函数调用之间保持不变，默认初始值为零，具有程序级别的生命周期

定义在函数外部时，它具有全局作用域，但是它的链接属性是内部的，这意味着它只能在本源文件内可见。

定义在函数内部时，它仅在函数内部可见，但是它的生命周期是整个程序的执行过程，即它只在程序开始执行时分配一次内存，并且在程序执行期间不会再次分配和释放。

静态全局变量：

```c
static int staticGlobalVar = 20; // 这是一个具有文件作用域的静态全局变量

void function() {
    // 在这个函数内部可以访问 staticGlobalVar
}

int main() {
    // 在 main 函数内部也可以访问 staticGlobalVar
    return 0;
}

```

静态局部变量:

```c
void function() {
    static int staticLocalVar = 30; // 这是一个静态局部变量
    // 每次调用function时，staticLocalVar的值都会保持上一次调用后的值
}

int main() {
    function(); // staticLocalVar 被初始化为 30
    function(); // staticLocalVar 仍然保持上次的值，不会再次初始化
    return 0;
}

```

**局部变量**：在函数内部定义的非静态变量，不会自动初始化为默认值，函数解释自动释放内存

**总结：**全局变量和静态变量的默认值为 **0**，字符型变量的默认值为 **\0**，指针变量的默认值为 NULL，而局部变量没有默认值，其初始值是未定义的。



#### 变量声明

变量声明向编译器保证变量以指定的类型和名称存在，这样编译器在不需要知道变量完整细节的情况下也能继续进一步的编译。

变量声明只在编译时有它的意义，在程序连接时编译器需要实际的变量声明。

```c
extern int i; //声明，不是定义
int i; //声明，也是定义
```

**int a** 在声明的时候就已经建立了存储空间

**extern int a** 不需要建立存储空间的，其中变量 **a** 可以在别的文件中定义的

**extern 	外部**

```c
#include <stdio.h>
 
// 函数外定义变量 x 和 y
int x;
int y;
int addtwonum()
{
    // 函数内声明变量 x 和 y 为外部变量
    extern int x;
    extern int y;
    // 给外部变量（全局变量）x 和 y 赋值
    x = 1;
    y = 2;
    return x+y;
}
 
int main()
{
    int result;
    // 调用函数 addtwonum
    result = addtwonum();
    
    printf("result 为: %d",result);
    return 0;
}
```

```c
result 为: 3
```

##### extern 多文件变量调用

addtwonum.c 文件代码：

```c
#include <stdio.h>
/*外部变量声明*/
extern int x ;
extern int y ;
int addtwonum()
{
    return x+y;
}
```

test.c 文件代码：

```c
#include <stdio.h>
  
/*定义两个全局变量*/
int x=1;
int y=2;
int addtwonum();
int main(void)
{
    int result;
    result = addtwonum();
    printf("result 为: %d\n",result);
    return 0;
}
```

编译并执行

```shell
$ gcc addtwonum.c test.c -o main
$ ./main
result 为: 3
```



**左值（Lvalues）和右值（Rvalues）**

**左值（lvalue）：**可以被赋值的值，左值可以出现在赋值号的左边或右边。

```c
int g = 20;		//g为左值，20为右值
```

**右值（rvalue）：**右值是不能对其进行赋值的表达式，右值只能出现在赋值号的右边

```
10 = 20;//不是一个有效的语句，会生成编译时错误
```

# 常量















































# 链表

数组和链表都可以存放数据，数组的格式如下

| a\[ \] | data |
| ------ | ---- |
| a\[0\] | 1    |
| a\[1\] | 2    |
| a\[2\] | 3    |

```text
然而对于数组来说，删除数组中指定为位置的元素，插入一个元素显得复杂且麻烦。 
人们想出利用一个结构 来使各种操作变得更加方便，这个结构便是链表。
```

## 链表各成分理解

### 1、头文件

头文件需要包含

```c
#include<stdio.h> 
#include<stdlib.h>
```

### 2、定义结构体

需要包含 数据域 和 指针域

数据域：可以是各种数据类型组合一起

指针域：通过指针来使各节点连接在一起，从而快速实现各种操作

```c
typedef struct student
{
    char name[100];
    int age;
    student *next; //也可以规范一点写成struct student *next 
};
```

这就是很简单的单链表的一个节点，可以表示为

![](pic_win/v2-27ec4a67096e1b214c78fcac934093b4_b.jpg)

在做下一步操作之前，先理解两个操作

### 1、指针访问结构体中的数据。

当定义一个指针指向结构体时，例如：

```c
student stu1={"hjw",18}; //自定义结构体内容
student *p = &stu1;      //指针指向结构体stu1的地址
操作 p->name 或者 p->age 为访问结构体中的数据，若 p->age=19 ，即直接修改了stu1的数据age为19。
```

代码如下

```c
typedef struct student
{
    char name[100];
    int age;
    student *next; //也可以规范一点写成struct student *next 
}student;


int main(void)
{
    student stu1={"hjw",18};
    student *p = &stu1;
    printf("%s,%d\n",p->name,p->age);
    p->age=19;
    printf("%d\n",p->age);
    return 0; 
}
```

运行结果：

```c
hjw,18
19

--------------------------------
Process exited after 0.07111 seconds with return value 0
请按任意键继续. . .
```

### 2、分配储存空间

要想存入一个数据，则需要利用malloc函数来开辟新的空间。

此时你并不知道需要开辟多大的空间。可以直接利用[sizeof函数](https://www.zhihu.com/search?q=sizeof%E5%87%BD%E6%95%B0&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A365087630%7D)来确定你所需要的空间大小。

```text
注意：使用malloc函数返回的是void*的指针，所以还需要强制转换为你所需要的类型。
若如上文我们所写的一样，需要强制转换成student*的类型，则如下所示
student *p1;
p1 = (student *)malloc(sizeof(student));
表示：指针 p1 指向 结构体student大小的 内存区域
```

### 3、创立第二个链表节点，并尝试连接起来

由第二点的操作，我们可以定义 两个指针 指向 两个结构体的内存区域 ，并通过这两个指针来进行 数据的修改等操作

```c
先定义两个指针，并指向两个结构体的内存区域。

    student *p1,*p2;
    p1 = (student *)malloc(sizeof(student));
    p2 = (student *)malloc(sizeof(student));
再通过这两个指针进行数据的填充

由于发现给了下标的数组不好赋值，我们可以利用指针字符串的方式定义名字

把char name[100] 修改为 const char *name
即把结构体改为了

typedef struct student
{
    const char *name;
    int age;
    student *next; //也可以规范一点写成struct student *next 
}student;
进行数据填充：

    p1->name = "hjw";
    p1->age= 18 ;
    p2->name = "wjh";
    p2->age = 81;

检测一下是否填充成功  
    printf("%s %d\n",p1->name,p1->age);
    printf("%s %d\n",p2->name,p2->age);


运行结果为
hjw 18
wjh 81

--------------------------------
Process exited after 0.05025 seconds with return value 0
请按任意键继续. . .
```

此时用图表示为

![](pic_win/v2-d2796738514f24a143043bbde68442c4_b.jpg)

### 再把这两个链表连接在一起

![](pic_win/v2-8006ea534e70c111157a4bf66bc8e7b2_b.jpg)

要想做更多操作，则需要把 头链表 以及 尾结点 给记录起来。

```c
student *head;
head = p1;
把头链表 p1 的位置记录给 head 。
p2->next = NULL;
把尾结点给标记为NULL，即进行操作时，可以通过这个终止操作。
```

表示为：

![](pic_win/v2-9ea1ed3753e22bf15aaa3af762975e07_b.jpg)

### 利用循环语句，实现多链表的连接

```c
直接上源代码：
#include<stdio.h>
#include<stdlib.h>

typedef struct student
{
    const char *name;
    int age;
    student *next; //也可以规范一点写成struct student *next 
}student;


int main(void)
{
    student *p;
    student *head;
    student *p1,*p2;
    head = 0;
    for(int i=0;i<=5;i++)
    {
        p1 = (student *)malloc(sizeof(student));//p1指向开辟一个内存
        p1->age = i;                            //数据的插入
        if(head == 0)                           //用if条件句判断head是否指向头链表
        {
            head = p1;
            p2 = p1;
        }
        else                                   //head已经标记头链表了
        {
            p2->next = p1;            //p2用来标记上一次的内存，把上一个内存的next指向下一个 
            p2 = p1;                  //p2为下次的连接做准备
        }
        
        /*
if(head == 0): 这个条件检查链表是否为空。在C语言中，0通常表示NULL，
这里head == 0就是检查head指针是否为NULL，即链表是否为空。
如果链表为空（即head是NULL）：
head = p1;: 将新创建的节点p1设置为链表的头部。
p2 = p1;: 同时将p2也指向这个新节点。p2用于跟踪链表的最后一个节点。
如果链表不为空（即head不是NULL）：
p2->next = p1;: 将当前链表的最后一个节点（p2指向的节点）的next指针设置为新的节点p1，
这样就把新节点添加到了链表的末尾。
p2 = p1;: 然后将p2更新为指向新的最后一个节点，即新添加的节点p1。
        */
    }
    p1->next = NULL;
    p = head;                         //p指向头链表，方便操作
    while(p != NULL)
    {
        printf("%d ",p->age);
        p = p->next ;
    }
    return 0; 
}
运行结果：

0 1 2 3 4 5
--------------------------------
Process exited after 0.03945 seconds with return value 0
请按任意键继续. . .
```

## 输入数据并连接链表

```c
输入数据：

    p1 = (student *)malloc(sizeof(student));
    scanf("%s",p1->name);
    scanf("%d",&p1->age)


再设置循环语句，连接链表

    if(head == 0)
    {
        head = p1;
        p2 = p1;
    }
    else
    {
        p2->next = p1;
        p2 = p1;
    }
标记一个变量，使输入数据可以结束循环。

直接上代码：
#include<stdio.h>
#include<stdlib.h>



typedef struct student
{
    char name[20];//改为数组
    int age;
    student *next; //也可以规范一点写成struct student *next 
}student;


int main(void)
{
    student *p;
    student *head;
    student *p1,*p2;
    head = 0;
    char q;



    while(1)
    {
        printf("continue?(y/n)\n");
        scanf("%c",&q);


        if(q=='y')
        {       


            p1 = (student *)malloc(sizeof(student));


            printf("your name:");
            scanf("%s",p1->name);
            printf("age:");
            scanf("%d",&p1->age);
            getchar();


            if(head == 0)
            {
                head = p1;
                p2 = p1 ;
            }
            else
            {
                p2->next = p1;
                p2 = p1;
            }
        }
        else
        {
            break;
        }


    }


    p1->next = NULL;
    p = head;
    printf("%s:%d",p->name,p->age);
    p=p->next;
    printf("%s:%d",p->name,p->age);
    return 0; 
}
```

## 删除链表

```c
三个节点，第一个节点直接连接到第三个节点上，释放第二个链表的内存。 
释放内存的函数为free（）。
free(p2)
```


[原理图](https://www.zhihu.com/search?q=%E5%8E%9F%E7%90%86%E5%9B%BE&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22article%22%2C%22sourceId%22%3A365087630%7D)：

![](pic_win/v2-232bceab16652bdff084fe6697d54804_b.jpg)

\--------------------------------------------------------------------------------------------------------------------------

![](pic_win/v2-b3834de16fb132c58b9df37ede58d5d1_b.jpg)

___

![](pic_win/v2-a87d06f73a56963b93001e30cf24753d_b.jpg)

```c
//删除整个列表
void freeList(Node **head) {
    Node *current = *head;
    Node *next;

    while (current != NULL) {
        next = current->next; // 保存下一个节点的地址
        free(current);        // 释放当前节点
        current = next;       // 移动到下一个节点
    }

    *head = NULL; // 将头指针设置为NULL，避免野指针
}
```



## 查找链表（删除特定的链表）

```text
利用while等循环语句，遍历链表直至查到所需要的数据位置。
```

### 1.通过学号或者年龄等数据查询

```c
例如通过年龄来查询
int a；
scanf("%d",&a);
while(p->age != a )  //当年龄符合要求时，退出循环
{
    p = p->next;   //p循环一次都会向下移动一个链表
}
怎么查询多个同一年龄的人呢？可以改进为：
int a;
scanf("%d",&a);
while(p->age != a || p != NULL)
{
    if(p->age == a)
    {
        printf("%s:%d",p->name,p->age);
    }
    p = p->next;
}
```

### 2.通过数组中的元素查询，例如名字

```text
可以借助关于 字符串 的函数来实现。例如strcmp（）
```

> 字符串比较函数strcmp的比较，两个字符串自左向右逐个字符相比(按ASCII值大小相比较)，直到出现不同的字符或遇’\\0’为止。基本形式为strcmp(str1,str2)，若str1=str2,则返回零，若str1str2，则返回正数。  

```c
char a[20];
scanf("%s",a);
while(!strcmp(a,p->name) || p != NULL)
{
    if(!strcmp(a,p->name))
    {
        printf("%s:%d",p->name,p->age);
    }
    p = p->next;
}
```

