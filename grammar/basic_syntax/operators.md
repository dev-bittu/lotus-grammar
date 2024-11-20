### **Operators in *mylang***
Operators are essential components in any programming language, used to perform operations on variables and values. *mylang* supports a wide range of operators, including the ones found in Python, with a few additional ones for optimized programming. Below is a breakdown of the different types of operators available in *mylang*.

---

### **Arithmetic Operators**
Arithmetic operators perform basic mathematical operations such as addition, subtraction, multiplication, and division.

| Operator | Description            | Example      |
|----------|------------------------|--------------|
| `+`      | Addition               | `5 + 3` → `8`|
| `-`      | Subtraction            | `5 - 3` → `2`|
| `*`      | Multiplication         | `5 * 3` → `15`|
| `/`      | Division               | `5 / 3` → `1.666`|
| `%`      | Modulo (remainder)     | `5 % 3` → `2` |
| `**`     | Exponentiation         | `2 ** 3` → `8` |

---

### **Comparison Operators**
Comparison operators are used to compare two values and return a boolean result.

| Operator | Description            | Example          |
|----------|------------------------|------------------|
| `==`     | Equal to               | `5 == 5` → `True`|
| `!=`     | Not equal to           | `5 != 3` → `True`|
| `>`      | Greater than           | `5 > 3` → `True` |
| `<`      | Less than              | `5 < 3` → `False`|
| `>=`     | Greater than or equal  | `5 >= 3` → `True`|
| `<=`     | Less than or equal     | `5 <= 3` → `False`|

---

### **Logical Operators**
Logical operators allow you to combine or negate conditions.

| Operator      | Description            | Example         |
|---------------|------------------------|-----------------|
| `&&` or `and` | Logical AND            | `True && False` → `False` |
| `||` or `or`  | Logical OR             | `True || False` → `True` |
| `!`  or `not` | Logical NOT            | `!True` → `False` |

---

### **Assignment Operators**
Assignment operators are used to assign values to variables.

| Operator | Description            | Example        |
|----------|------------------------|----------------|
| `:=`     | Assigns value          | `x := 5`        |
| `+=`     | Adds and assigns       | `x += 5` (equivalent to `x = x + 5`)|
| `-=`     | Subtracts and assigns  | `x -= 5` (equivalent to `x = x - 5`)|
| `*=`     | Multiplies and assigns | `x *= 5` (equivalent to `x = x * 5`)|
| `/=`     | Divides and assigns    | `x /= 5` (equivalent to `x = x / 5`)|
| `**=`    | Exponentiates and assigns | `x **= 5` (equivalent to `x = x ** 5`)|

---

### **Increment and Decrement Operators**
The increment (`i++`) and decrement (`--i`) operators are used to add or subtract `1` from a variable.

| Operator | Description            | Example        |
|----------|------------------------|----------------|
| `i++`    | Post-increment         | `i++` (value of `i` is increased by 1 after the expression) |
| `++i`    | Pre-increment          | `++i` (value of `i` is increased by 1 before the expression) |

*Note:* The increment and decrement operators are part of the *mylang* syntax for convenience and efficiency, similar to languages like C and Java.

---

### **Bitwise Operators**
Bitwise operators perform operations on binary representations of integers.

| Operator | Description            | Example         |
|----------|------------------------|-----------------|
| `&`      | Bitwise AND            | `5 & 3` → `1`   |
| `|`      | Bitwise OR             | `5 | 3` → `7`   |
| `^`      | Bitwise XOR            | `5 ^ 3` → `6`   |
| `~`      | Bitwise NOT            | `~5` → `-6`     |
| `<<`     | Left shift             | `5 << 1` → `10` |
| `>>`     | Right shift            | `5 >> 1` → `2`  |

---

### **Membership Operators**
Membership operators are used to test if a value is found in a sequence (like lists, tuples, sets, or strings).

| Operator | Description            | Example         |
|----------|------------------------|-----------------|
| `in`     | Checks if a value exists in a sequence | `'a' in "apple"` → `True` |
| `not in` | Checks if a value does not exist in a sequence | `'z' not in "apple"` → `True` |

---

### **Identity Operators**
Identity operators are used to check if two variables point to the same object in memory.

| Operator | Description            | Example        |
|----------|------------------------|----------------|
| `is`     | Checks if two variables point to the same object | `x is y` |
| `is not` | Checks if two variables do not point to the same object | `x is not y` |

---

### **Example Usage of All Operators**

```mylang
// Arithmetic Operators
x := 10 + 5  // 15
y := 10 - 5  // 5
z := 10 * 5  // 50

// Comparison Operators
a := 10
b := 5
print(a == b)  // False
print(a > b)   // True

// Logical Operators
flag := True
print(!flag)  // False
print(True && False)  // False
print(True || False)  // True

// Assignment Operators
x := 10
x += 5  // x = 15

// Increment and Decrement Operators
i := 10
i++   // i = 11 (post-increment)
++i   // i = 12 (pre-increment)

// Bitwise Operators
x := 5 & 3   // 1
y := 5 | 3   // 7

// Membership Operators
fruits := ["apple", "banana", "cherry"]
print("apple" in fruits)  // True
print("orange" not in fruits)  // True

// Identity Operators
x := 10
y := 10
print(x is y)  // True
```

---

This summary covers the most commonly used operators in *mylang*. With the flexibility provided by these operators, you can perform a wide range of operations on variables and values for more efficient and concise code.