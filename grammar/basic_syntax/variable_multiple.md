### Assigning Values to Variables in mylang  

*mylang* offers flexible ways to assign values to variables, including multiple assignments and unpacking.  

---

### Assigning Multiple Values to Multiple Variables  

You can assign values to multiple variables in a single line  
```mylang
x, y, z := "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

**Note:** Ensure the number of variables matches the number of values. Otherwise, *mylang* will raise an error.  

---

### Assigning One Value to Multiple Variables  

*mylang* does **not** allow assigning the same value to multiple variables in a single line  
```mylang
// This is invalid in mylang:
x = y = z = "Orange"  // Error Multiple assignments with a single value are not supported
```

---

### Unpacking a Collection  

*mylang* allows unpacking collections such as lists, tuples, etc., into individual variables.  

**Example – Unpacking a List:**  
```mylang
fruits := ["apple", "banana", "cherry"]
x, y, z := fruits
print(x)  // Outputs apple
print(y)  // Outputs banana
print(z)  // Outputs cherry
```

By unpacking, each variable is assigned a corresponding value from the collection.  

--- 

These features make *mylang* efficient for handling multiple values in a clear and concise way.