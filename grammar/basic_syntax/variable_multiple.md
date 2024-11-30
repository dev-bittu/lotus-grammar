### Assigning Values to Variables in b2  

*b2* offers flexible ways to assign values to variables, including multiple assignments and unpacking.  

---

### Assigning Multiple Values to Multiple Variables  

You can assign values to multiple variables in a single line  
```b2
x, y, z := "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

**Note:** Ensure the number of variables matches the number of values. Otherwise, *b2* will raise an error.  

---

### Assigning One Value to Multiple Variables  

*b2* does **not** allow assigning the same value to multiple variables in a single line  
```b2
// This is invalid in b2:
x = y = z = "Orange"  // Error Multiple assignments with a single value are not supported
```

---

### Unpacking a Collection  

*b2* allows unpacking collections such as lists, tuples, etc., into individual variables.  

**Example – Unpacking a List:**  
```b2
fruits := ["apple", "banana", "cherry"]
x, y, z := fruits
print(x)  // Outputs apple
print(y)  // Outputs banana
print(z)  // Outputs cherry
```

By unpacking, each variable is assigned a corresponding value from the collection.  

--- 

These features make *b2* efficient for handling multiple values in a clear and concise way.