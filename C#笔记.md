# C#教程

C# 是一个简单的、现代的、通用的、面向对象的编程语言，它是由微软（Microsoft）开发的。

本教程将告诉您基础的 C# 编程，同时将向您讲解 C# 编程语言相关的各种先进理念。

## 编译/执行 C# 程序

菜鸟教程提供了在线的 C# 在线编译环境，您只需进行简单的点击动作，即可在高端的服务器上体验真实的编程经验。这是完全免费的在线工具。

```c#
using System;
namespace HelloWorldApplication
{
    /* 类名为 HelloWorld */
    class HelloWorld
    {
        /* main函数 */
        static void Main(string[] args)
        {
            /* 我的第一个 C# 程序 */
            Console.WriteLine("Hello World!");
            Console.ReadKey();
        }
    }
}
```

# C# 简介

C# 是一个现代的、通用的、面向对象的编程语言，它是由微软（Microsoft）开发的，由 Ecma 和 ISO 核准认可的。

C# 是由 Anders Hejlsberg 和他的团队在 .Net 框架开发期间开发的。

C# 是专为公共语言基础结构（CLI）设计的。CLI 由可执行代码和运行时环境组成，允许在不同的计算机平台和体系结构上使用各种高级语言。

下面列出了 C# 成为一种广泛应用的专业语言的原因：

- 现代的、通用的编程语言。
- 面向对象。
- 面向组件。
- 容易学习。
- 结构化语言。
- 它产生高效率的程序。
- 它可以在多种计算机平台上编译。
- .Net 框架的一部分。

## C# 强大的编程功能

虽然 C# 的构想十分接近于传统高级语言 C 和 C++，是一门面向对象的编程语言，但是它与 Java 非常相似，有许多强大的编程功能，因此得到广大程序员的青睐。

下面列出 C# 一些重要的功能：

- 布尔条件（Boolean Conditions）
- 自动垃圾回收（Automatic Garbage Collection）
- 标准库（Standard Library）
- 组件版本（Assembly Versioning）
- 属性（Properties）和事件（Events）
- 委托（Delegates）和事件管理（Events Management）
- 易于使用的泛型（Generics）
- 索引器（Indexers）
- 条件编译（Conditional Compilation）
- 简单的多线程（Multithreading）
- LINQ 和 Lambda 表达式
- 集成 Windows

# C#基本语法

C# 是一种面向对象的编程语言。在面向对象的程序设计方法中，程序由各种相互交互的对象组成。相同种类的对象通常具有相同的类型，或者说，是在相同的 class 中。

例如，以 Rectangle（矩形）对象为例。它具有 length 和 width 属性。根据设计，它可能需要接受这些属性值、计算面积和显示细节。

让我们来看看一个 Rectangle（矩形）类的实现，并借此讨论 C# 的基本语法：

```c#
using System;
namespace RectangleApplication
{
    class Rectangle
    {
        // 成员变量
        double length;
        double width;
        public void Acceptdetails()
        {
            length = 4.5;    
            width = 3.5;
        }
        public double GetArea()
        {
            return length * width;
        }
        public void Display()
        {
            Console.WriteLine("Length: {0}", length);
            Console.WriteLine("Width: {0}", width);
            Console.WriteLine("Area: {0}", GetArea());
        }
    }
    
    class ExecuteRectangle
    {
        static void Main(string[] args)
        {
            Rectangle r = new Rectangle();
            r.Acceptdetails();
            r.Display();
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
Length: 4.5
Width: 3.5
Area: 15.75
```

## *using* 关键字

在任何 C# 程序中的第一条语句都是：

```
using System;
```

**using** 关键字用于在程序中包含命名空间。一个程序可以包含多个 using 语句。

## *class* 关键字

**class** 关键字用于声明一个类。

## C# 中的注释

注释是用于解释代码。编译器会忽略注释的条目。在 C# 程序中，多行注释以 **/\*** 开始，并以字符 ***/** 终止，如下所示：

```
/* 这个程序演示
C# 的注释
使用 */
```

单行注释是用 **//** 符号表示。例如：

```
// 这一行是注释 
```

## 成员变量

变量是类的属性或数据成员，用于存储数据。在上面的程序中，*Rectangle* 类有两个成员变量，名为 *length* 和 *width*。

## 成员函数

函数是一系列执行指定任务的语句。类的成员函数是在类内声明的。我们举例的类 Rectangle 包含了三个成员函数： *AcceptDetails*、*GetArea* 和 *Display*。

## 实例化一个类

在上面的程序中，类 *ExecuteRectangle* 是一个包含 *Main()* 方法和实例化 *Rectangle* 类的类。

## 标识符

标识符是用来识别类、变量、函数或任何其它用户定义的项目。在 C# 中，类的命名必须遵循如下基本规则：

- 标识符必须以字母、下划线或 **@** 开头，后面可以跟一系列的字母、数字（ 0 - 9 ）、下划线（ _ ）、@。
- 标识符中的第一个字符不能是数字。
- 标识符必须不包含任何嵌入的空格或符号，比如 ? - +! # % ^ & * ( ) [ ] { } . ; : " ' / \。
- 标识符不能是 C# 关键字。除非它们有一个 @ 前缀。 例如，@if 是有效的标识符，但 if 不是，因为 if 是关键字。
- 标识符必须区分大小写。大写字母和小写字母被认为是不同的字母。
- 不能与C#的类库名称相同。

## C# 关键字

关键字是 C# 编译器预定义的保留字。这些关键字不能用作标识符，但是，如果您想使用这些关键字作为标识符，可以在关键字前面加上 @ 字符作为前缀。

在 C# 中，有些关键字在代码的上下文中有特殊的意义，如 get 和 set，这些被称为上下文关键字（contextual keywords）。

下表列出了 C# 中的保留关键字（Reserved Keywords）和上下文关键字（Contextual Keywords）：

| **保留关键字**   |           |           |            |                        |                       |                |
| ---------------- | --------- | --------- | ---------- | ---------------------- | --------------------- | -------------- |
| abstract         | as        | base      | bool       | break                  | byte                  | case           |
| catch            | char      | checked   | class      | const                  | continue              | decimal        |
| default          | delegate  | do        | double     | else                   | enum                  | event          |
| explicit         | extern    | false     | finally    | fixed                  | float                 | for            |
| foreach          | goto      | if        | implicit   | in                     | in (generic modifier) | int            |
| interface        | internal  | is        | lock       | long                   | namespace             | new            |
| null             | object    | operator  | out        | out (generic modifier) | override              | params         |
| private          | protected | public    | readonly   | ref                    | return                | sbyte          |
| sealed           | short     | sizeof    | stackalloc | static                 | string                | struct         |
| switch           | this      | throw     | true       | try                    | typeof                | uint           |
| ulong            | unchecked | unsafe    | ushort     | using                  | virtual               | void           |
| volatile         | while     |           |            |                        |                       |                |
| **上下文关键字** |           |           |            |                        |                       |                |
| add              | alias     | ascending | descending | dynamic                | from                  | get            |
| global           | group     | into      | join       | let                    | orderby               | partial (type) |
| partial (method) | remove    | select    | set        |                        |                       |                |

## 顶级语句（Top-Level Statements）

在 C# 9.0 版本中，引入了顶级语句（Top-Level Statements）的概念，这是一种新的编程范式，允许开发者在文件的顶层直接编写语句，而不需要将它们封装在方法或类中。

**特点：**

- **无需类或方法**：顶级语句允许你直接在文件的顶层编写代码，无需定义类或方法。
- **文件作为入口点**：包含顶级语句的文件被视为程序的入口点，类似于 C# 之前的 `Main` 方法。
- **自动 `Main` 方法**：编译器会自动生成一个 `Main` 方法，并将顶级语句作为 `Main` 方法的主体。
- **支持局部函数**：尽管不需要定义类，但顶级语句的文件中仍然可以定义局部函数。
- **更好的可读性**：对于简单的脚本或工具，顶级语句提供了更好的可读性和简洁性。
- **适用于小型项目**：顶级语句非常适合小型项目或脚本，可以快速编写和运行代码。
- **与现有代码兼容**：顶级语句可以与现有的 C# 代码库一起使用，不会影响现有代码。

**传统 C# 代码** - 在使用顶级语句之前，你必须像这样编写一个 C# 程序：

```c#
using System;

namespace MyApp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, World!");
        }
    }
}
```

**使用顶级语句的 C# 代码** - 使用顶级语句，可以简化为：

```c#
using System;

Console.WriteLine("Hello, World!");
```

顶级语句支持所有常见的 C# 语法，包括声明变量、定义方法、处理异常等。

```
using System;
using System.Linq;

// 顶级语句中的变量声明
int number = 42;
string message = "The answer to life, the universe, and everything is";

// 输出变量
Console.WriteLine($"{message} {number}.");

// 定义和调用方法
int Add(int a, int b) => a + b;
Console.WriteLine($"Sum of 1 and 2 is {Add(1, 2)}.");

// 使用 LINQ
var numbers = new[] { 1, 2, 3, 4, 5 };
var evens = numbers.Where(n => n % 2 == 0).ToArray();
Console.WriteLine("Even numbers: " + string.Join(", ", evens));

// 异常处理
try
{
    int zero = 0;
    int result = number / zero;
}
catch (DivideByZeroException ex)
{
    Console.WriteLine("Error: " + ex.Message);
}
```

### 注意事项

- **文件限制：**顶级语句只能在一个源文件中使用。如果在一个项目中有多个使用顶级语句的文件，会导致编译错误。
- **程序入口：**如果使用顶级语句，则该文件会隐式地包含 Main 方法，并且该文件将成为程序的入口点。
- **作用域限制：**顶级语句中的代码共享一个全局作用域，这意味着可以在顶级语句中定义的变量和方法可以在整个文件中访问。

顶级语句在简化代码结构、降低学习难度和加快开发速度方面具有显著优势，特别适合于编写简单程序和脚本。

# C#常用快捷键

### 常用快捷方式

| 快捷键                     | 功能                 |
| :------------------------- | :------------------- |
| Ctrl + K + C               | 注释选定内容         |
| Ctrl + K + U               | 取消注释选定内容     |
| Ctrl + K + D               | 代码格式整个文档内容 |
| Ctrl + K + F               | 格式化选定内容       |
| F12                        | 转到定义             |
| Ctrl+F12                   | 转到声明             |
| Ctrl + -                   | 后退                 |
| Ctrl + Shift + -           | 前进                 |
| Ctrl + M + O               | 折叠当前代码块       |
| Ctrl + M + P               | 展开当前代码块       |
| Ctrl + M + M               | 切换大纲显示展开     |
| Ctrl + R + M               | 重构.提取方法        |
| Ctrl+Shift+K、Ctrl+Shift+P | 文件夹中的上一个书签 |
| Ctrl + Z                   | 撤销                 |
| Ctrl + X                   | 剪切                 |
| Ctrl + C                   | 复制                 |
| Ctrl + V                   | 粘贴                 |
| Ctrl+A                     | 全选                 |

### 文件操作

| 快捷键           | 功能       |
| :--------------- | :--------- |
| Ctrl + N         | 新建文件   |
| Ctrl + O         | 打开文件   |
| Ctrl + S         | 保存文件   |
| Ctrl + Shift + S | 文件另存为 |
| F2               | 文件重命名 |

### 查找与替换

| 快捷键           | 功能         |
| :--------------- | :----------- |
| Ctrl + F         | 查找         |
| Ctrl + H         | 替换         |
| Shift+F12        | 查找所有引用 |
| Ctrl + Shift + F | 在文件中查找 |
| Ctrl + Shift + H | 在文件中替换 |
| Ctrl + Shift + V | 循环剪贴板环 |

### 调试与运行

| 快捷键         | 功能           |
| :------------- | :------------- |
| F5             | 启动调试       |
| Ctrl+F5        | 开始执行不调试 |
| Shift + F5     | 停止调试       |
| F9             | 切换断点       |
| Ctrl+Shift+F9  | 删除所有断点   |
| F10            | 单步逐过程执行 |
| F11            | 逐语句调试     |
| Shift + F11    | 单步跳出       |
| Ctrl+Shift+F10 | 设置下一语句   |
| Ctrl+Alt+Q     | 快速监视       |

### 窗口管理

| 快捷键             | 功能                 |
| :----------------- | :------------------- |
| Ctrl + Tab         | 切换到下一个文档窗口 |
| Ctrl + Shift + Tab | 切换到上一个文档窗口 |
| Alt+`              | 窗口搜索             |
| Alt+F7             | 下一个工具窗口导航   |
| Ctrl+F4            | 关闭文档窗口         |
| Ctrl+F6            | 下一个文档窗口       |

### 其他

| 快捷键       | 功能                   |
| :----------- | :--------------------- |
| Shift+Alt+A  | 添加现有项目           |
| Ctrl+Shift+A | 添加新项目             |
| Ctrl+Alt+P   | 附加到进程             |
| Ctrl+Shift+C | 查看类视图             |
| Ctrl+Alt+X   | 工具箱                 |
| Ctrl+Shift+B | 生成解决方案           |
| Ctrl+Break   | 生成取消               |
| Ctrl+F7      | 生成编译               |
| Alt+F11      | 对解决方案运行代码分析 |
| Ctrl+Alt+O   | 输出                   |



# 变量的几种类型

用来计算机当中储存数据

1)、整数类型：int只能存储整数，不能存储小数.
2)、小数类型：doub1e 既能存储整数，也能存储小数，小数点后面的位数15~16位
3)、金钱类型：decimal 用来储存金钱，值后面需要加上一个m.
4)、字符串类型：string 用来存储多个文本，也可以存储空，字符串类型的值需要被双引号""引来，这个双引号必须是英文半角状态下的双引号
5)、字符类型：char,用来存储单个字符，最多、最少只能有一个字符，不能存储空.
字符类型的值需要用单引号因起来。英文半角状态下的单引号''。

## 值类型（Value types）

| 类型    | 描述                                 | 范围                                                    | 默认值 |
| :------ | :----------------------------------- | :------------------------------------------------------ | :----- |
| bool    | 布尔值                               | True 或 False                                           | False  |
| byte    | 8 位无符号整数                       | 0 到 255                                                | 0      |
| char    | 16 位 Unicode 字符                   | U +0000 到 U +ffff                                      | '\0'   |
| decimal | 128 位精确的十进制值，28-29 有效位数 | (-7.9 x 1028 到 7.9 x 1028) / 100 到 28                 | 0.0M   |
| double  | 64 位双精度浮点型                    | (+/-)5.0 x 10-324 到 (+/-)1.7 x 10308                   | 0.0D   |
| float   | 32 位单精度浮点型                    | -3.4 x 1038 到 + 3.4 x 1038                             | 0.0F   |
| int     | 32 位有符号整数类型                  | -2,147,483,648 到 2,147,483,647                         | 0      |
| long    | 64 位有符号整数类型                  | -9,223,372,036,854,775,808 到 9,223,372,036,854,775,807 | 0L     |
| sbyte   | 8 位有符号整数类型                   | -128 到 127                                             | 0      |
| short   | 16 位有符号整数类型                  | -32,768 到 32,767                                       | 0      |
| uint    | 32 位无符号整数类型                  | 0 到 4,294,967,295                                      | 0      |
| ulong   | 64 位无符号整数类型                  | 0 到 18,446,744,073,709,551,615                         | 0      |
| ushort  | 16 位无符号整数类型                  | 0 到 65,535                                             | 0      |

```c#
using System;

namespace DataTypeApplication
{
   class Program
   {
      static void Main(string[] args)
      {
            //变量类型 变量名;
            //变量名=值;
            //100
            //官方语言：声明或定义一个int类型的变量、
            int number;//在内存中开辟了一块能够储存整数的变量
            //官方语言：给这个变量赋值
            number = 100;//表示把199储存到了这块空间

            double n = 3.14; //浮点型
          
          
      }
   }
}
```

## 字符串（String）类型

```c#
using System;

namespace DataTypeApplication
{
   class Program
   {
      static void Main(string[] args)
      {
        String str = "runoob.com"; //字符串
        char str1 = '男';//字符
        //char str2 = '';//报错
        char str3 = '男女';//报错，只能一个          
        String str4 = "";//可以为空

	
          Console.WriteLine("Size of int: {0}", sizeof(int));
         Console.ReadLine();
      }
   }
}
```

# 变量的使用及命名规则

### **先声明--在赋值--在使用**

在C#中，直接使用未初始化的局部变量会导致编译错误。局部变量在使用之前必须显式初始化。因此，以下代码会导致编译错误：

```c#
int number; // 声明一个整数类型的变量
Console.WriteLine(number); // 错误：使用了未赋值的局部变量 'number'
```

**修正方法**

你需要在使用 `number` 变量之前为其赋值。例如：

```c#
int number = 10; // 声明并初始化变量
Console.WriteLine(number); // 正确：输出 10
```

------

### 1. **命名规则**

- **字母、数字和下划线**：变量名只能包含字母（a-z, A-Z）、数字（0-9）和下划线（_）。
- **首字符**：变量名必须以字母或下划线开头，不能以数字开头。
- **区分大小写**：C#是区分大小写的，因此`myVar`和`myvar`是两个不同的变量。
- **关键字**：不能使用C#的关键字（如`int`, `class`, `return`等）作为变量名。如果必须使用关键字，可以在前面加上`@`符号（如`@int`），但不推荐这样做。

### 2. **命名约定**

- **PascalCase**：用于类名、方法名、属性名、事件名等。每个单词的首字母大写，不包含下划线。

  ```c#
  public class MyClass
  {
      public void MyMethod()
      {
      }
  }
  ```

- **camelCase**：用于局部变量、参数、私有字段等。第一个单词的首字母小写，后续单词的首字母大写。

  ```c#
  int myVariable;
  string firstName;
  ```

- **_camelCase**：用于私有字段（private fields），通常在前面加一个下划线。

  ```c#
  private int _myPrivateField;
  ```

- **UPPER_CASE**：用于常量（const）和枚举值。所有字母大写，单词之间用下划线分隔。

  ```c#
  public const int MAX_COUNT = 100;
  public enum MyEnum
  {
      VALUE_ONE,
      VALUE_TWO
  }
  ```

### 3. **命名建议**

- **描述性**：变量名应具有描述性，能够清晰地表达变量的用途。避免使用单个字母或无意义的缩写。

  ```c#
  // 不推荐
  int x;
  string str;
  
  // 推荐
  int userAge;
  string userName;
  ```

- **避免缩写**：除非是广泛认可的缩写（如`id`、`url`等），否则应避免使用缩写。

  ```c#
  // 不推荐
  int usrCnt;
  
  // 推荐
  int userCount;
  ```

- **布尔变量**：布尔变量名应以`is`、`has`、`can`等开头，以明确表示其布尔类型。

  ```c#
  bool isActive;
  bool hasPermission;
  bool canExecute;
  ```

- **集合类型**：集合类型的变量名应使用复数形式，或者在名称中包含`List`、`Array`等表示集合的词汇。

  ```c#
  List<string> userNames;
  int[] scores;
  ```

### 4. **命名示例**

```c#
public class User
{
    private string _firstName;
    private string _lastName;

    public string FullName => $"{_firstName} {_lastName}";

    public User(string firstName, string lastName)
    {
        _firstName = firstName;
        _lastName = lastName;
    }

    public void PrintUserInfo()
    {
        Console.WriteLine($"User: {FullName}");
    }
}

public class Program
{
    public const int MAX_USERS = 100;

    public static void Main()
    {
        int userCount = 0;
        List<User> users = new List<User>();

        User newUser = new User("John", "Doe");
        users.Add(newUser);
        userCount++;

        Console.WriteLine($"Total Users: {userCount}");
    }
}
```

### 5. **总结**

- **遵循命名规则**：确保变量名符合C#的命名规则。
- **使用命名约定**：根据变量的作用域和类型选择合适的命名约定（如`camelCase`、`PascalCase`等）。
- **保持描述性**：变量名应清晰、简洁且具有描述性，避免使用无意义的缩写或单个字母。

遵循这些命名规范可以使代码更易于阅读、理解和维护。

# C#常量

常量和变量都是用来存储数据的容器，在定义时都需要指明数据类型，它们唯一的区别是：变量（Variable）中所存放的值是允许改变的，而常量（Constant）中存放的值不允许改变。

与变量不同的是，常量在第一次被赋值后值就不能再改变。定义常量需要使用关键字 **const** 来完成。

具体的语法形式如下：

```c#
const 数据类型 常量名 = 值;
```

需要注意的是，在定义常量时必须为其赋值，因为不赋值的话以后就再也不能赋值了。另外，也可以同时定义多个常量。

在程序中使用常量也会带来很多好处，包括增强了程序的可读性以及便于程序的修改。例如在一个计算率的程序中，为了保证程序中的税率统一，设置一个名为 TAX 的常量来完成，如果需要修改税率只修改该常量的值即可。

【实例1】分别求圆的面积和周长，并使用常量存放 π 的值，将 π 的值定义为3.14。

```c#
class Program
{
    static void Main(string[] args)
    {
        const double PI = 3.14;
        int r = 3;  //存放半径
        Console.WriteLine("圆的周长是：" + 2 * PI * r);
        Console.WriteLine("圆的面积是：" + PI * r * r);
    }
}	
```

# 类型转换方法

在 C# 中，类型转换是将一个数据类型的值转换为另一个数据类型的过程。

C# 中的类型转换可以分为两种：**隐式类型转换**和**显式类型转换**（也称为强制类型转换）。

### 隐式类型转换

隐式转换是不需要编写代码来指定的转换，编译器会自动进行。

隐式转换是指将一个较小范围的数据类型转换为较大范围的数据类型时，编译器会自动完成类型转换，这些转换是 C# 默认的以安全方式进行的转换, 不会导致数据丢失。

例如，从 int 到 long，从 float 到 double 等。

从小的整数类型转换为大的整数类型，从派生类转换为基类。将一个 byte 类型的变量赋值给 int 类型的变量，编译器会自动将 byte 类型转换为 int 类型，不需要显示转换。

```c#
byte b = 10;
int i = b; // 隐式转换，不需要显式转换
```

将一个整数赋值给一个长整数，或者将一个浮点数赋值给一个双精度浮点数，这种转换不会导致数据丢失：

```
int intValue = 42;
long longValue = intValue; // 隐式转换，从 int 到 long
```

### 显式转换

显式类型转换，即强制类型转换，需要程序员在代码中明确指定。

显式转换是指将一个较大范围的数据类型转换为较小范围的数据类型时，或者将一个对象类型转换为另一个对象类型时，需要使用强制类型转换符号进行显示转换，强制转换会造成数据丢失。

例如，将一个 int 类型的变量赋值给 byte 类型的变量，需要显示转换。

```
int i = 10;
byte b = (byte)i; // 显式转换，需要使用强制类型转换符号
```

强制转换为整数类型：

```
double doubleValue = 3.14;
int intValue = (int)doubleValue; // 强制从 double 到 int，数据可能损失小数部分
```

强制转换为字符串类型：

```
int intValue = 123;
string stringValue = intValue.ToString(); // 将 int 转换为字符串
```

下面的实例显示了一个显式的类型转换：

```c#
using System;

namespace TypeConversionApplication
{
    class ExplicitConversion
    {
        static void Main(string[] args)
        {
            double d = 5673.74;
            int i;

            // 强制转换 double 为 int
            i = (int)d;
            Console.WriteLine(i);
            Console.ReadKey();
            
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
5673
```

## C# 类型转换方法

C# 提供了下列内置的类型转换方法：

| 序号 | 方法 & 描述                                                  |
| :--- | :----------------------------------------------------------- |
| 1    | **ToBoolean** 如果可能的话，把类型转换为布尔型。             |
| 2    | **ToByte** 把类型转换为字节类型。                            |
| 3    | **ToChar** 如果可能的话，把类型转换为单个 Unicode 字符类型。 |
| 4    | **ToDateTime** 把类型（整数或字符串类型）转换为 日期-时间 结构。 |
| 5    | **ToDecimal** 把浮点型或整数类型转换为十进制类型。           |
| 6    | **ToDouble** 把类型转换为双精度浮点型。                      |
| 7    | **ToInt16** 把类型转换为 16 位整数类型。                     |
| 8    | **ToInt32** 把类型转换为 32 位整数类型。                     |
| 9    | **ToInt64** 把类型转换为 64 位整数类型。                     |
| 10   | **ToSbyte** 把类型转换为有符号字节类型。                     |
| 11   | **ToSingle** 把类型转换为小浮点数类型。                      |
| 12   | **ToString** 把类型转换为字符串类型。                        |
| 13   | **ToType** 把类型转换为指定类型。                            |
| 14   | **ToUInt16** 把类型转换为 16 位无符号整数类型。              |
| 15   | **ToUInt32** 把类型转换为 32 位无符号整数类型。              |
| 16   | **ToUInt64** 把类型转换为 64 位无符号整数类型。              |

这些方法都定义在 System.Convert 类中，使用时需要包含 System 命名空间。它们提供了一种安全的方式来执行类型转换，因为它们可以处理 null值，并且会抛出异常，如果转换不可能进行。

例如，使用 Convert.ToInt32 方法将字符串转换为整数：

```
string str = "123";
int number = Convert.ToInt32(str); // 转换成功，number为123
```

如果字符串不是有效的整数表示，Convert.ToInt32 将抛出 FormatException。

下面的实例把不同值的类型转换为字符串类型：

```
using System;

namespace TypeConversionApplication
{
    class StringConversion
    {
        static void Main(string[] args)
        {
            // 定义一个整型变量
            int i = 75;
            
            // 定义一个浮点型变量
            float f = 53.005f;
            
            // 定义一个双精度浮点型变量
            double d = 2345.7652;
            
            // 定义一个布尔型变量
            bool b = true;

            // 将整型变量转换为字符串并输出
            Console.WriteLine(i.ToString());
            
            // 将浮点型变量转换为字符串并输出
            Console.WriteLine(f.ToString());
            
            // 将双精度浮点型变量转换为字符串并输出
            Console.WriteLine(d.ToString());
            
            // 将布尔型变量转换为字符串并输出
            Console.WriteLine(b.ToString());

            // 等待用户按键后关闭控制台窗口
            Console.ReadKey();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
75
53.005
2345.7652
True
```

在进行类型转换时需要注意以下几点：

- 隐式转换只能将较小范围的数据类型转换为较大范围的数据类型，不能将较大范围的数据类型转换为较小范围的数据类型；
- 显式转换可能会导致数据丢失或精度降低，需要进行数据类型的兼容性检查；
- 对于对象类型的转换，需要进行类型转换的兼容性检查和类型转换的安全性检查。

## 类型转换方法

C# 提供了多种类型转换方法，例如使用 Convert 类、Parse 方法和 TryParse 方法，这些方法可以帮助处理不同的数据类型之间的转换。

### 使用 Convert 类

Convert 类提供了一组静态方法，可以在各种基本数据类型之间进行转换。

```
string str = "123";
int num = Convert.ToInt32(str);
```

### 使用 Parse 方法

Parse 方法用于将字符串转换为对应的数值类型，如果转换失败会抛出异常。

```
string str = "123.45";
double d = double.Parse(str);
```

### 使用 TryParse 方法

TryParse 方法类似于 Parse，但它不会抛出异常，而是返回一个布尔值指示转换是否成功。

```
string str = "123.45";
double d;
bool success = double.TryParse(str, out d);

if (success) {
    Console.WriteLine("转换成功: " + d);
} else {
    Console.WriteLine("转换失败");
}
```

## 自定义类型转换

C# 还允许你定义自定义类型转换操作，通过在类型中定义 implicit 或 explicit 关键字。

```
using System;

public class Fahrenheit
{
    public double Degrees { get; set; }

    public Fahrenheit(double degrees)
    {
        Degrees = degrees;
    }

    // 隐式转换从Fahrenheit到double
    public static implicit operator double(Fahrenheit f)
    {
        return f.Degrees;
    }

    // 显式转换从double到Fahrenheit
    public static explicit operator Fahrenheit(double d)
    {
        return new Fahrenheit(d);
    }
}

public class Program
{
    public static void Main()
    {
        Fahrenheit f = new Fahrenheit(98.6);
        Console.WriteLine("Fahrenheit object: " + f.Degrees + " degrees");

        double temp = f; // 隐式转换
        Console.WriteLine("After implicit conversion to double: " + temp + " degrees");

        Fahrenheit newF = (Fahrenheit)temp; // 显式转换
        Console.WriteLine("After explicit conversion back to Fahrenheit: " + newF.Degrees + " degrees");
    }
}
```

以上例子中，我们定义了一个 Fahrenheit 类，并实现了从 Fahrenheit 到 double 的隐式转换和从 double 到 Fahrenheit 的显式转换。

输出结果将显示如下：

```
Fahrenheit object: 98.6 degrees
After implicit conversion to double: 98.6 degrees
After explicit conversion back to Fahrenheit: 98.6 degrees
```

## 总结

在 C# 中，内置的类型转换方法主要通过以下几种方式实现：隐式转换、显式转换（强制转换）、使用 Convert 类的方法、Parse 方法和 TryParse 方法，这些方法广泛应用于不同数据类型之间的转换。

以下是 C# 内置类型转换方法的表格：

| **方法类别**         | **方法**                                  | **描述**                                                     |
| :------------------- | :---------------------------------------- | :----------------------------------------------------------- |
| 隐式转换             | 自动进行的转换                            | 无需显式指定，通常用于安全的类型转换，如从较小类型到较大类型 |
| 显式转换（强制转换） | `(type)value`                             | 需要显式指定，通常用于可能导致数据丢失或转换失败的情况       |
| `Convert` 类方法     | `Convert.ToBoolean(value)`                | 将指定类型转换为 `Boolean`                                   |
|                      | `Convert.ToByte(value)`                   | 将指定类型转换为 `Byte`                                      |
|                      | `Convert.ToChar(value)`                   | 将指定类型转换为 `Char`                                      |
|                      | `Convert.ToDateTime(value)`               | 将指定类型转换为 `DateTime`                                  |
|                      | `Convert.ToDecimal(value)`                | 将指定类型转换为 `Decimal`                                   |
|                      | `Convert.ToDouble(value)`                 | 将指定类型转换为 `Double`                                    |
|                      | `Convert.ToInt16(value)`                  | 将指定类型转换为 `Int16`（短整型）                           |
|                      | `Convert.ToInt32(value)`                  | 将指定类型转换为 `Int32`（整型）                             |
|                      | `Convert.ToInt64(value)`                  | 将指定类型转换为 `Int64`（长整型）                           |
|                      | `Convert.ToSByte(value)`                  | 将指定类型转换为 `SByte`                                     |
|                      | `Convert.ToSingle(value)`                 | 将指定类型转换为 `Single`（单精度浮点型）                    |
|                      | `Convert.ToString(value)`                 | 将指定类型转换为 `String`                                    |
|                      | `Convert.ToUInt16(value)`                 | 将指定类型转换为 `UInt16`（无符号短整型）                    |
|                      | `Convert.ToUInt32(value)`                 | 将指定类型转换为 `UInt32`（无符号整型）                      |
|                      | `Convert.ToUInt64(value)`                 | 将指定类型转换为 `UInt64`（无符号长整型）                    |
| `Parse` 方法         | `Boolean.Parse(string)`                   | 将字符串解析为 `Boolean`                                     |
|                      | `Byte.Parse(string)`                      | 将字符串解析为 `Byte`                                        |
|                      | `Char.Parse(string)`                      | 将字符串解析为 `Char`                                        |
|                      | `DateTime.Parse(string)`                  | 将字符串解析为 `DateTime`                                    |
|                      | `Decimal.Parse(string)`                   | 将字符串解析为 `Decimal`                                     |
|                      | `Double.Parse(string)`                    | 将字符串解析为 `Double`                                      |
|                      | `Int16.Parse(string)`                     | 将字符串解析为 `Int16`                                       |
|                      | `Int32.Parse(string)`                     | 将字符串解析为 `Int32`                                       |
|                      | `Int64.Parse(string)`                     | 将字符串解析为 `Int64`                                       |
|                      | `SByte.Parse(string)`                     | 将字符串解析为 `SByte`                                       |
|                      | `Single.Parse(string)`                    | 将字符串解析为 `Single`                                      |
|                      | `UInt16.Parse(string)`                    | 将字符串解析为 `UInt16`                                      |
|                      | `UInt32.Parse(string)`                    | 将字符串解析为 `UInt32`                                      |
|                      | `UInt64.Parse(string)`                    | 将字符串解析为 `UInt64`                                      |
| `TryParse` 方法      | `Boolean.TryParse(string, out bool)`      | 尝试将字符串解析为 `Boolean`，返回布尔值表示是否成功         |
|                      | `Byte.TryParse(string, out byte)`         | 尝试将字符串解析为 `Byte`，返回布尔值表示是否成功            |
|                      | `Char.TryParse(string, out char)`         | 尝试将字符串解析为 `Char`，返回布尔值表示是否成功            |
|                      | `DateTime.TryParse(string, out DateTime)` | 尝试将字符串解析为 `DateTime`，返回布尔值表示是否成功        |
|                      | `Decimal.TryParse(string, out decimal)`   | 尝试将字符串解析为 `Decimal`，返回布尔值表示是否成功         |
|                      | `Double.TryParse(string, out double)`     | 尝试将字符串解析为 `Double`，返回布尔值表示是否成功          |
|                      | `Int16.TryParse(string, out short)`       | 尝试将字符串解析为 `Int16`，返回布尔值表示是否成功           |
|                      | `Int32.TryParse(string, out int)`         | 尝试将字符串解析为 `Int32`，返回布尔值表示是否成功           |
|                      | `Int64.TryParse(string, out long)`        | 尝试将字符串解析为 `Int64`，返回布尔值表示是否成功           |
|                      | `SByte.TryParse(string, out sbyte)`       | 尝试将字符串解析为 `SByte`，返回布尔值表示是否成功           |
|                      | `Single.TryParse(string, out float)`      | 尝试将字符串解析为 `Single`，返回布尔值表示是否成功          |
|                      | `UInt16.TryParse(string, out ushort)`     | 尝试将字符串解析为 `UInt16`，返回布尔值表示是否成功          |
|                      | `UInt32.TryParse(string, out uint)`       | 尝试将字符串解析为 `UInt32`，返回布尔值表示是否成功          |
|                      | `UInt64.TryParse(string, out ulong)`      | 尝试将字符串解析为 `UInt64`，返回布尔值表示是否成功          |

# 赋值运算

### 1. **基本赋值运算**

- **语法**：`变量 = 值或表达式`

- **作用**：将右侧的值或表达式的结果赋值给左侧的变量。

- **示例**：

  ```c#
  int a = 10; // 将 10 赋值给变量 a
  string name = "Alice"; // 将字符串 "Alice" 赋值给变量 name
  double result = 3.14 * 2; // 将表达式 3.14 * 2 的结果赋值给变量 result
  ```

------

### 2. **复合赋值运算**

- **语法**：`变量 运算符= 值或表达式`

- **作用**：将变量与右侧的值或表达式进行运算，然后将结果赋值给变量。

- **常用复合赋值运算符**：

  - `+=`：加法赋值
  - `-=`：减法赋值
  - `*=`：乘法赋值
  - `/=`：除法赋值
  - `%=`：取模赋值
  - `&=`：按位与赋值
  - `|=`：按位或赋值
  - `^=`：按位异或赋值
  - `<<=`：左移赋值
  - `>>=`：右移赋值

- **示例**：

  ```c#
  int x = 5;
  x += 3; // 等价于 x = x + 3; 结果 x = 8
  x *= 2; // 等价于 x = x * 2; 结果 x = 16
  x %= 3; // 等价于 x = x % 3; 结果 x = 1
  ```

------

### 3. **多重赋值**

- **语法**：`变量1 = 变量2 = 值或表达式`

- **作用**：将同一个值或表达式的结果赋值给多个变量。

- **示例**：

  ```c#
  int a, b, c;
  a = b = c = 10; // a, b, c 都被赋值为 10
  ```

------

### 4. **解构赋值**

- **语法**：`(变量1, 变量2, ...) = (值1, 值2, ...)`

- **作用**：将元组或数组中的值解构并分别赋值给多个变量。

- **示例**：

  ```c#
  var (x, y) = (10, 20); // x = 10, y = 20
  int[] numbers = { 1, 2, 3 };
  var (a, b, c) = (numbers[0], numbers[1], numbers[2]); // a = 1, b = 2, c = 3
  ```

------

### 5. **空合并赋值（C# 8.0 引入）**

- **语法**：`变量 ??= 值或表达式`

- **作用**：如果变量为`null`，则将右侧的值或表达式赋值给变量；否则不进行赋值。

- **示例**：

  ```c#
  string name = null;
  name ??= "Unknown"; // name 为 null，赋值 "Unknown"
  Console.WriteLine(name); // 输出 "Unknown"
  
  name ??= "John"; // name 不为 null，不进行赋值
  Console.WriteLine(name); // 输出 "Unknown"
  ```

------

### 6. **条件赋值**

- **语法**：`变量 = 条件 ? 值1 : 值2`

- **作用**：根据条件判断，将`值1`或`值2`赋值给变量。

- **示例**：

  ```c#
  int age = 20;
  string status = age >= 18 ? "Adult" : "Minor"; // status = "Adult"
  ```

------

### 7. **引用类型赋值**

- **特点**：引用类型的赋值是传递引用（内存地址），而不是复制值。

- **示例**：

  ```c#
  int[] array1 = { 1, 2, 3 };
  int[] array2 = array1; // array2 和 array1 指向同一个数组
  array2[0] = 100;
  Console.WriteLine(array1[0]); // 输出 100
  ```

------

### 8. **只读赋值（`readonly` 和 `const`）**

- **`const`**：编译时常量，必须在声明时赋值，且不能修改。

  ```c#
  const double PI = 3.14;
  ```

- **`readonly`**：运行时常量，可以在声明时或构造函数中赋值，之后不能修改。

  ```c#
  readonly int maxValue;
  public MyClass(int value)
  {
      maxValue = value;
  }
  ```

------

### 9. **特殊赋值场景**

- **`out` 参数**：用于方法中返回多个值。

  ```c#
  void Divide(int a, int b, out int quotient, out int remainder)
  {
      quotient = a / b;
      remainder = a % b;
  }
  
  int q, r;
  Divide(10, 3, out q, out r); // q = 3, r = 1
  ```

- **`ref` 参数**：传递变量的引用，允许方法直接修改原始变量。

  ```c#
  void Increment(ref int value)
  {
      value++;
  }
  
  int num = 5;
  Increment(ref num); // num = 6
  ```

------

### 10. **赋值运算的注意事项**

- **类型匹配**：赋值时，右侧的值或表达式必须与左侧变量的类型兼容。

  ```c#
  int a = 10; // 正确
  int b = "Hello"; // 错误，类型不匹配
  ```

- **隐式类型转换**：某些情况下，C#会自动进行隐式类型转换（如`int`到`double`）。

  ```c#
  double d = 10; // 正确，int 隐式转换为 double
  ```

- **显式类型转换**：如果类型不兼容且无法隐式转换，需要使用显式类型转换。

  ```c#
  int x = (int)3.14; // 显式将 double 转换为 int
  ```

# 占位符的使用

## 1. `String.Format` 方法

`String.Format` 方法可以根据指定的格式字符串和参数列表创建格式化后的字符串，占位符用 `{索引}` 表示，索引从 0 开始。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        string name = "Alice";
        int age = 25;
        string message = String.Format("My name is {0} and I'm {1} years old.", name, age);
        Console.WriteLine(message);
    }
}
```

### 代码解释

- `{0}` 代表 `name` 变量，`{1}` 代表 `age` 变量。
- `String.Format` 方法会按照顺序将变量的值替换到占位符的位置，最终输出格式化后的字符串。

## 2. `Console.WriteLine` 方法

`Console.WriteLine` 方法同样支持占位符，用法和 `String.Format` 类似。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        string city = "New York";
        double temperature = 28.5;
        Console.WriteLine("The temperature in {0} is {1} degrees Celsius.", city, temperature);
    }
}
```

### 代码解释

- `{0}` 对应 `city` 变量，`{1}` 对应 `temperature` 变量。
- `Console.WriteLine` 会直接将格式化后的字符串输出到控制台。

## 3. 字符串插值（C# 6.0 及以上版本）

字符串插值使用 `$` 符号，在字符串中直接使用 `{变量名}` 作为占位符，使代码更简洁直观。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        string product = "Laptop";
        decimal price = 999.99m;
        string info = $"The {product} costs {price:C}.";
        Console.WriteLine(info);
    }
}
```

### 代码解释

- 在字符串前加上 `$` 符号后，就可以直接在 `{}` 里使用变量名。
- `{price:C}` 中的 `:C` 是格式说明符，表示将 `price` 格式化为货币形式。

## 4. 带有对齐和格式说明符的占位符

占位符可以指定对齐方式和格式说明符，语法为 `{索引,对齐方式:格式说明符}`。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        int number = 123;
        string formatted = String.Format("{0,10:D5}", number);
        Console.WriteLine($"|{formatted}|");
    }
}
```

### 代码解释

- `{0,10:D5}` 中，`0` 是索引，`10` 表示右对齐宽度为 10 个字符，`D5` 表示将整数格式化为至少 5 位的十进制数。
- 如果数字不足 5 位，会在前面补 0；右对齐会在左边填充空格。

## 5. 日期和时间格式化

对于 `DateTime` 类型的变量，占位符可以实现不同的日期和时间格式化。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        DateTime now = DateTime.Now;
        string shortDate = String.Format("{0:d}", now);
        string longTime = String.Format("{0:T}", now);
        Console.WriteLine($"Short date: {shortDate}");
        Console.WriteLine($"Long time: {longTime}");
    }
}
```

### 代码解释

- `{0:d}` 会将 `DateTime` 对象格式化为短日期形式。
- `{0:T}` 会将其格式化为长时间形式。

# 变量交换

在 C# 中，变量交换是指将两个变量的值互相交换。以下是几种常见的实现变量交换的方法：

### 1. 使用临时变量

这是最传统、最容易理解的方法，通过引入一个临时变量来暂存其中一个变量的值，从而实现两个变量值的交换。

```csharp
using System;

class Program
{
    static void Main()
    {
        int a = 10;
        int b = 20;

        // 输出交换前的值
        Console.WriteLine($"交换前: a = {a}, b = {b}");

        // 使用临时变量交换
        int temp = a;
        a = b;
        b = temp;

        // 输出交换后的值
        Console.WriteLine($"交换后: a = {a}, b = {b}");
    }
}
```

**代码解释**：

- 首先，定义了两个整数变量 `a` 和 `b`，并分别初始化为 10 和 20。
- 然后，声明一个临时变量 `temp`，将 `a` 的值赋给 `temp`。
- 接着，把 `b` 的值赋给 `a`。
- 最后，将 `temp`（即原来 `a` 的值）赋给 `b`，完成交换。

# 接收用户控制台输入

#### 1. 使用 `Console.ReadLine` 方法

`Console.ReadLine` 方法可用于从控制台读取用户输入的一行文本，返回值为字符串类型。若要处理其他数据类型，就需要进行相应的类型转换。

**示例代码：接收用户输入的字符串**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("请输入你的姓名：");
        string name = Console.ReadLine();
        Console.WriteLine($"你好，{name}！");
    }
}
```

**代码解释**：

- `Console.Write` 会在控制台输出提示信息，且输出后不会换行。
- `Console.ReadLine` 会等待用户输入内容，将输入的内容作为字符串返回，并赋值给 `name` 变量。
- 最后，`Console.WriteLine` 输出包含用户输入姓名的问候语。

**示例代码：接收用户输入的整数**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.Write("请输入一个整数：");
        string input = Console.ReadLine();
        if (int.TryParse(input, out int number))
        {
            Console.WriteLine($"你输入的整数是 {number}，它的平方是 {number * number}。");
        }
        else
        {
            Console.WriteLine("输入无效，请输入一个有效的整数。");
        }
    }
}
```

**代码解释**：

- 先使用 `Console.ReadLine` 读取用户输入的字符串。
- 接着用 `int.TryParse` 方法尝试把输入的字符串转换为整数。该方法会返回一个布尔值，表明转换是否成功，同时通过 `out` 参数输出转换后的整数。
- 若转换成功，计算该整数的平方并输出结果；若失败，则提示用户输入无效。

#### 2. 使用 `Console.ReadKey` 方法

`Console.ReadKey` 方法用于读取用户按下的一个按键，返回一个 `ConsoleKeyInfo` 对象，该对象包含了按键的相关信息。

**示例代码：读取用户按下的单个按键**

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("请按下任意一个按键...");
        ConsoleKeyInfo keyInfo = Console.ReadKey();
        Console.WriteLine($"\n你按下的按键是：{keyInfo.Key}");
    }
}
```

**代码解释**：

- `Console.ReadKey` 方法会暂停程序执行，等待用户按下一个按键。
- 按下按键后，该方法返回一个 `ConsoleKeyInfo` 对象，通过 `keyInfo.Key` 能获取按下的按键信息。
- `\n` 用于在输出按键信息前换行，使显示更清晰。

# 转义符

转义符是一种特殊的字符序列，以反斜杠`\`开头，用于表示一些无法直接输入的字符或具有特殊意义的字符。当你需要在字符串中包含引号、换行符等特殊字符时，就可以使用转义符。

#### 常见的转义符及其作用

| 转义符 | 描述         |
| ------ | ------------ |
| `\'`   | 单引号       |
| `\"`   | 双引号       |
| `\\`   | 反斜杠       |
| `\0`   | 空字符       |
| `\a`   | 警报（响铃） |
| `\b`   | 退格         |
| `\f`   | 换页         |
| `\n`   | 换行         |
| `\r`   | 回车         |
| `\t`   | 水平制表符   |
| `\v`   | 垂直制表符   |

#### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        // 包含双引号的字符串
        string quote = "He said, \"Hello!\"";
        Console.WriteLine(quote);

        // 包含换行符的字符串
        string multiLine = "First line.\nSecond line.";
        Console.WriteLine(multiLine);

        // 包含反斜杠的字符串
        string path = "C:\\Program Files\\Example";
        Console.WriteLine(path);
    }
}
```

#### 运行结果

```
He said, "Hello!"
First line.
Second line.
C:\Program Files\Example
```

#### 代码解释

- `He said, \"Hello!\"`：使用`\"`来表示字符串中的双引号。
- `First line.\nSecond line.`：使用`\n`来表示换行符，使字符串分两行输出。
- `C:\\Program Files\\Example`：使用`\\`来表示一个反斜杠，因为反斜杠本身是转义符的起始字符，所以需要用两个反斜杠来表示一个实际的反斜杠。

# `@`符号

在 C# 中，`@`符号有两种主要用途：用于逐字字符串字面量和用于处理与 C# 关键字同名的标识符。

#### 逐字字符串字面量

当在字符串前面加上`@`符号时，该字符串就是逐字字符串字面量。在逐字字符串中，转义符将失去作用，所有字符都将按原样输出，并且可以跨越多行。

#### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        // 包含反斜杠的逐字字符串
        string path = @"C:\Program Files\Example";
        Console.WriteLine(path);

        // 跨越多行的逐字字符串
        string multiLine = @"This is a
multi - line string.";
        Console.WriteLine(multiLine);

        // 包含双引号的逐字字符串
        string quote = @"He said, ""Hello!""";
        Console.WriteLine(quote);
    }
}
```

#### 代码解释

- `@"C:\Program Files\Example"`：使用逐字字符串，反斜杠不需要转义，直接按原样输出。
- `@"This is a multi - line string."`：逐字字符串可以跨越多行，换行符会被保留。
- `@"He said, ""Hello!"""`：在逐字字符串中，要表示双引号，需要使用两个双引号`""`。

#### 处理与 C# 关键字同名的标识符

`@`符号还可以用于处理与 C# 关键字同名的标识符，在标识符前面加上`@`符号，就可以将其作为普通的标识符使用。

#### 示例代码

```csharp
class Program
{
    static void Main()
    {
        // 使用 @ 符号定义与关键字同名的变量
        int @class = 10;
        Console.WriteLine(@class);
    }
}
```

#### 代码解释

在这个示例中，使用`@`符号定义了一个名为`@class`的变量，`class`是 C# 的关键字，但通过`@`符号，它可以作为普通的标识符使用

## 算术运算符

下表显示了 C# 支持的所有算术运算符。假设变量 **A** 的值为 10，变量 **B** 的值为 20，则：

| 运算符 | 描述                             | 实例             |
| :----- | :------------------------------- | :--------------- |
| +      | 把两个操作数相加                 | A + B 将得到 30  |
| -      | 从第一个操作数中减去第二个操作数 | A - B 将得到 -10 |
| *      | 把两个操作数相乘                 | A * B 将得到 200 |
| /      | 分子除以分母                     | B / A 将得到 2   |
| %      | 取模运算符，整除后的余数         | B % A 将得到 0   |
| ++     | 自增运算符，整数值增加 1         | A++ 将得到 11    |
| --     | 自减运算符，整数值减少 1         | A-- 将得到 9     |

# C# ++ 和--

- **c = a++**: 先将 a 赋值给 c，再对 a 进行自增运算。
- **c = ++a**: 先将 a 进行自增运算，再将 a 赋值给 c 。
- **c = a--**: 先将 a 赋值给 c，再对 a 进行自减运算。
- **c = --a**: 先将 a 进行自减运算，再将 a 赋值给 c 。

```c#
using System;

namespace DataTypeApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = 1;
            int b;

            // a++ 先赋值再进行自增运算
            b = a++; //b
            Console.WriteLine("a = {0}", a);
            Console.WriteLine("b = {0}", b);
            Console.ReadLine();

            // ++a 先进行自增运算再赋值
            a = 1; // 重新初始化 a
            b = ++a;
            Console.WriteLine("a = {0}", a);
            Console.WriteLine("b = {0}", b);
            Console.ReadLine();

            // a-- 先赋值再进行自减运算
            a = 1;  // 重新初始化 a
            b = a--;
            Console.WriteLine("a = {0}", a);
            Console.WriteLine("b = {0}", b);
            Console.ReadLine();

            // --a 先进行自减运算再赋值
            a = 1;  // 重新初始化 a
            b = --a;
            Console.WriteLine("a = {0}", a);
            Console.WriteLine("b = {0}", b);
            Console.ReadLine();
        }
    }
}

```

执行以上程序，输出结果为：

```c#
a = 2
b = 1
a = 2
b = 2
a = 0
b = 1
a = 0
b = 0
```

# 关系运算符

下表显示了 C# 支持的所有关系运算符。假设变量 **A** 的值为 10，变量 **B** 的值为 20，则：

| 运算符 | 描述                                                         | 实例              |
| :----- | :----------------------------------------------------------- | :---------------- |
| ==     | 检查两个操作数的值是否相等，如果相等则条件为真。             | (A == B) 不为真。 |
| !=     | 检查两个操作数的值是否相等，如果不相等则条件为真。           | (A != B) 为真。   |
| >      | 检查左操作数的值是否大于右操作数的值，如果是则条件为真。     | (A > B) 不为真。  |
| <      | 检查左操作数的值是否小于右操作数的值，如果是则条件为真。     | (A < B) 为真。    |
| >=     | 检查左操作数的值是否大于或等于右操作数的值，如果是则条件为真。 | (A >= B) 不为真。 |
| <=     | 检查左操作数的值是否小于或等于右操作数的值，如果是则条件为真。 | (A <= B) 为真。   |

### 实例

请看下面的实例，了解 C# 中所有可用的关系运算符：

## 实例

```c#
using System;

class Program
{
  static void Main(string[] args)
  {
      int a = 21;
      int b = 10;
      
      if (a == b)
      {
          Console.WriteLine("Line 1 - a 等于 b");
      }
      else
      {
          Console.WriteLine("Line 1 - a 不等于 b");
      }
      if (a < b)
      {
          Console.WriteLine("Line 2 - a 小于 b");
      }
      else
      {
          Console.WriteLine("Line 2 - a 不小于 b");
      }
      if (a > b)
      {
          Console.WriteLine("Line 3 - a 大于 b");
      }
      else
      {
          Console.WriteLine("Line 3 - a 不大于 b");
      }
      /* 改变 a 和 b 的值 */
      a = 5;
      b = 20;
      if (a <= b)
      {
         Console.WriteLine("Line 4 - a 小于或等于 b");
      }
      if (b >= a)
      {
         Console.WriteLine("Line 5 - b 大于或等于 a");
      }
  }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
Line 1 - a 不等于 b
Line 2 - a 不小于 b
Line 3 - a 大于 b
Line 4 - a 小于或等于 b
Line 5 - b 大于或等于 a
```

# 逻辑运算符

下表显示了 C# 支持的所有逻辑运算符。假设变量 **A** 为布尔值 true，变量 **B** 为布尔值 false，则：

| 运算符 | 描述                                                         | 实例              |
| :----- | :----------------------------------------------------------- | :---------------- |
| &&     | 称为逻辑与运算符。如果两个操作数都非零，则条件为真。         | (A && B) 为假。   |
| \|\|   | 称为逻辑或运算符。如果两个操作数中有任意一个非零，则条件为真。 | (A \|\| B) 为真。 |
| !      | 称为逻辑非运算符。用来逆转操作数的逻辑状态。如果条件为真则逻辑非运算符将使其为假。 | !(A && B) 为真。  |

### 实例

请看下面的实例，了解 C# 中所有可用的逻辑运算符：

## 实例

```c#
using System;

namespace OperatorsAppl
{
    class Program
    {
        static void Main(string[] args)
        {
            bool a = true;
            bool b = true;
           
            if (a && b)
            {
               Console.WriteLine("Line 1 - 条件为真");
            }
            if (a || b)
            {
                Console.WriteLine("Line 2 - 条件为真");
            }
            /* 改变 a 和 b 的值 */
            a = false;
            b = true;
            if (a && b)
            {
                Console.WriteLine("Line 3 - 条件为真");
            }
            else
            {
                Console.WriteLine("Line 3 - 条件不为真");
            }
            if (!(a && b))
            {
                Console.WriteLine("Line 4 - 条件为真");
            }
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
Line 1 - 条件为真
Line 2 - 条件为真
Line 3 - 条件不为真
Line 4 - 条件为真
```

# 判断润年练习

闰年的判断规则是：普通年份能被 4 整除但不能被 100 整除，或者世纪年份能被 400 整除。以下是几种不同的实现方式：

```c#
using System;

class Program
{
    static void Main()
    {
        // 示例年份
        int year = 2024;
        bool isLeapYear = IsLeapYear(year);
        if (isLeapYear)
        {
            Console.WriteLine($"{year} 是闰年。");
        }
        else
        {
            Console.WriteLine($"{year} 不是闰年。");
        }
    }

    static bool IsLeapYear(int year)
    {
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
        {
            return true;
        }
        return false;
    }
}
```

在上述代码中，定义了一个名为 `IsLeapYear` 的方法，该方法接收一个整数类型的参数 `year`，表示要判断的年份。在方法内部，使用 `if-else` 语句根据闰年的判断规则进行判断，如果是闰年则返回 `true`，否则返回 `false`。在 `Main` 方法中，调用 `IsLeapYear` 方法进行判断，并输出相应的结果。

# 判断

## 判断语句

C# 提供了以下类型的判断语句。点击链接查看每个语句的细节。

| 语句                                                         | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [if 语句](https://www.runoob.com/csharp/csharp-if.html)      | 一个 **if 语句** 由一个布尔表达式后跟一个或多个语句组成。    |
| [if...else 语句](https://www.runoob.com/csharp/csharp-if-else.html) | 一个 **if 语句** 后可跟一个可选的 **else 语句**，else 语句在布尔表达式为假时执行。 |
| [嵌套 if 语句](https://www.runoob.com/csharp/csharp-nested-if.html) | 您可以在一个 **if** 或 **else if** 语句内使用另一个 **if** 或 **else if** 语句。 |
| [switch 语句](https://www.runoob.com/csharp/csharp-switch.html) | 一个 **switch** 语句允许测试一个变量等于多个值时的情况。     |
| [嵌套 switch 语句](https://www.runoob.com/csharp/csharp-nested-switch.html) | 您可以在一个 **switch** 语句内使用另一个 **switch** 语句。   |

## if 语句

一个 **if 语句** 由一个布尔表达式后跟一个或多个语句组成。

### 语法

C# 中 **if** 语句的语法：

```c#
if(boolean_expression)
{
   /* 如果布尔表达式为真将执行的语句 */
}
```

如果布尔表达式为 **true**，则 if 语句内的代码块将被执行。如果布尔表达式为 **false**，则 if 语句结束后的第一组代码（闭括号后）将被执行。

### 实例

```c#
using System;

namespace DecisionMaking
{
    
    class Program
    {
        static void Main(string[] args)
        {
            /* 局部变量定义 */
            int a = 10;

            /* 使用 if 语句检查布尔条件 */
            if (a < 20)
            {
                /* 如果条件为真，则输出下面的语句 */
                Console.WriteLine("a 小于 20");
            }
            Console.WriteLine("a 的值是 {0}", a);
            Console.ReadLine();
        }
    }
}
```

 当上面的代码被编译和执行时，它会产生下列结果：

```
a 小于 20
a 的值是 10
```

## if...else 语句

一个 **if 语句** 后可跟一个可选的 **else 语句**，else 语句在布尔表达式为假时执行。

### 语法

C# 中 **if...else** 语句的语法：

```c#
if(boolean_expression)
{
   /* 如果布尔表达式为真将执行的语句 */
}
else
{
  /* 如果布尔表达式为假将执行的语句 */
}
```

如果布尔表达式为 **true**，则执行 **if** 块内的代码。如果布尔表达式为 **false**，则执行 **else** 块内的代码。

### 实例1

```c#
using System;

namespace DataTypeApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("请输入用户名：");
            string name = Console.ReadLine();
            Console.WriteLine("请输入密码：");
            string pwd = Console.ReadLine();
            if (name == "admin" && pwd == "123")
            {
                Console.WriteLine("登录成功！");

            }
            else
            {
                Console.WriteLine("登录失败！");
            }
            
        }
    }
}
```

### 实例2

```c#
using System;

namespace DecisionMaking
{
    
    class Program
    {
        static void Main(string[] args)
        {

            /* 局部变量定义 */
            int a = 100;

            /* 检查布尔条件 */
            if (a < 20)
            {
                /* 如果条件为真，则输出下面的语句 */
                Console.WriteLine("a 小于 20");
            }
            else
            {
                /* 如果条件为假，则输出下面的语句 */
                Console.WriteLine("a 大于 20");
            }
            Console.WriteLine("a 的值是 {0}", a);
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
a 大于 20
a 的值是 100
```

## if...else if...else 语句

一个 **if** 语句后可跟一个可选的 **else if...else** 语句，这可用于测试多种条件。

当使用 if...else if...else 语句时，以下几点需要注意：

- 一个 if 后可跟零个或一个 else，它必须在任何一个 else if 之后。
- 一个 if 后可跟零个或多个 else if，它们必须在 else 之前。
- 一旦某个 else if 匹配成功，其他的 else if 或 else 将不会被测试。

### 语法

C# 中的 **if...else if...else** 语句的语法：

```c#
if(boolean_expression 1)
{
   /* 当布尔表达式 1 为真时执行 */
}
else if( boolean_expression 2)
{
   /* 当布尔表达式 2 为真时执行 */
}
else if( boolean_expression 3)
{
   /* 当布尔表达式 3 为真时执行 */
}
else 
{
   /* 当上面条件都不为真时执行 */
}

```

### 实例

```c#
using System;

namespace DecisionMaking
{
    
    class Program
    {
        static void Main(string[] args)
        {

            /* 局部变量定义 */
            int a = 100;

            /* 检查布尔条件 */
            if (a == 10)
            {
                /* 如果 if 条件为真，则输出下面的语句 */
                Console.WriteLine("a 的值是 10");
            }
            else if (a == 20)
            {
                /* 如果 else if 条件为真，则输出下面的语句 */
                Console.WriteLine("a 的值是 20");
            }
            else if (a == 30)
            {
                /* 如果 else if 条件为真，则输出下面的语句 */
                Console.WriteLine("a 的值是 30");
            }
            else
            {
                /* 如果上面条件都不为真，则输出下面的语句 */
                Console.WriteLine("没有匹配的值");
            }
            Console.WriteLine("a 的准确值是 {0}", a);
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
没有匹配的值
a 的准确值是 100
```

##  三元表达式

在 C# 里，三元表达式也叫条件运算符，它是一种简洁的条件判断结构，能够根据给定条件的值来返回不同的结果。其基本语法如下：

```c#
condition ? expression1 : expression2;
```

### 语法解释

- `condition`：这是一个布尔表达式，会对其进行求值，结果为 `true` 或者 `false`。

- `expression1`：当 `condition` 的结果为 `true` 时，返回此表达式的值。

- `expression2`：当 `condition` 的结果为 `false` 时，返回此表达式的值。

- ### 示例代码

  ```c#
  using System;
  
  class Program
  {
      static void Main()
      {
          int num = 10;
          string result = num > 5 ? "数字大于 5" : "数字小于等于 5";
          Console.WriteLine(result);
      }
  }
  ```

  ### 代码解释

  在这个示例中，先定义了一个整数变量 `num` 并赋值为 10。接着使用三元表达式来判断 `num` 是否大于 5。因为 `num` 大于 5，所以条件 `num > 5` 的结果为 `true`，那么就会返回 `expression1` 的值，也就是字符串 `"数字大于 5"`，最后将这个结果输出。

  三元表达式通常用于简化简单的 `if-else` 语句，让代码更加简洁易读。不过，若条件判断较为复杂，还是建议使用 `if-else` 语句，以保证代码的可读性和可维护性。

# 异常捕获

在 C# 中，异常捕获是一种处理程序运行时错误的机制，它允许你在代码中捕获并处理可能出现的异常，从而避免程序因未处理的异常而崩溃。C# 提供了 `try-catch-finally` 语句块来实现异常捕获和处理。下面为你详细介绍：

### 基本语法

```csharp
try
{
    // 可能会抛出异常的代码
}
catch (ExceptionType1 ex1)
{
    // 处理 ExceptionType1 类型的异常
}
catch (ExceptionType2 ex2)
{
    // 处理 ExceptionType2 类型的异常
}
finally
{
    // 无论是否发生异常，都会执行的代码
}
```

- **`try` 块**：包含可能会抛出异常的代码。
- **`catch` 块**：用于捕获并处理特定类型的异常。可以有多个 `catch` 块，每个块处理不同类型的异常。
- **`finally` 块**：可选的，无论是否发生异常，`finally` 块中的代码都会执行。

### 示例代码

```csharp
using System;

class Program
{
    static void Main()
    {
        try
        {
            // 尝试将字符串转换为整数，可能会抛出 FormatException 异常
            string input = "abc";
            int number = int.Parse(input);
            Console.WriteLine($"转换后的数字是: {number}");
        }
        catch (FormatException ex)
        {
            // 处理 FormatException 异常
            Console.WriteLine($"输入格式错误: {ex.Message}");
        }
        catch (Exception ex)
        {
            // 处理其他类型的异常
            Console.WriteLine($"发生未知异常: {ex.Message}");
        }
        finally
        {
            // 无论是否发生异常，都会执行的代码
            Console.WriteLine("程序结束。");
        }
    }
}
```

### 代码解释

1. **`try` 块**：尝试将字符串 `"abc"` 转换为整数，由于 `"abc"` 不是有效的整数格式，`int.Parse` 方法会抛出 `FormatException` 异常。
2. **`catch (FormatException ex)` 块**：捕获 `FormatException` 异常，并输出错误信息。
3. **`catch (Exception ex)` 块**：捕获其他类型的异常，并输出未知异常信息。
4. **`finally` 块**：无论是否发生异常，都会输出 "程序结束。"。

### 捕获特定异常

你可以根据不同的异常类型编写不同的 `catch` 块来处理特定的异常。例如，在进行文件操作时，可能会抛出 `FileNotFoundException` 异常：

```csharp
using System;
using System.IO;

class Program
{
    static void Main()
    {
        try
        {
            // 尝试打开一个不存在的文件
            string filePath = "nonexistentfile.txt";
            string content = File.ReadAllText(filePath);
            Console.WriteLine(content);
        }
        catch (FileNotFoundException ex)
        {
            // 处理文件未找到异常
            Console.WriteLine($"文件未找到: {ex.Message}");
        }
        catch (Exception ex)
        {
            // 处理其他类型的异常
            Console.WriteLine($"发生未知异常: {ex.Message}");
        }
    }
}
```

### 抛出异常

在某些情况下，你可能需要手动抛出异常。可以使用 `throw` 关键字来抛出异常：

```csharp
using System;

class Program
{
    static int Divide(int a, int b)
    {
        if (b == 0)
        {
            // 手动抛出 DivideByZeroException 异常
            throw new DivideByZeroException("除数不能为零。");
        }
        return a / b;
    }

    static void Main()
    {
        try
        {
            int result = Divide(10, 0);
            Console.WriteLine($"结果: {result}");
        }
        catch (DivideByZeroException ex)
        {
            // 处理除零异常
            Console.WriteLine($"除零错误: {ex.Message}");
        }
    }
}
```

在上述代码中，`Divide` 方法检查除数是否为零，如果为零，则手动抛出 `DivideByZeroException` 异常。在 `Main` 方法中，使用 `try-catch` 块捕获并处理该异常。

#  switch 语句

一个 **switch** 语句允许测试一个变量等于多个值时的情况。每个值称为一个 case，且被测试的变量会对每个 **switch case** 进行检查。

## 语法

C# 中 **switch** 语句的语法：

```c#
switch(expression){
    case constant-expression  :
       statement(s);
       break; 
    case constant-expression  :
       statement(s);
       break; 
  
    /* 您可以有任意数量的 case 语句 */
    default : /* 可选的 */
       statement(s);
       break; 
}
```

**switch** 语句必须遵循下面的规则：

- **switch** 语句中的 **expression** 必须是一个整型或枚举类型，或者是一个 class 类型，其中 class 有一个单一的转换函数将其转换为整型或枚举类型。
- 在一个 switch 中可以有任意数量的 case 语句。每个 case 后跟一个要比较的值和一个冒号。
- case 的 **constant-expression** 必须与 switch 中的变量具有相同的数据类型，且必须是一个常量。
- 当被测试的变量等于 case 中的常量时，case 后跟的语句将被执行，直到遇到 **break** 语句为止。
- 当遇到 **break** 语句时，switch 终止，控制流将跳转到 switch 语句后的下一行。
- 不是每一个 case 都需要包含 **break**。如果 case 语句为空，则可以不包含 **break**，控制流将会 *继续* 后续的 case，直到遇到 break 为止。
- C# 不允许从一个 case 部分继续执行到下一个 case 部分。如果 case 语句中有已经执行，则必须包含 **break** 或其他跳转语句。
- 一个 **switch** 语句可以有一个可选的 **default** 语句，在 switch 的结尾。default 语句用于在上面所有 case 都不为 true 时执行的一个任务。default 也需要包含 **break** 语句，这是一个良好的习惯。
- C# 不支持从一个 case 标签显式贯穿到另一个 case 标签。如果要使 C# 支持从一个 case 标签显式贯穿到另一个 case 标签，可以使用 goto 一个 switch-case 或 goto default。

## 实例1

以下实例用于判断当前是星期几：

```c#
using System;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      int day = 4;
      switch (day) 
      {
        case 1:
          Console.WriteLine("Monday");
          break;
        case 2:
          Console.WriteLine("Tuesday");
          break;
        case 3:
          Console.WriteLine("Wednesday");
          break;
        case 4:
          Console.WriteLine("Thursday");
          break;
        case 5:
          Console.WriteLine("Friday");
          break;
        case 6:
          Console.WriteLine("Saturday");
          break;
        case 7:
          Console.WriteLine("Sunday");
          break;
      }    
    }
  }
}
```

执行结果根据当天日期有所不同，我这里执行这天的结果为：

```
Thursday
```

## 实例2

包含了 **default** 语句：

```c#
using System;

namespace DecisionMaking
{
    
    class Program
    {
        static void Main(string[] args)
        {
            /* 局部变量定义 */
            char grade = 'B';

            switch (grade)
            {
                case 'A':
                    Console.WriteLine("很棒！");
                    break;
                case 'B':
                    Console.WriteLine("也很棒！");
                case 'C':
                    Console.WriteLine("做得好");
                    break;
                case 'D':
                    Console.WriteLine("您通过了");
                    break;
                case 'F':
                    Console.WriteLine("最好再试一下");
                    break;
                default:
                    Console.WriteLine("无效的成绩");
                    break;
            }
            Console.WriteLine("您的成绩是 {0}", grade);
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```
做得好
您的成绩是 B
```

## 嵌套 switch 语句

您可以把一个 **switch** 作为一个外部 **switch** 的语句序列的一部分，即可以在一个 **switch** 语句内使用另一个 **switch** 语句。即使内部和外部 switch 的 case 常量包含共同的值，也没有矛盾。

### 语法

C# 中 **嵌套 switch** 语句的语法：

```c#
switch(ch1) 
{
   case 'A': 
      printf("这个 A 是外部 switch 的一部分" );
      switch(ch2) 
      {
         case 'A':
            printf("这个 A 是内部 switch 的一部分" );
            break;
         case 'B': /* 内部 B case 代码 */
      }
      break;
   case 'B': /* 外部 B case 代码 */
}
```

### 实例

```c#
using System;

namespace DecisionMaking
{
    
    class Program
    {
        static void Main(string[] args)
        {
            int a = 100;
            int b = 200;

            switch (a)
            {
                case 100:
                    Console.WriteLine("这是外部 switch 的一部分");
                    switch (b)
                    {
                        case 200:
                        Console.WriteLine("这是内部 switch 的一部分");
                        break;
                    }
                    break;
            }
            Console.WriteLine("a 的准确值是 {0}", a);
            Console.WriteLine("b 的准确值是 {0}", b);
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
这是外部 switch 的一部分
这是内部 switch 的一部分
a 的准确值是 100
b 的准确值是 200
```

# 循环

## 循环类型

C# 提供了以下几种循环类型。点击链接查看每个类型的细节。

| 循环类型                                                     | 描述                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [while 循环](https://www.runoob.com/csharp/csharp-while-loop.html) | 当给定条件为真时，重复语句或语句组。它会在执行循环主体之前测试条件。 |
| [for/foreach 循环](https://www.runoob.com/csharp/csharp-for-loop.html) | 多次执行一个语句序列，简化管理循环变量的代码。               |
| [do...while 循环](https://www.runoob.com/csharp/csharp-do-while-loop.html) | 除了它是在循环主体结尾测试条件外，其他与 while 语句类似。    |
| [嵌套循环](https://www.runoob.com/csharp/csharp-nested-loops.html) | 您可以在 while、for 或 do..while 循环内使用一个或多个循环。  |

## while 循环

只要给定的条件为真，C# 中的 **while** 循环语句会重复执行一个目标语句。

### 语法

C# 中 **while** 循环的语法：

```
while(condition)
{
   statement(s);
}
```

在这里，**statement(s)** 可以是一个单独的语句，也可以是几个语句组成的代码块。**condition** 可以是任意的表达式，当为任意非零值时都为真。当条件为真时执行循环。

当条件为假时，程序流将继续执行紧接着循环的下一条语句。

在这里，*while* 循环的关键点是循环可能一次都不会执行。当条件被测试且结果为假时，会跳过循环主体，直接执行紧接着 while 循环的下一条语句。

### 实例1

```c#
using System;

namespace Loops
{
    
    class Program
    {
        static void Main(string[] args)
        {
            /* 局部变量定义 */
            int a = 10;

            /* while 循环执行 */
            while (a < 20)
            {
                Console.WriteLine("a 的值： {0}", a);
                a++;
            }
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
a 的值： 10
a 的值： 11
a 的值： 12
a 的值： 13
a 的值： 14
a 的值： 15
a 的值： 16
a 的值： 17
a 的值： 18
a 的值： 19
```

### 实例2

```c#
using System;

namespace DataTypeApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("请输入班级人数");
            int count = Convert.ToInt32(Console.ReadLine());
            int sum = 0; //存放总成绩
            int i = 1;//声明一个循环变量用来记录循环次数
            while (i <= count)
            {
                Console.WriteLine("请输入第{0}个学员的学习成绩：", i);
                int score = Convert.ToInt32(Console.ReadLine());
                //表示把每一个学员的成绩累加到总成绩当中
                sum += score;
                i++;
            }
            Console.WriteLine("总成绩为{0},平均成绩为{1}",sum,sum/count);


        }
    }
}


```

## do...while 循环

不像 **for** 和 **while** 循环，它们是在循环头部测试循环条件。**do...while** 循环是在循环的尾部检查它的条件。

**do...while** 循环与 while 循环类似，但是 do...while 循环会确保至少执行一次循环。

### 语法

C# 中 **do...while** 循环的语法：

```c#
do
{
   statement(s);

}while( condition );
```

请注意，条件表达式出现在循环的尾部，所以循环中的 statement(s) 会在条件被测试之前至少执行一次。

如果条件为真，控制流会跳转回上面的 do，然后重新执行循环中的 statement(s)。这个过程会不断重复，直到给定条件变为假为止。

```c#
using System;

namespace Loops
{
    
    class Program
    {
        static void Main(string[] args)
        {
            /* 局部变量定义 */
            int a = 10;

            /* do 循环执行 */
            do
            {
               Console.WriteLine("a 的值： {0}", a);
                a = a + 1;
            } while (a < 20);

            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
a 的值： 10
a 的值： 11
a 的值： 12
a 的值： 13
a 的值： 14
a 的值： 15
a 的值： 16
a 的值： 17
a 的值： 18
a 的值： 19
```

## for循环

一个 **for** 循环是一个允许您编写一个执行特定次数的循环的重复控制结构。

### 语法

C# 中 **for** 循环的语法：

```c#
for ( init; condition; increment )
{
   statement(s);
}
```

下面是 for 循环的控制流：

1. **init** 会首先被执行，且只会执行一次。这一步允许您声明并初始化任何循环控制变量。您也可以不在这里写任何语句，只要有一个分号出现即可。

2. 接下来，会判断 **condition**。如果为真，则执行循环主体。如果为假，则不执行循环主体，且控制流会跳转到紧接着 for 循环的下一条语句。

3. 在执行完 for 循环主体后，控制流会跳回上面的 **increment** 语句。该语句允许您更新循环控制变量。该语句可以留空，只要在条件后有一个分号出现即可。

4. 条件再次被判断。如果为真，则执行循环，这个过程会不断重复（循环主体，然后增加步值，再然后重新判断条件）。在条件变为假时，for 循环终止。

   ```c#
   using System;
   
   namespace Loops
   {
       
       class Program
       {
           static void Main(string[] args)
           {
               /* for 循环执行 */
               for (int a = 10; a < 20; a = a + 1)
               {
                   Console.WriteLine("a 的值： {0}", a);
               }
               Console.ReadLine();
           }
       }
   }
   ```

   当上面的代码被编译和执行时，它会产生下列结果：

   ```
   a 的值： 10
   a 的值： 11
   a 的值： 12
   a 的值： 13
   a 的值： 14
   a 的值： 15
   a 的值： 16
   a 的值： 17
   a 的值： 18
   a 的值： 19
   ```

## C# continue 语句

C# 中的 **continue** 语句有点像 **break** 语句。但它不是强迫终止，continue 会跳过当前循环中的代码，强迫开始下一次循环。

对于 **for** 循环，**continue** 语句会导致执行条件测试和循环增量部分。对于 **while** 和 **do...while** 循环，**continue** 语句会导致程序控制回到条件测试上。

C# 中 **continue** 语句的语法：

```c#
continue;
```

代码

```c#
class Program
{
    static void Main(string[] args)
    {
        for(int i = 1; i <= 10; i++)
        {
            if (i == 4)//i等于4的时候跳过
            {
                continue;
            }
            Console.WriteLine(i);
        }
    }  
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
1
2
3
5
6
7
8
9
10
```

# break语句

C# 中 **break** 语句有以下两种用法：

1. 当 **break** 语句出现在一个循环内时，循环会立即终止，且程序流将继续执行紧接着循环的下一条语句。
2. 它可用于终止 **switch** 语句中的一个 case。

如果您使用的是嵌套循环（即一个循环内嵌套另一个循环），break 语句会停止执行最内层的循环，然后开始执行该块之后的下一行代码。

## 语法

C# 中 **break** 语句的语法：

```
break;
```

```c#
using System;

namespace Loops
{
    
    class Program
    {
        static void Main(string[] args)
        {
            /* 局部变量定义 */
            int a = 10;

            /* while 循环执行 */
            while (a < 20)
            {
                Console.WriteLine("a 的值： {0}", a);
                a++;
                if (a > 15)
                {
                    /* 使用 break 语句终止 loop */
                    break;
                }
            }
            Console.ReadLine();
        }
    }
}
```

当上面的代码被编译和执行时，它会产生下列结果：

```c#
a 的值： 10
a 的值： 11
a 的值： 12
a 的值： 13
a 的值： 14
a 的值： 15
```

# Random随机数

在 C# 里，`Random` 类主要用于生成伪随机数。以下为你详细介绍其使用方法：

### 1. 创建 `Random` 类的实例

在使用 `Random` 类生成随机数之前，需要先创建它的一个实例。示例如下：csharp

```csharp
Random random = new Random();
```

### 2. 生成随机整数

可以使用 `Next` 方法来生成随机整数，它有几种不同的重载形式：

#### 2.1 生成一个非负随机整数

```csharp
int randomNumber = random.Next();
```

这种方式会生成一个大于等于 0 的随机整数。

#### 2.2 生成一个指定范围内的随机整数

```csharp
int minValue = 1;
int maxValue = 10;
int randomInRange = random.Next(minValue, maxValue);
```

上述代码会生成一个大于等于 `minValue` 且小于 `maxValue` 的随机整数。

### 3. 生成随机双精度浮点数

使用 `NextDouble` 方法可以生成一个大于等于 0.0 且小于 1.0 的随机双精度浮点数：

```csharp
double randomDouble = random.NextDouble();
```

### 完整示例代码

以下是一个完整的 C# 程序，展示了如何使用 `Random` 类生成随机整数和随机双精度浮点数：

```csharp
using System;

class Program
{
    static void Main()
    {
        // 创建 Random 类的实例
        Random random = new Random();

        // 生成一个非负随机整数
        int randomNumber = random.Next();
        Console.WriteLine($"生成的非负随机整数: {randomNumber}");

        // 生成一个指定范围内的随机整数
        int minValue = 1;
        int maxValue = 10;
        int randomInRange = random.Next(minValue, maxValue);
        Console.WriteLine($"生成的 {minValue} 到 {maxValue} 之间的随机整数: {randomInRange}");

        // 生成一个随机双精度浮点数
        double randomDouble = random.NextDouble();
        Console.WriteLine($"生成的随机双精度浮点数: {randomDouble}");
    }
}
```

此程序先创建了 `Random` 类的一个实例，接着分别使用 `Next` 和 `NextDouble` 方法生成随机整数和随机双精度浮点数，最后将这些随机数输出到控制台。

### 注意事项

- 由于 `Random` 类是基于种子值生成伪随机数的，若在短时间内多次创建 `Random` 类的实例，可能会得到相同的随机数序列。为避免这种情况，建议在整个程序中只创建一个 `Random` 类的实例。

- 若需要更高质量的随机数，可考虑使用 `System.Security.Cryptography.RandomNumberGenerator` 类。


# C#枚举

枚举是一组命名整型常量。枚举类型是使用 **enum** 关键字声明的。

C# 枚举是值类型。换句话说，枚举包含自己的值，且不能继承或传递继承。

```c#
using System;
using System.Diagnostics;

namespace DataTypeApplication
{
    public enum Sesons
    {
        春,
        夏,
        秋,
        冬,
    }
    class Program
    {
        static void Main(string[] args)
        {
            Sesons s = Sesons.春;
            Console.WriteLine(s);//春
        }
    }
}
```

## 枚举练习

```c#
using System;  // 引入基础系统命名空间
using System.Diagnostics;  // 引入诊断相关功能（虽然本例中未使用）

namespace DataTypeApplication  // 定义命名空间
{
    // 定义QQ状态枚举
    public enum QQState
    {
        OnLine = 1,   // 在线状态，显式赋值为1
        OffLine,      // 离线状态，自动赋值为2
        Leave,        // 离开状态，自动赋值为3
        Busy,         // 忙碌状态，自动赋值为4
        Qme,         // Q我吧状态，自动赋值为5
    }

    class Program  // 主程序类
    {
        static void Main(string[] args)  // 程序入口点
        {
            // 枚举练习：处理用户选择的QQ状态
            
            // 显示状态选择菜单
            Console.WriteLine("请选择你的QQ在线状态 1--OnLine 2--OffLine 3--Leave 4--Busy 5--Qme");
            
            // 读取用户输入
            string input = Console.ReadLine();
            
            // 使用switch处理不同输入
            switch(input)
            {
                case "1":
                    // 将字符串"1"转换为QQState.OnLine枚举值
                    QQState s1 = (QQState)Enum.Parse(typeof(QQState), input);
                    Console.WriteLine("你选择的状态是{0}", s1);
                    break;
                case "2":
                    QQState s2 = (QQState)Enum.Parse(typeof(QQState), input);
                    Console.WriteLine("你选择的状态是{0}", s2);
                    break;
                case "3":
                    QQState s3 = (QQState)Enum.Parse(typeof(QQState), input);
                    Console.WriteLine("你选择的状态是{0}", s3);
                    break;
                case "4":
                    QQState s4 = (QQState)Enum.Parse(typeof(QQState), input);
                    Console.WriteLine("你选择的状态是{0}", s4);
                    break;
                case "5":
                    QQState s5 = (QQState)Enum.Parse(typeof(QQState), input);
                    Console.WriteLine("你选择的状态是{0}", s5);
                    break;
            }
        }
    }
}
```

# C# 结构体（Struct）

在 C# 中，结构体（struct）是一种值类型（value type），用于组织和存储相关数据。

在 C# 中，结构体是值类型数据结构，这样使得一个单一变量可以存储各种数据类型的相关数据。

**struct** 关键字用于创建结构体。

结构体是用来代表一个记录，假设您想跟踪图书馆中书的动态，您可能想跟踪每本书的以下属性：

- Title
- Author
- Subject
- Book ID

```c#
// 定义一个名为 Person 的结构体，用于表示一个人的基本信息
// 结构体是值类型，通常用于封装少量相关的数据
public struct Person
{
    // 定义一个公共的字符串类型字段 _name，用于存储人的姓名
    public string _name;
    // 定义一个公共的整数类型字段 _age，用于存储人的年龄
    public int _age;
    // 定义一个公共的字符类型字段 _gender，用于存储人的性别
    public char _gender;
}

// 定义一个名为 Program 的类，这是 C# 程序的主类
class Program
{
    // 定义程序的入口点方法 Main
    // static 表示这是一个静态方法，无需创建 Program 类的实例即可调用
    // void 表示该方法没有返回值
    // string[] args 是命令行参数数组，用于接收程序启动时传递的参数
    static void Main(string[] args)
    {
        // 声明一个 Person 类型的变量 zsPerson，用于表示一个名为张三的人
        Person zsPerson;
        // 给 zsPerson 的 _name 字段赋值为 "张三"
        zsPerson._name = "张三";
        // 给 zsPerson 的 _age 字段赋值为 18
        zsPerson._age = 18;
        // 给 zsPerson 的 _gender 字段赋值为 '男'
        zsPerson._gender = '男';

        // 声明一个 Person 类型的变量 lsPerson，用于表示一个名为李四的人
        Person lsPerson;
        // 给 lsPerson 的 _name 字段赋值为 "李四"
        lsPerson._name = "李四";
        // 给 lsPerson 的 _age 字段赋值为 22
        lsPerson._age = 22;
        // 给 lsPerson 的 _gender 字段赋值为 '女'
        lsPerson._gender = '女';

        // 使用 Console.WriteLine 方法将 lsPerson 的 _name 字段的值输出到控制台
        Console.WriteLine(lsPerson._name);
    }
}
```

这段代码的主要功能是定义一个 `Person` 结构体来表示人的基本信息，然后在 `Main` 方法中创建两个 `Person` 结构体的实例，分别表示 "张三" 和 "李四"，最后将 "李四" 的姓名输出到控制台。

# C# 数组（Array）

数组是一个存储相同类型元素的固定大小的顺序集合。数组是用来存储数据的集合，通常认为数组是一个同一类型变量的集合。

声明数组变量并不是声明 number0、number1、...、number99 一个个单独的变量，而是声明一个就像 numbers 这样的变量，然后使用 numbers[0]、numbers[1]、...、numbers[99] 来表示一个个单独的变量。数组中某个指定的元素是通过索引来访问的。

所有的数组都是由连续的内存位置组成的。最低的地址对应第一个元素，最高的地址对应最后一个元素。

## 初始化数组

声明一个数组不会在内存中初始化数组。当初始化数组变量时，您可以赋值给数组。

数组是一个引用类型，所以您需要使用 **new** 关键字来创建数组的实例。

例如：

```c#
double[] balance = new double[10];
```

## 赋值给数组

您可以通过使用索引号赋值给一个单独的数组元素，比如：

```c#
double[] balance = new double[10];
balance[0] = 4500.0;
```

您可以在声明数组的同时给数组赋值，比如：

```c#
double[] balance = { 2340.0, 4523.69, 3421.0};
```

您也可以创建并初始化一个数组，比如：

```c#
int [] marks = new int[5]  { 99,  98, 92, 97, 95};
```

在上述情况下，你也可以省略数组的大小，比如：

```c#
int [] marks = new int[]  { 99,  98, 92, 97, 95};
```

您也可以赋值一个数组变量到另一个目标数组变量中。在这种情况下，目标和源会指向相同的内存位置：

```c#
int [] marks = new int[]  { 99,  98, 92, 97, 95};
int[] score = marks;
```

当您创建一个数组时，C# 编译器会根据数组类型隐式初始化每个数组元素为一个默认值。例如，int 数组的所有元素都会被初始化为 0。

## 访问数组元素

元素是通过带索引的数组名称来访问的。这是通过把元素的索引放置在数组名称后的方括号中来实现的。例如：

```c#
double salary = balance[9];
```

## 实例1

```c#
using System;
using System.Diagnostics;

namespace DataTypeApplication
{

    class Program
    {
        static void Main(string[] args)
        {
            //int[] balance = new double[10]; 和下面是一样的
            int[] nums = { 1, 34, 3, 4, 5, 6, 7, 8, 9, 0 };
            int max = 0;
            int min = 0;
            
            for (int i = 0; i < nums.Length; i++)
            {
                if(nums[i]>max)
                {
                    max = nums[i];
                }
                if (nums[i] < min)
                {
                    min = nums[i];
                }
                
                
            }
            Console.WriteLine("这个数组最大值是{0},最小值是{1}", max, min);
        }
    }
}


```

## 实例2

```c#
using System;
using System.Diagnostics;

namespace DataTypeApplication
{

    class Program
    {
        static void Main(string[] args)
        {
            string[] names = { "李白", "貂蝉", "鲁班", "典韦", "韩信" };
            //不想要最后的值for (int i = 0; i < names.Length-1; i++)
            for (int i = 0; i < names.Length; i++)
            {
                Console.WriteLine(names[i]);
            }
            
        }
    }
}

```

## 实例3

```c#
using System;
using System.Diagnostics;

namespace DataTypeApplication
{

    class Program
    {
        static void Main(string[] args)
        {
            //如果元素是正数则将这个位置的元素的值+1
            //如果元素是负数则将这个位置的元素的值-1,如果是0则不变
            int[] nums = { 1, -2, 3, -4, 5, -6, 0 };
            //对每一个元素进行判断
            for (int i = 0; i < nums.Length; i++)
            {
                if (nums[i] > 0)
                {
                    nums[i] += 1;
                }
                else if (nums[i] < 0) 
                {
                    nums[i] -= 1;
                }
                else
                {

                }
            }
            for (int i = 0; i < nums.Length; i++)
            {
                Console.WriteLine(nums[i]);
            }

        }
    }
}


```

结果

```c#
2
-3
4
-5
6
-7
0
```

## 冒泡排序

```c#
// 引入 System 命名空间，该命名空间包含了许多常用的类型和功能
using System;
// 引入 System.Diagnostics 命名空间，不过在本代码中未实际使用
using System.Diagnostics;

// 定义一个名为 DataTypeApplication 的命名空间
namespace DataTypeApplication
{
    // 定义一个名为 Program 的类
    class Program
    {
        // 程序的入口点，Main 方法
        static void Main(string[] args)
        {
            // 定义一个整型数组 nums，并初始化其元素
            int[] nums = { 9, 4, 3, 13, 1, 6, 11 };

            // 外层循环控制排序的轮数，总共需要进行数组长度减 1 轮
            for (int i = 0; i < nums.Length - 1; i++)
            {
                // 内层循环用于比较相邻元素并进行交换
                for (int j = 0; j < nums.Length - 1 - i; j++)
                {
                    // 如果当前元素大于下一个元素
                    if (nums[j] > nums[j + 1])
                    {
                        // 使用临时变量 temp 来交换两个元素的值
                        int temp = nums[j];
                        nums[j] = nums[j + 1];
                        nums[j + 1] = temp;
                    }
                }
            }

            // 遍历排序后的数组并输出每个元素
            for (int i = 0; i < nums.Length; i++)
            {
                Console.WriteLine(nums[i]);
            }

            // 等待用户按下任意键，防止控制台窗口立即关闭
            Console.ReadKey();
        }
    }
}
```

结果

```c#
1
3
4
6
9
11
13
```

