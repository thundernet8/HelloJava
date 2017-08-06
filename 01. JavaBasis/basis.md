## 数据类型

### 基本数据类型（8种）

**整型**
  * int - 4bytes - 32bits
  * short - 2bytes - 16bits
  * long - 8bytes - 64bits
  * byte - 1bytes - 8bits

```
**Java没有任何无符号类型(unsigned)
```

**浮点类型**
  * float - 4bytes - 32bits
  * double - 8bytes - 64bits

**char类型**

**boolean类型**

### 变量

**常量**

```
final int constantNum = 100;
```

## 运算符

### 位运算符

**`>>>`运算符用0填充高位，`>>`运算符用符号位填充高位，没有`<<<`运算符**

## 类型转换

**不要在boolean类型与数值类型之间进行强制类型转换，可以使用条件表达式`int num = b ? 1 : 0`**

## 字符串
**不可变字符串**

要修改Java的字符串，需按如下操作:
```
String greeting = "Hello"; // 原始字符串
greeting = greeting.substring(0,3) + "!"; // 重新拼接新字符串并赋值给原字符串变量
```

***不要认为字符串是字符型数组***
```
char greeting[] = "Hello"; // 错误的认识
```

***Java中字符串更像是`char*`指针***
```
char* greeting = "Hello";
```

***比较两个字符串是否相等***

应该使用
```
str1.equals(str2);
```
而不能使用
```
str1 == str2;
```

***可以利用`StringBuilder`构建字符串，代替效率较低的拼接字符串方法***

## 输入输出

### Scanner
```
import java.util.*;
...
Scanner in = new Scanner(Systen.in);
String input = in.nextLine();
...
```

### Console
要实现控制台不可见输入，如输入密码等场景，可以使用SE6引入的`Console`类
```
Console cons = System.console();
String passwd = cons.readPassword("Password: ");
```