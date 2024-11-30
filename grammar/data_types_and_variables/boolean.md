### **Booleans in *b2***

Booleans represent one of two values: **true** or **false**. They are used to evaluate conditions and make decisions based on logical expressions.

---

### **Boolean Values**

In *b2*, a boolean is typically used to evaluate if an expression is true or false. You can evaluate any expression to get one of two possible outcomes: **true** or **false**.

#### **Comparison Expressions**

When you compare two values, *b2* evaluates the expression and returns a boolean answer:

```b2
print(10 > 9)   // true
print(10 == 9)  // false
print(10 < 9)   // false
```

#### **Conditional Expressions in if-else**

When used in `if` statements, *b2* returns `true` or `false`, which helps decide which block of code to execute.

Example:

```b2
a := 200
b := 33

if b > a {
    print("b is greater than a")
} else {
    print("b is not greater than a")
}
```

---

### **Evaluate Values and Variables**

You can evaluate any value using the `bool()` function in *b2* to get `true` or `false`.

#### **Evaluating Values**

```b2
print(bool("Hello"))  // true
print(bool(15))       // true
```

#### **Evaluating Variables**

```b2
x := "Hello"
y := 15

print(bool(x))  // true
print(bool(y))  // true
```

---

### **Truthy and Falsy Values**

- **Truthy Values:** Most values evaluate to `true` in *b2*. A string, non-zero number, list, tuple, dictionary, or set will return `true` if it contains content.

Example:

```b2
print(bool("abc"))                // true
print(bool(123))                  // true
print(bool(["apple", "cherry"]))  // true
```

- **Falsy Values:** There are a few values that evaluate to `false`. These include empty containers like `()`, `[]`, `{}`, empty strings `""`, the number `0`, and `None`.

Example:

```b2
print(bool(false))  // false
print(bool(None))   // false
print(bool(0))      // false
print(bool(""))     // false
print(bool(()))     // false
print(bool([]))     // false
print(bool({}))     // false
```

If an object has a `__len__` function returning `0` or `false`, it will also evaluate to `false`.

Example:

```b2
class MyClass {
    def __len__(self) {
        return 0
    }
}

myObj := MyClass()
print(bool(myObj))  // false
```

---

### **Functions that Return Booleans**

You can create functions that return boolean values based on conditions.

Example:

```b2
def myFunction() {
    return true
}

print(myFunction())  // true
```

You can execute code based on the boolean return value:

```b2
def myFunction() {
    return true
}

if myFunction() {
    print("YES!")
} else {
    print("NO!")
}
```

### **Built-in Functions Returning Booleans**

*b2* provides various built-in functions that return boolean values. One such function is `isinstance()`, which checks if an object is of a particular data type.

Example:

```b2
x := 200
print(isinstance(x, i64))  // true
```

---

By using boolean expressions, you can control the flow of your program and evaluate conditions to make decisions, handle different data types, and work with various logical expressions.
