### What is lotus?  
*lotus* is a statically typed, compiled programming language designed by Bittu. It combines the simplicity of Python with the performance of C/C++ and is set to be released in the future.  

### Key Applications  
*lotus* is versatile and can be used for  
- **Web Development** Build robust server-side applications.  
- **Software Development** Create efficient, scalable software.  
- **Mathematics and Big Data** Perform complex computations and handle large datasets.  
- **System Scripting** Automate tasks and manage system operations.  
- **Machine Learning and AI** Develop ML models and AI-driven applications.  
- **Embedded Systems** Write performant code for hardware devices.  

### What can *lotus* do?  
*lotus* is designed to handle a wide range of programming tasks  
- **Web Applications** Develop web servers and backend systems.  
- **Workflow Integration** Build tools and scripts that integrate seamlessly with other software.  
- **Database Connectivity** Read from and write to databases efficiently.  
- **File Manipulation** Perform file-based operations for various workflows.  
- **Big Data and Complex Math** Process and analyze massive datasets.  
- **Prototyping and Production** Quickly prototype ideas and deploy production-ready applications.  

### Why Choose lotus?  
*lotus* stands out with these features  
- **Cross-Platform Support** Works seamlessly across Windows, Mac, Linux, Raspberry Pi, and more.
- **Simple Syntax** Offers a clean, intuitive syntax inspired by Python, making it easy to learn and use.
- **Code Efficiency** Allows developers to write concise, readable code, reducing boilerplate.
- **Object Oriented** Supports object oriented programming (OOP) style.
- **Performance** Delivers near-C/C++ performance, suitable for resource-intensive tasks.
- **Static Typing** Enables safer code with fewer runtime errors, thanks to strong type-checking, and null safety.


Here's a table explaining the usage of each keyword in your language, **Lotus**, along with examples:

| **Keyword**      | **Description**                                                                                   | **Example**                                                                                  |
|-------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| `let`            | Declares immutable variables.                                                                     | `let x = 10`                                                                                |
| `const`          | Declares compile-time constants.                                                                  | `const pi = 3.14`                                                                           |
| `static`         | Declares static members in a class or maintains state across function calls.                      | `static counter = 0`                                                                        |
| `i8`, `u8`, etc. | Signed (`i`) and unsigned (`u`) integer types of varying bit sizes.                               | `let smallNumber i8 = 127`                                                                  |
| `f32`, `f64`     | Floating-point types of varying precision.                                                        | `let pi f32 = 3.14159`                                                                      |
| `bool`           | Boolean type representing `true` or `false`.                                                      | `let isOpen bool = true`                                                                    |
| `any`            | Type that can hold any value.                                                                     | `let data any = 42`                                                                         |
| `error`          | Represents error types for error handling.                                                        | `throw error("Something went wrong")`                                                      |
| `char`, `str`    | `char` is a single character; `str` is a string of characters.                                    | `let initial char = 'A'; let name str = "Alice"`                                           |
| `tuple`          | Immutable ordered collection of elements of varying types.                                        | `let person tuple = ("Alice", 25)`                                                         |
| `array`          | Fixed-size ordered collection of elements.                                                        | `let days array[str, 7] = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]`                |
| `dict`           | Key-value pair collection.                                                                        | `let capitals dict[str, str] = {"USA": "Washington", "France": "Paris"}`                    |
| `set`            | Collection of unique elements.                                                                    | `let uniqueNumbers set = {1, 2, 3}`                                                        |
| `true`, `false`  | Boolean literals.                                                                                 | `let isActive bool = true`                                                                  |
| `null`           | Represents the absence of a value.                                                                | `let optionalValue str? = null`                                                            |
| `if`, `else`     | Conditional statements.                                                                           | `if age > 18 { print("Adult") } else { print("Minor") }`                                   |
| `elif`           | "Else if" for multiple conditions.                                                                | `if x < 0 { ... } elif x == 0 { ... } else { ... }`                                        |
| `switch`, `case` | Multi-condition control structure.                                                                | `switch status { case 1: print("Active") default: print("Unknown") }`                      |
| `default`        | Default branch in `switch` when no case matches.                                                  | `switch x { case 1: ... default: ... }`                                                    |
| `fallthrough`    | Allows case to fall through to the next one in `switch`.                                          | `case 1: ... fallthrough case 2: ...`                                                     |
| `and`, `or`, `not`| Logical operators for combining or negating conditions.                                           | `if x > 0 and y > 0 { ... }`                                                               |
| `is`             | Checks type or identity.                                                                          | `if x is int { ... }`                                                                      |
| `for`, `while`   | Iterative control structures.                                                                     | `for i in range(0, 10) { ... } while count > 0 { ... }`                                    |
| `break`          | Exits a loop.                                                                                     | `if x > 5 { break }`                                                                       |
| `continue`       | Skips to the next iteration of the loop.                                                          | `if x % 2 == 0 { continue }`                                                               |
| `in`             | Checks membership or iterates over a collection.                                                  | `if "Alice" in names { ... }`                                                              |
| `try`, `catch`   | Error handling mechanism.                                                                         | `try { riskyFunction() } catch (e error) { print(e) }`                                     |
| `throw`          | Throws an error.                                                                                  | `throw error("Unexpected value")`                                                          |
| `def`            | Defines a function.                                                                               | `fn greet(name str): return "Hello, " + name`                                             |
| `return`         | Exits from a function and optionally returns a value.                                             | `return x + y`                                                                             |
| `defer`          | Schedules a statement to run at the end of the function scope.                                    | `defer { print("Done") }`                                                                  |
| `class`          | Defines a class.                                                                                  | `class Person { let name str; fn greet(): print("Hello, " + name) }`                      |
| `impl`           | Implements methods for a class or interface.                                                      | `impl Person { fn greet(): ... }`                                                         |
| `enum`           | Defines a type with a fixed set of constant values.                                               | `enum Color { Red, Blue, Green }`                                                          |
| `interface`      | Declares a contract for classes to implement.                                                     | `interface Drawable { fn draw(): void }`                                                 |
| `delete`         | Deletes an object or element.                                                                     | `delete list[index]`                                                                       |
| `new`            | Creates a new instance of a class.                                                                | `let obj = new Person()`                                                                   |
| `yield`          | Pauses a generator function and returns a value.                                                  | `yield x`                                                                                  |
| `import`, `as`   | Imports modules with optional aliasing.                                                           | `import math as m; let result = m.sqrt(16)`                                               |


### **Operators in *lotus***
Operators are essential components in any programming language, used to perform operations on variables and values. *lotus* supports a wide range of operators, including the ones found in Python, with a few additional ones for optimized programming. Below is a breakdown of the different types of operators available in *lotus*.

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
| `\|\|` or `or`  | Logical OR             | `True \|\| False` → `True` |
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

### **Bitwise Operators**
Bitwise operators perform operations on binary representations of integers.

| Operator | Description            | Example         |
|----------|------------------------|-----------------|
| `&`      | Bitwise AND            | `5 & 3` → `1`   |
| `\|`     | Bitwise OR             | `5 \| 3` → `7`  |
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

