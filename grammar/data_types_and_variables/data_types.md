### Built-in Data Types in b2  

*b2* provides a variety of built-in data types, categorized as follows:

---

### Data Type Categories  

1. **Text Type**  
   - `str`  

2. **Numeric Types**  
   - Signed Integers `i8`, `i16`, `i32`, `i64`, `i128`  
   - Unsigned Integers `u8`, `u16`, `u32`, `u64`, `u128`  
   - Floating-Point Numbers `f32`, `f64`  
   - Complex Numbers `complex` (to be implemented)  

3. **Sequence Types**  
   - `list`  
   - `array`  
   - `tuple`  
   - `range`  

4. **Mapping Type**  
   - `dict`  
   - `map`  

5. **Set Type**  
   - `set`  

6. **Boolean Type**  
   - `bool`  

7. **Binary Types**  
   - `bytes`  

8. **None Type**  
   - `null`  

---

### Getting the Data Type  

To check a variable's type, use the `type()` function  
```b2
x := 5
print(type(x))  // Outputs i64
```

---

### Setting the Data Type  

By default, *b2* infers the data type during assignment  

```b2
x := "Hello World"   // str
x := 20              // i64
x := 20.5            // f32
x := ["apple", "banana", "cherry"]  // list
x := array<str, 3>("apple", "banana", "cherry")  // array of str type, 3 elements
x := ("apple", "banana", "cherry")  // tuple
x := range(6)       // range
x := map<str, str>(name="John", age="36")  // map
x := {"apple", "banana", "cherry"}  // set
x := True           // bool
x := b"Hello"       // bytes
x := null           // NoneType
```

---

### Setting a Specific Data Type  

Use type constructors or explicit type declarations for precision  

```b2
x := str("Hello World")   // Explicitly set as str
y := i64(1234)            // Explicitly set as i64
z := f32(3.14)            // Explicitly set as f32
a := bool(True)           // Explicitly set as bool
b := array<i32, 4>(1, 2, 3, 4)  // Explicitly declare an array of i32 with 4 elements
c := map<str, str>(name="bittu", age="36")  // Explicitly declare a map with str keys and values
```

---

### Notes  

- **Complex Numbers** Implementation pending; will handle real and imaginary parts.  
- **Array Type** Requires type and size to be specified, followed by the elements.  
- **Map Type** Enables key-value pairs with specified key and value types, similar to dictionaries in Python.  
- Strong typing in *b2* ensures consistency and improves code readability.