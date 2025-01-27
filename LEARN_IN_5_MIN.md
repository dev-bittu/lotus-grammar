# Table of Contents
1. **What is Lotus?**  
2. **Key Applications**  
3. **What Can Lotus Do?**  
4. **Why Choose Lotus?**  
---
### Keywords and Operators
5. **Keywords**  
6. **Operators in Lotus**  
   - **Arithmetic Operators**  
   - **Comparison Operators**  
   - **Logical Operators**  
   - **Assignment Operators**  
   - **Bitwise Operators**  
   - **Membership Operators**  
   - **Identity Operators**  
---
### Lotus Language Quick Guide
7. **Comments**  
8. **Variable Declaration**  
9. **Operators**  
10. **Type Casting**  
11. **Variable Names**  
---
### Control Flow
12. **Conditional Statements**  
---
### Data Types and Structures
13. **Array**  
14. **Null Safety**  
---
### Error Handling and Functions
15. **Error Handling**  
16. **Functions**  
---
### Object-Oriented Programming in Lotus
17. **Defining Interface**  
18. **Classes**  
19. **Inheritance**


# What is lotus?  
*lotus* is a statically typed, compiled programming language designed by Bittu. It combines the simplicity of Python with the performance of C/C++ and is set to be released in the future.  


# Key Applications  
*lotus* is versatile and can be used for  
- **Web Development** Build robust server-side applications.  
- **Software Development** Create efficient, scalable software.  
- **Mathematics and Big Data** Perform complex computations and handle large datasets.  
- **System Scripting** Automate tasks and manage system operations.  
- **Machine Learning and AI** Develop ML models and AI-driven applications.  
- **Embedded Systems** Write performant code for hardware devices.  

# What can *lotus* do?  
*lotus* is designed to handle a wide range of programming tasks  
- **Web Applications** Develop web servers and backend systems.  
- **Workflow Integration** Build tools and scripts that integrate seamlessly with other software.  
- **Database Connectivity** Read from and write to databases efficiently.  
- **File Manipulation** Perform file-based operations for various workflows.  
- **Big Data and Complex Math** Process and analyze massive datasets.  
- **Prototyping and Production** Quickly prototype ideas and deploy production-ready applications.  

# Why Choose lotus?  
*lotus* stands out with these features  
- **Cross-Platform Support** Works seamlessly across Windows, Mac, Linux, Raspberry Pi, and more.
- **Simple Syntax** Offers a clean, intuitive syntax inspired by Python, making it easy to learn and use.
- **Code Efficiency** Allows developers to write concise, readable code, reducing boilerplate.
- **Object Oriented** Supports object oriented programming (OOP) style.
- **Performance** Delivers near-C/C++ performance, suitable for resource-intensive tasks.
- **Static Typing** Enables safer code with fewer runtime errors, thanks to strong type-checking, and null safety.


# Keywords
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


# **Operators in *lotus***
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

---

# Lotus Language Quick Guide
#### **Comments**
In Lotus, comments are used to add notes or explanations to your code. There are two types of comments:  
1. **Single-line comments**: Use `//` to comment out a single line.  
```lotus
// This is a single-line comment
let x i32 = 5 // This variable stores the value 5
```
2. **Multi-line comments**: Use `/*` and `*/` to comment out multiple lines.  
```lotus
"""
   This is a multi-line comment.
   It spans multiple lines and is useful for larger explanations.
"""
```

---

#### **Variable Declaration**
Lotus provides a flexible and intuitive syntax for declaring variables. It supports both type inference and explicit type annotations.  
1. **Declaring variables with type inference**:  
```lotus
let age = 25 // Lotus infers the type as int
```
2. **Declaring variables with explicit types**:  
```lotus
let name str = "Lotus" // Explicitly declares a string variable
```
3. **Declaring variables using walrus operator**:  
```lotus
name := "Lotus"
```
1. **Declaring nullable variables**:  
Use `?` after the type to indicate a variable can be null.  
```lotus
let username str? = null // Nullable string
```

---

#### **Operators**
Lotus supports a wide range of operators for various operations:  

1. **Arithmetic Operators**:  
`+`, `-`, `*`, `/`, `%`  
```lotus
let sum = 5 + 3
let product = 4 * 2
```

2. **Comparison Operators**:  
`==`, `!=`, `<`, `>`, `<=`, `>=`  
```lotus
if x == y {
    print("x is equal to y")
}
```

3. **Logical Operators**:  
`&&`, `||`, `!`  
```lotus
if isAdmin && isLoggedIn {
    print("Access granted")
}
```

4. **Assignment Operators**:  
`=`, `+=`, `-=`, `*=`, `/=`, `%=`  
```lotus
let score = 10
score += 5 // Equivalent to score = score + 5
```

5. **Null-coalescing Operator**:  
Use `??` to provide a default value for nullable variables.  
```lotus
let displayName = username ?? "Guest"
```

---

#### **Type Casting**
In Lotus, type casting is used to convert a value from one type to another.  
Lotus supports **explicit type casting** to ensure safe and intentional type conversions.

1. **Casting between numeric types**:
```lotus
   let x i32 = 10
   let y = f32(x) // Casts integer to f32
```

2. **String conversions**:  
Convert numbers or other types to strings using `str()`.  
```lotus
   let num = 42
   let str = str(num) // Converts 42 to "42"
```

3. **Invalid casts throw errors**:  
Lotus ensures type safety and will throw runtime errors for invalid casts.  
```lotus
   let value i32 = i32("text") // error: Invalid cast
```

---

#### **Variable Names**
Lotus follows a set of rules and best practices for naming variables.

1. **Valid naming rules**:  
   - Variable names can contain letters, digits, and underscores (`_`).  
   - Must start with a letter or an underscore.  
   - Cannot start with a digit.  
```lotus
   let username = "Alice" // Valid
   let _count = 10 // Valid
   let 1stVar = 5 // Invalid: Cannot start with a digit
```

2. **Case sensitivity**:  
   Variable names are case-sensitive.  
```lotus
   let Name = "Lotus"
   let name = "Language"
   print(Name) // Prints "Lotus"
   print(name) // Prints "Language"
```

3. **Reserved keywords**:  
   Variable names cannot use reserved keywords (e.g., `let`, `fn`, `if`, etc.).  
```lotus
   let fn = "function" // Error: 'fn' is a reserved keyword
```

4. **Best practices**:  
   - Use descriptive names for clarity.  
   - Follow camelCase or snake_case conventions for consistency.  
```lotus
   let userName = "Alice" // camelCase (preferred for variables)
   let user_name = "Bob"  // snake_case (also acceptable)
```

---

#### **Conditional Statements**
Control the flow of execution based on conditions.

**`if`, `elif`, `else`**  
Lotus supports standard conditional branching.

```lotus
if condition {
    // Execute if the condition is true
} elif anotherCondition {
    // Execute if the first condition is false and this is true
} else {
    // Execute if all previous conditions are false
}
```

Example:  
```lotus
let age = 20
if age < 18 {
    print("Minor")
} elif age < 65 {
    print("Adult")
} else {
    print("Senior")
}
```

---

#### **2. Pattern Matching with `when`**
Lotus provides a concise way to match patterns using `when`.

```lotus
when value {
    1 -> print("One")
    2 -> print("Two")
    _ -> print("Other") // _ acts as a wildcard
}
```

Example:  
```lotus
let status = 200
when status {
    200 -> print("OK")
    404 -> print("Not Found")
    _ -> print("Unknown status")
}
```

---

#### **3. Loops**
Loops in Lotus allow iteration over collections, ranges, or based on conditions.

**`for` Loop**  
The `for` loop is used for iteration.  
```lotus
for i in range(0, 5) {
    print(i) // Outputs: 0, 1, 2, 3, 4
}
```

**Iterating over collections**:  
```lotus
let items = [1, 2, 3]
for item in items {
    print(item)
}
```

**Infinite Loop with `for`**:  
```lotus
for {
    print("Looping forever")
}
```

---

#### **4. Loop Control: `continue` and `break`**
- **`continue`**: Skips the current iteration and moves to the next.  
- **`break`**: Exits the loop.

Example:  
```lotus
for i in range(1, 10) {
    if i % 2 == 0 {
        continue // Skip even numbers
    }
    if i > 7 {
        break // Exit loop if i > 7
    }
    print(i) // Outputs: 1, 3, 5, 7
}
```

---

#### **5. Range (`range(..)`)**
The `range` function generates a sequence of numbers.

**Syntax**:  
```lotus
range(start, end) // From start to end (exclusive)
range(start, end, step) // With a custom step value
```

Example:  
```lotus
for i in range(0, 10, 2) {
    print(i) // Outputs: 0, 2, 4, 6, 8
}
```

---

#### **6. `switch` Statement**
The `switch` statement is used to evaluate a variable against multiple cases.

**Syntax**:  
```lotus
switch variable {
    value1 -> {
        // Code for value1
    }
    value2 -> {
        // Code for value2
    }
    default -> {
        // Code if no cases match
    }
}
```

Example:  
```lotus
let day = 3
switch day {
    1 -> print("Monday")
    2 -> print("Tuesday")
    3 -> print("Wednesday")
    default -> print("Invalid day")
}
```

---

#### **7. Fallthrough in `switch`**
Lotus allows cases to "fall through" into the next case explicitly using the `fallthrough` keyword.

Example:  
```lotus
let grade = "B"
switch grade {
    "A" -> print("Excellent")
    "B" -> {
        print("Good")
        fallthrough
    }
    "C" -> print("Average")
    default -> print("Poor")
}
// Outputs:
// Good
// Average
```

---

#### **Array**
Arrays in Lotus are dynamic by default but can be restricted using generics for type safety.  
- **Dynamic Arrays**: Can store values of any type and grow as needed.  
- **Restricted Arrays**: Use generics to enforce type constraints.  

**Syntax**:  
```lotus
let dynamicArray = [1, "two", true] // Dynamic array
let intArray = array<i32>(1, 2, 3)     // Restricted to integers
```

**Accessing Elements**:  
```lotus
let nums = [10, 20, 30]
print(nums[0]) // Outputs: 10
```

**Modifying Arrays**:  
```lotus
var arr = ["apple", "banana"]
arr.append("cherry") // Adds an element
arr.remove(0)        // Removes the first element
```

---

#### **2. Boolean**
The `bool` type represents `true` or `false`.  
Certain values evaluate to `false`:  
- `0`, `None`, `""` (empty string), `[]` (empty array), `()` (empty tuple), `{}` (empty dictionary).  

**Examples**:  
```lotus
let isActive bool = true
if isActive {
    print("It's active!")
}

print(bool([])) // Outputs: false
print(bool(42)) // Outputs: true
```

---

#### **3. Constants**
Constants are immutable and are typically declared at the global scope for clarity.  

**Syntax**:  
```lotus
const PI = 3.14
const MAX_USERS i32 = 100
```

Constants cannot be reassigned:  
```lotus
PI = 3.1415 // Error: Cannot modify a constant
```

---

#### **4. Dictionary (`dict`)**
Dictionaries in Lotus store key-value pairs, allowing fast lookup.  
Keys must be unique, and values can be of any type.

**Syntax**:  
```lotus
let user dict = {
    "name": "Alice",
    "age": 30
}
```

**Accessing Values**:  
```lotus
print(user["name"]) // Outputs: Alice
```

**Adding/Updating Entries**:  
```lotus
user["email"] = "alice@example.com"
```

**Removing Entries**:  
```lotus
user.remove("age")
```

---

#### **5. Integer (`i32`)**
The `i32` type represents whole numbers. It supports all standard arithmetic operations.  

**Examples**:  
```lotus
let a = 10
let b i32 = 20
result := a + b
```

---

#### **6. Set**
Sets in Lotus store unique, unordered elements.  

**Syntax**:  
```lotus
let fruits = {"apple", "banana", "cherry"}
```

**Adding/Removing Elements**:  
```lotus
fruits.add("orange")
fruits.remove("banana")
```

**Operations**:  
```lotus
let setA = {1, 2, 3}
let setB = {3, 4, 5}
print(setA.union(setB))       // Outputs: {1, 2, 3, 4, 5}
print(setA.intersection(setB)) // Outputs: {3}
```

---

#### **7. String (`str`)**
The `str` type represents a sequence of characters.  

**Creating Strings**:  
```lotus
let greeting str = "Hello, Lotus!"
```

**String Interpolation**:  
```lotus
let name = "Alice"
print(f"Hello, {name}!") // Outputs: Hello, Alice!
```

**String Methods**:  
```lotus
text := "lotus"
print(text.upper()) // Outputs: LOTUS
```

---

#### **8. Tuple**
Tuples are immutable, ordered collections of values, often used to return multiple values from a function.

**Syntax**:  
```lotus
let coordinates = (10, 20)
```

**Accessing Values**:  
```lotus
print(coordinates[0]) // Outputs: 10
```

**Returning Multiple Values**:  
```lotus
fn getInfo()tuple {
    return "Alice", 30
}
let (name, age) = getInfo()
```

---

#### **9. Byte**
The `byte` type is used to represent raw binary data.

**Creating a Byte Array**:  
```lotus
let data byte = b"Lotus"
```

**Accessing Byte Data**:  
```lotus
print(data[0]) // Outputs: ASCII value of 'L'
```

---

#### **10. Range**
The `range` type generates sequences of numbers, often used in loops.

**Syntax**:  
```lotus
let r = range(1, 10) // Generates numbers from 1 to 9
```

**Using in Loops**:  
```lotus
for i in r {
    print(i) // Outputs: 0, 1, 2, 3, 4
}
```

---

#### **Nullable Types (`?`)**
A variable can be declared as nullable by appending `?` to its type.

**Syntax**:  
```lotus
let name str? = null // `name` can hold a string or `null`
```

**Example**:  
```lotus
let age int? = 25
age = null // Valid because `age` is nullable
```

---

#### **2. Safe Access (`?.`)**
The safe access operator is used to call properties or methods on nullable objects. If the object is `null`, the expression evaluates to `null` without throwing an error.

**Syntax**:  
```lotus
let length int? = name?.length
```

**Example**:  
```lotus
let name str? = "Alice"
print(name?.length) // Outputs: 5

let nullName str? = null
print(nullName?.length) // Outputs: null
```

---

#### **3. Non-Null Assertion (`!!`)**
The non-null assertion operator forces access to a nullable variable and throws a runtime error if the variable is `null`.

**Syntax**:  
```lotus
let length i32 = name!!.length
```

**Example**:  
```lotus
let name str? = "Alice"
print(name!!.length) // Outputs: 5

let nullName str? = null
print(nullName!!.length) // Throws a runtime error
```

---

#### **4. Elvis Operator (`??`)**
The Elvis operator provides a default value when a nullable expression evaluates to `null`.

**Example**:  
```lotus
let name str? = null
let displayName = name ?? "Anonymous"
print(displayName) // Outputs: Anonymous

let anotherName str? = "Lotus"
let anotherDisplayName = anotherName ?? "Anonymous"
print(anotherDisplayName) // Outputs: Lotus
```

---

#### **5. Combining Null Safety Features**
Null safety features can be combined to create concise and safe code.

**Example**:  
```lotus
let name str? = null

// Safe access with a fallback value
let length = name?.length ?? 0
print(length) // Outputs: 0

// Non-null assertion for a known non-null value
let knownName str? = "Lotus"
print(knownName!!.length) // Outputs: 5
```

---

#### **6. Null Checking**
You can check for `null` explicitly using an `if` statement to ensure safe usage of nullable variables.

**Example**:  
```lotus
let name str? = null

if name != null {
    print(name!!.length) // Safe to use as `name` is not null
} else {
    print("Name is null")
}
```

---

#### **7. Declaring Nullable and Non-Nullable Variables**
- **Nullable Variable**: `let variable type? = value`
- **Non-Nullable Variable**: `let variable type = value`

**Example**:  
```lotus
let nullableName str? = null
let nonNullableName str = "Lotus" // Cannot hold null
```

### **Summary of Null Safety Operators**
| Operator | Description                                                                 |
|----------|-----------------------------------------------------------------------------|
| `?`      | Declares a nullable type.                                                  |
| `?.`     | Safe access operator to call properties/methods if the object is not null. |
| `!!`     | Non-null assertion operator; throws an error if the value is null.         |
| `??`     | Elvis operator to provide a default value when the object is null.         |

---

#### **Error Basics**
Errors in Lotus are values of the `Error` type. They can be created, returned, and handled like any other value.  

**Declaring a Function that Returns an Error**:  
```lotus
fn divide(a int, b int) (int, error) {
    if b == 0 {
        return (0, error.New("Division by zero"))
    }
    return (a / b, null)
}
```

**Handling Errors**:  
```lotus
let (result, err) = divide(10, 0)
if err != null {
    print(err.message) // Outputs: Division by zero
} else {
    print(result)
}
```

---

#### **2. Creating New Errors**
Errors can be created using the `Error.New` method.

**Example**:  
```lotus
let err = error.New("Something went wrong")
print(err.message) // Outputs: Something went wrong
```

---

#### **3. Custom Errors (Extending the `error` Class)**
For more detailed or domain-specific errors, you can create custom error types by extending the `error` class.

**Defining a Custom Error**:  
```lotus
class ValidationError extends error {
    ...
}
```

**Using a Custom Error**:  
```lotus
fn validateAge(age int) error? {
    if age < 18 {
        return ValidationError.new("age", "Age must be at least 18")
    }
    return null
}

let err = validateAge(16)
if err != null {
    if err is ValidationError {
        print(err.details()) // Outputs: Validation failed on field 'age': Age must be at least 18
    } else {
        print(err.message)
    }
}
```

---

#### **4. Error Propagation**
You can propagate errors using explicit returns, ensuring they are handled at the appropriate level.

**Example**:  
```lotus
fn readFile(fileName str)(str, Error) {
    if fileName == "" {
        return ("", Error.New("File name cannot be empty"))
    }
    return ("File content", null)
}

fn processFile(fileName str) Error? {
    let (content, err) = readFile(fileName)
    if err != null {
        return err // Propagate the error
    }
    print(content)
    return null
}

let err = processFile("")
if err != null {
    print(err.message) // Outputs: File name cannot be empty
}
```

---

#### **5. Error Unwrapping**
Errors in Lotus can be wrapped to provide additional context. You can unwrap them to retrieve the original error.

**Example**:  
```lotus
let baseError = error.New("Base error")
let wrappedError = error.Wrap(baseError, "Additional context")

print(wrappedError.message) // Outputs: Additional context: Base error
print(wrappedError.message) // Outputs: Base error
```

---

#### **6. Panic and Recovery**
For critical errors that should terminate execution, you can use `panic`. However, `panic` is discouraged in favor of proper error handling.

**Example**:  
```lotus
fn riskyOperation() {
    panic("Critical failure!") // Terminates the program
}

fn main() {
    riskyOperation() // Program will terminate
}
```

To handle a `panic`, use `recover` in a controlled block (e.g., to clean up resources).  

---


#### **Function Basics**
Functions in Lotus are defined using the `fn` keyword.

**Syntax**:  
```lotus
fn functionName(param1 type, param2 type) returnType {
    // Function body
    return value
}
```

**Example**:  
```lotus
fn add(a int, b int) i32 {
    return a + b
}
print(add(5, 3)) // Outputs: 8
```

---

#### **Parameters with Default Values**
Functions can have parameters with default values, making them optional during the function call.

**Syntax**:  
```lotus
fn greet(name str = "Guest") str {
    return f"Hello, {name}!"
}
```

**Example**:  
```lotus
print(greet())           // Outputs: Hello, Guest!
print(greet("Alice"))    // Outputs: Hello, Alice!
```

---

#### **Generics**
Generics allow functions to operate on different types without specifying them explicitly.

**Syntax**:  
```lotus
fn identity<T>(value T) T {
    return value
}
```

**Example**:  
```lotus
print(identity<i32>(42))        // Outputs: 42
print(identity(34))             // Outputs: 34

print(identity<str>("Lotus"))   // Outputs: Lotus
print(identity("Hello"))        // Outputs: Hello
```

---

#### **Variadic Arguments**
Variadic arguments enable a function to accept an arbitrary number of arguments of a specific type.

**Syntax**:  
```lotus
fn sumAll(numbers ...i32) i32 {
    let total = 0
    for num in numbers {
        total += num
    }
    return total
}
```

**Example**:  
```lotus
print(sumAll(1, 2, 3, 4, 5)) // Outputs: 15
```

---

#### **5. Keyword Arguments**
Functions can be called using keyword arguments to improve readability and flexibility.

**Example**:  
```lotus
fn createUser(name str, age int, role str = "User") str {
    return f"Name: {name}, Age: {age}, Role: {role}"
}

print(createUser(name="Alice", age=25))            // Outputs: Name: Alice, Age: 25, Role: User
print(createUser(name="Bob", age=30, role="Admin")) // Outputs: Name: Bob, Age: 30, Role: Admin
```

---

#### **Higher-Order Functions**
Higher-order functions are functions that take other functions as arguments or return functions.

**Example**:  
```lotus
fn apply(op fn, a i32, b i32) i32 {
    return op(a, b)
}

fn multiply(x i32, y i32) i32 {
    return x * y
}

print(apply(multiply, 5, 3)) // Outputs: 15
```

---

#### **7. Keyword Arguments and Variadic Arguments Together**
Keyword and variadic arguments can be used in the same function.

**Example**:  
```lotus
fn logMessage(level str = "INFO", messages ...str) {
    for message in messages {
        print(f"[{level}] {message}")
    }
}

logMessage(messages: "Starting process", "Process completed")
// Outputs:
// [INFO] Starting process
// [INFO] Process completed
```

---

#### **Decorators**
Decorators in Lotus allow you to modify or enhance the behavior of functions by wrapping them.

**Syntax**:  
```lotus
@decorator
fn functionName(params...) {
    // Function body
}
```

**Example**:  
```lotus
fn logExecution(func fn) fn {
    return fn() str {
        print("Function is being executed")
        return func()
    }
}

@logExecution
fn greet() str {
    return "Hello, Lotus!"
}

print(greet())
// Outputs:
// Function is being executed
// Hello, Lotus!
```

---

### **Defining Interfaces**
An interface is declared using the `interface` keyword. It contains method signatures that a type must implement to conform to the interface.

**Syntax**:  
```lotus
interface Name {
    fn methodName(param1 type, param2 type) returnType
}
```

**Example**:  
```lotus
interface Drawable {
    fn draw() void
}
```

---

### **Implementing Interfaces**
A type implements an interface by defining all the methods declared in the interface.

**Example**:  
```lotus
class Circle impl Drawable {
    let radius int

    fn new(radius i32) Circle {
        let obj = Circle()
        obj.radius = radius
        return obj
    }

    fn draw() {
        print("Drawing a circle with radius {self.radius}")
    }
}

class Square impl Drawable {
    let side i32

    fn new(side i32) Square {
        let obj = Square()
        obj.side = side
        return obj
    }

    fn draw() {
        print("Drawing a square with side {self.side}")
    }
}
```

---

### **Using Interfaces**
You can declare a variable of an interface type and assign any object that implements the interface to it.

**Example**:  
```lotus
fn render(drawable Drawable) {
    drawable.draw()
}

let c = Circle.new(5)
let s = Square.new(3)

render(c) // Outputs: Drawing a circle with radius 5
render(s) // Outputs: Drawing a square with side 3
```

---

### **Checking Interface Conformance**
Use the `is` operator to check if a type implements a specific interface.

**Example**:  
```lotus
if c is Drawable {
    print("c implements Drawable")
}
```

---

### **Combining Interfaces**
Lotus allows a type to implement multiple interfaces.

**Example**:  
```lotus
interface Movable {
    fn moveTo(x int, y int) void
}

class Shape impl Drawable, Movable {
    fn draw() {
        print("Drawing a shape")
    }

    fn moveTo(x i32, y i32) {
        print(f"Moving to ({x}, {y})")
    }
}

let shape = Shape()
shape.draw()           // Outputs: Drawing a shape
shape.moveTo(10, 20)   // Outputs: Moving to (10, 20)
```

---

### **6. Interface Composition**
Interfaces can be composed by embedding other interfaces.

**Example**:  
```lotus
interface Transformable {
    fn rotate(angle f32) void
    fn scale(factor f32) void
}

interface AdvancedDrawable extends Drawable, Transformable {}

class ComplexShape implements AdvancedDrawable {
    fn draw() {
        print("Drawing a complex shape")
    }

    fn rotate(angle f32) {
        print(f"Rotating by {angle} degrees")
    }

    fn scale(factor f32) {
        print(f"Scaling by a factor of {factor}")
    }
}
```

---

### **7. Generic Interfaces**
Interfaces can also be used with generics to define type constraints.

**Example**:  
```lotus
interface Comparable<T> {
    fn compareTo(other T) i32
}

class Number impl Comparable<Number> {
    let value i32

    fn new(value i32) Number {
        let obj = Number()
        obj.value = value
        return obj
    }

    fn compareTo(other Number) i32 {
        return self.value - other.value
    }
}

let n1 = Number.new(10)
let n2 = Number.new(20)

print(n1.compareTo(n2)) // Outputs: -10
```

---

### **Abstract Methods in Interfaces**
If a method is declared but not implemented in an interface, the implementing class must define it.

**Example**:  
```lotus
interface Vehicle {
    fn drive() void
}

class Car impl Vehicle {
    fn drive() void {
        print("Driving a car")
    }
}

let v = Car()
v.drive() // Outputs: Driving a car
```

---

### **Classes**
A class in Lotus is defined using the `class` keyword. Classes group related data (fields) and behavior (methods) together.

**Syntax**:  
```lotus
class ClassName {
    // Fields (Variables)
    // Methods
}
```

**Example**:  
```lotus
class Person {
    let name str
    let age i32

    fn new(name str, age i32) Person {
        let obj = Person()
        obj.name = name
        obj.age = age
        return obj
    }

    fn greet() {
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")
    }
}

let p = Person.new("Alice", 30)
p.greet() // Outputs: Hello, my name is Alice and I am 30 years old.
```

---

### **2. Access Modifiers**
Lotus supports access control for fields and methods using the `public` and `private` keywords.

- **Public**: Accessible from outside the class (default behavior).  
- **Private**: Accessible only within the class (priv keyword).
- **Protected**: Accessible only within the module (prot keyword).

**Example**:  
```lotus
class BankAccount {
    priv let (
        balance f32
        lean f64
    )
    prot let (
        ...
    )

    fn new(initialBalance f32) BankAccount {
        let obj = BankAccount()
        obj.balance = initialBalance
        return obj
    }

    fn deposit(amount f32) void {
        self.balance += amount
    }

    fn getBalance() f32 {
        return self.balance
    }
}

let account = BankAccount.new(100.0)
account.deposit(50.0)
print(account.getBalance()) // Outputs: 150.0
```

---

### **3. Method Declaration**
Methods are functions defined within a class. They can access the class's fields and other methods using the `this` keyword.

**Example**:  
```lotus
class Calculator {
    fn add(a i32, b i32) i32 {
        return a + b
    }

    fn multiply(a i32, b i32) i32 {
        return a * b
    }
}

let calc = Calculator()
print(calc.add(5, 3))       // Outputs: 8
print(calc.multiply(4, 6))  // Outputs: 24
```

---

### **4. Inheritance**
A class can inherit from another class to reuse its fields and methods.


**Example**:  
```lotus
class Animal {
    fn speak() {
        print("Some generic animal sound")
    }
}

class Dog(Animal) {
    fn speak() {
        print("Woof Woof!")
    }
}

let d = Dog()
d.speak() // Outputs: Woof Woof!
```

### **Note on Inheritance in Lotus**

In Lotus, a class can only extend **one** other class at a time. This is because Lotus follows a single inheritance model, ensuring simplicity and avoiding the complexities of multiple inheritance (such as the diamond problem).

If you need functionality from multiple sources, consider using **interfaces**. A class in Lotus can implement multiple interfaces, allowing you to achieve a similar effect as multiple inheritance without its drawbacks.

---

**Example**:  
```lotus
class A {
    fn methodA() void {
        print("Method A")
    }
}

class B(A) {
    fn methodB() void {
        print("Method B")
    }
}

// Not Allowed
class C(A, B) {} // Error: A class can only extend one class
```

To combine functionality:  
```lotus
interface X {
    fn methodX() void
}

interface Y {
    fn methodY() void
}

class Z impl X, Y {
    fn methodX() {
        print("Method X")
    }

    fn methodY() {
        print("Method Y")
    }
}
```

---

### **Method Overriding**
A subclass can override a method from its parent class. Use `super.methodName()` to call the parent class's implementation.

**Example**:  
```lotus
class Vehicle {
    fn describe() {
        print("This is a vehicle.")
    }
}

class Car(Vehicle) {
    fn describe() {
        super.describe()
        print("Specifically, this is a car.")
    }
}

let c = Car()
c.describe()
// Outputs:
// This is a vehicle.
// Specifically, this is a car.
```

---

### **6. Interfaces and Implementation**
Lotus allows a class to implement one or more interfaces. This is done using the `impl` keyword.

**Example**:  
```lotus
interface Shape {
    fn area() f32
}

class Circle impl Shape {
    let radius f32

    fn new(radius f32) Circle {
        let obj = Circle()
        obj.radius = radius
        return obj
    }

    fn area() f32 {
        return 3.14 * self.radius * self.radius
    }
}

let circle = Circle.new(5.0)
print(circle.area()) // Outputs: 78.5
```

---

### **7. Constructor**
The `__init__` method in a class serves as its constructor. It initializes the class's fields and returns an instance of the class.

**Example**:  
```lotus
class Rectangle {
    let width f32
    let height f32

    fn __init__(width f32, height f32) Rectangle {
        let obj = Rectangle()
        obj.width = width
        obj.height = height
        return obj
    }

    fn area() f32 {
        return self.width * self.height
    }
}

let rect = Rectangle.new(4.0, 5.0)
print(rect.area()) // Outputs: 20.0
```

---

### **Abstract Classes**
An abstract class cannot be instantiated directly and is intended to be extended by other classes. It can define methods that must be implemented by subclasses.

**Example**:  
```lotus
abs class Animal {
    fn makeSound() void
}

class Cat(Animal) {
    fn makeSound() void {
        print("Meow")
    }
}

let cat = Cat()
cat.makeSound() // Outputs: Meow
```

---
