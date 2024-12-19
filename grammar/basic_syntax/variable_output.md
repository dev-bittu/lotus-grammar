### Outputting Variables in lotus  

The `print()` function in *lotus* is used to display the values of variables. It supports various ways of combining and displaying data.

---

### Basic Output  

You can print a variable directly using `print()`  
```lotus
x := "lotus is awesome"
print(x)  // Outputs lotus is awesome
```

---

### Printing Multiple Variables  

The `print()` function allows outputting multiple variables separated by commas. This is convenient for handling different data types  
```lotus
x := "lotus"
y := "is"
z := "awesome"
print(x, y, z)  // Outputs lotus is awesome
```

---

### Using the `+` Operator  

You can use the `+` operator to concatenate strings  
```lotus
x := "lotus "
y := "is "
z := "awesome"
print(x + y + z)  // Outputs lotus is awesome
```

**Note:** Ensure that strings contain necessary spaces to avoid undesired results like `lotusisawesome`.  

---

### Mathematical Operations with Numbers  

The `+` operator also performs addition when used with numbers  
```lotus
x := 5
y := 10
print(x + y)  // Outputs 15
```

---

### Combining Strings and Numbers  

When combining a string and a number with `+`, *lotus* will throw an error  
```lotus
x := 5
y := "John"
print(x + y)  // Error Cannot concatenate string and number
```

The correct approach is to separate variables with commas  
```lotus
x := 5
y := "John"
print(x, y)  // Outputs 5 John
```

---

TODO: Show print func defination
TODO: print vs println