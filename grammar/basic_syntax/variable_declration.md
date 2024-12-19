### Variables and Data Types in lotus  
*lotus* allows for flexible and type-safe variable declarations. It supports both explicit and implicit typing, along with various ways to declare and initialize variables.  

---

### Declaring Variables  

1. **Explicit Declaration**  
Specify the variable type during declaration  
```lotus
let myint64 i64 = 57878
```

2. **Implicit Declaration**  
The type is inferred based on the assigned value  
```lotus
let myint64 = 57878  // Defaults to i64
```

3. **Using `:=` for Declaration**  
Declare and initialize a variable in one step  
```lotus
myint64 i64 := 57878  // Explicit type
myint64 := 57878       // Defaults to i64
```

---

### Integer Types  
*lotus* supports both signed and unsigned integers  
- **Signed:** `i8`, `i16`, `i32`, `i64`, `i128`  
- **Unsigned:** `u8`, `u16`, `u32`, `u64`, `u128`  

---

### Updating Variables  
You can update a variable's value as long as the type remains the same  
```lotus
myint64 = 237846
```

**Invalid Example:**  
*lotus* does not allow changing a variable's type  
```lotus
myint64 = "this is string"  // Error Type mismatch
```

---

### Strings and Characters  
- Strings are enclosed in **double quotes** (`"`).  
- Characters are enclosed in **single quotes** (`'`).  

```lotus
mystr := "Hello World"
mychar := 'H'

print(mystr)
print(mychar)
```

---

### Casting  
You can cast variables to a specific type  
```lotus
x = str(3)    // Converts 3 to "3"
y = i64(3)    // Converts 3 to an integer
z = f32(3)  // Converts 3 to 3.0
```

---

### Getting the Type  
Use the `type()` function to check a variable's type  
```lotus
x := 5
y := "John"
print(type(x))  // Outputs: i64
print(type(y))  // Outputs: str
```

---

### Case Sensitivity  
Variable names in *lotus* are case-sensitive  
```lotus
a = 4
A = "Sally"
// `A` will not overwrite `a`
```

---

This demonstrates how *lotus* balances simplicity with type safety, providing developers with both flexibility and control.