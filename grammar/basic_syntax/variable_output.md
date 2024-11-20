### Outputting Variables in mylang  

The `print()` function in *mylang* is used to display the values of variables. It supports various ways of combining and displaying data.

---

### Basic Output  

You can print a variable directly using `print()`  
```mylang
x := "mylang is awesome"
print(x)  // Outputs mylang is awesome
```

---

### Printing Multiple Variables  

The `print()` function allows outputting multiple variables separated by commas. This is convenient for handling different data types  
```mylang
x := "mylang"
y := "is"
z := "awesome"
print(x, y, z)  // Outputs mylang is awesome
```

---

### Using the `+` Operator  

You can use the `+` operator to concatenate strings  
```mylang
x := "mylang "
y := "is "
z := "awesome"
print(x + y + z)  // Outputs mylang is awesome
```

**Note:** Ensure that strings contain necessary spaces to avoid undesired results like `mylangisawesome`.  

---

### Mathematical Operations with Numbers  

The `+` operator also performs addition when used with numbers  
```mylang
x := 5
y := 10
print(x + y)  // Outputs 15
```

---

### Combining Strings and Numbers  

When combining a string and a number with `+`, *mylang* will throw an error  
```mylang
x := 5
y := "John"
print(x + y)  // Error Cannot concatenate string and number
```

The correct approach is to separate variables with commas  
```mylang
x := 5
y := "John"
print(x, y)  // Outputs 5 John
```

---

### Summary  

- Use commas to combine variables of different types in the `print()` function.  
- Use the `+` operator for string concatenation or numerical addition.  
- Avoid combining strings and numbers with `+` to prevent errors.  

These methods allow versatile and error-free output handling in *mylang*.