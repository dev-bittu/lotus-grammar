### Functions in MyLang: Comprehensive Documentation (Updated)

Functions in MyLang are reusable blocks of code that perform specific tasks. They are defined using the `def` keyword and support various features like default arguments, recursion, variadic arguments, higher-order functions, pointers, references, and more.

---

## **Basic Function Syntax**
Functions are defined using the `def` keyword followed by the function name, parameters (if any), and the function body enclosed in `{}`.

### Example:
```mylang
def greet() {
    print("Hello, World!")
}
greet()
```

---

## **Functions with Parameters**
Functions can accept parameters to make them dynamic. Parameter types are declared without `:` and are placed directly after the parameter name.

### Example:
```mylang
def greet(name str) {
    print("Hello, " + name + "!")
}
greet("Bittu")
```

**Output:**  
`Hello, Bittu!`

---

## **Functions with Default Parameter Values**
You can define default values for parameters. If no value is provided during the function call, the default is used.

### Example:
```mylang
def greet(name str = "User") {
    print("Hello, " + name + "!")
}
greet()          // Output: Hello, User!
greet("Bittu")   // Output: Hello, Bittu!
```

---

## **Functions with Multiple Parameters**
MyLang supports functions with multiple parameters.

### Example:
```mylang
def add(a i32, b i32) {
    print(a + b)
}
add(5, 3)  // Output: 8
```

---

## **Returning Values from Functions**
Use the `return` keyword to return a value. Specify the return type using parentheses `()` with the type.

### Example:
```mylang
def multiply(a i32, b i32) (i32) {
    return a * b
}
result := multiply(4, 5)
print(result)  // Output: 20
```

---

## **Variable Types in Function Declarations**
Variable types are declared directly after the parameter name. Return types are specified in parentheses after the function signature.

### Example:
```mylang
def divide(a f32, b f32) (f32) {
    return a / b
}
print(divide(10.0, 2.0))  // Output: 5.0
```

---

## **Functions with Variadic Arguments**
MyLang supports variadic arguments using `...`, allowing you to pass a variable number of arguments.

### Example:
```mylang
def sum(...numbers i32) (i32) {
    total := 0
    for n in numbers {
        total += n
    }
    return total
}
print(sum(1, 2, 3, 4))  // Output: 10
```

---

## **Functions with Keyword Arguments**
MyLang allows passing arguments as key-value pairs using dictionaries.

### Example:
```mylang
def displayInfo(info dict<str, any>) {
    for key, value in info {
        print(key + ": " + value)
    }
}
displayInfo({"name": "Bittu", "age": 25, "city": "Delhi"})
```

**Output:**  
```
name: Bittu  
age: 25  
city: Delhi  
```

---

## **Pointers in Functions**
Pointers allow passing the memory address of a variable to enable modification of the original value.

### Example:
```mylang
def increment(value *i32) {
    *value += 1
}
num := 10
increment(&num)
print(num)  // Output: 11
```

---

## **References in Functions**
References allow accessing and modifying the original variable without explicitly using pointers.

### Example:
```mylang
def double(value &i32) {
    value *= 2
}
num := 5
double(num)
print(num)  // Output: 10
```

---

## **Recursive Functions**
A recursive function calls itself. This is useful for solving problems that can be divided into smaller, similar sub-problems.

### Example: Factorial
```mylang
def factorial(n i32) (i32) {
    if n <= 1 {
        return 1
    }
    return n * factorial(n - 1)
}
print(factorial(5))  // Output: 120
```

---

## **Higher-Order Functions**
MyLang allows functions to accept other functions as arguments or return them. When using higher-order functions, the `def` keyword is sufficient without specifying parameter or return types.

### Example:
```mylang
def applyOperation(a i32, b i32, operation def) (i32) {
    return operation(a, b)
}

def add(x, y) {
    return x + y
}

print(applyOperation(5, 3, add))  // Output: 8
```

---

## **Default Arguments with Mixed Parameters**
You can mix positional arguments, default arguments, and variadic arguments.

### Example:
```mylang
def calculate(a i32, b i32 = 10, ...extra i32) (i32) {
    result := a + b
    for val in extra {
        result += val
    }
    return result
}
print(calculate(5))              // Output: 15
print(calculate(5, 3, 1, 2))     // Output: 11
```

---

## **Lambda (Anonymous) Functions**
Lambda functions are small, unnamed functions used for short tasks.

### Example:
```mylang
square := def(x i32) (i32) {
    return x * x
}
print(square(4))  // Output: 16
```

---

## **Function Overloading**
MyLang supports function overloading, allowing multiple functions with the same name but different parameter types.

### Example:
```mylang
def display(value i32) {
    print("Integer: " + value)
}

def display(value str) {
    print("String: " + value)
}

display(10)       // Output: Integer: 10
display("Hello")  // Output: String: Hello
```
