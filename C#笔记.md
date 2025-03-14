# C#中的注释

在C#中，注释用于解释代码，提高代码的可读性，或临时禁用某些代码。C#支持三种注释方式：

### 1. 单行注释
使用 `//` 进行单行注释，从 `//` 开始到行末的内容都会被编译器忽略。

```c#
// 这是一个单行注释
int x = 10; // 初始化变量x为10
```

### 2. 多行注释
使用 `/*` 和 `*/` 进行多行注释，`/*` 和 `*/` 之间的所有内容都会被编译器忽略。

```c#
/* 这是一个多行注释
   可以跨越多行 */
int y = 20; /* 初始化变量y为20 */
```

### 3. XML文档注释
使用 `///` 进行XML文档注释，通常用于生成代码文档。这些注释可以包含XML标签，如 `<summary>`、`<param>`、`<returns>` 等。

```c#
/// <summary>
/// 这是一个方法的XML文档注释
/// </summary>
/// <param name="a">参数a的说明</param>
/// <param name="b">参数b的说明</param>
/// <returns>返回值的说明</returns>
public int Add(int a, int b)
{
    return a + b;
}
```

### 注释的使用场景
- **解释代码**：帮助其他开发者理解代码的意图。
- **调试代码**：临时禁用某些代码段以进行调试。
- **生成文档**：使用XML文档注释生成API文档。

### 注意事项
- 注释应简洁明了，避免过度注释。
- 及时更新注释，确保注释与代码一致。
- 避免使用注释来注释掉不再使用的代码，应直接删除。

通过合理使用注释，可以提高代码的可维护性和可读性。



# C#常用快捷键

| 快捷键                  | 方法                         |
| ----------------------- | ---------------------------- |
| **Ctrl+K+D**            | **快速对齐代码**             |
| **Ctrl+Z**              | **撤销**                     |
| **Ctrl+S**              | **保存（一定要经常保存！）** |
| **Ctrl+J**              | **快速弹出智能提示**         |
| **Ctrl+K+C**            | **注释所选代码**             |
| **Ctr+K+U**             | **取消对所选代码的注释**     |
| **F1**                  | **转到帮助文档**             |
| **#Region和#EndRegion** | **折叠冗余代码**             |



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
