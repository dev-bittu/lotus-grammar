### Integer Data Types in *lotus*  

*lotus* provides a variety of integer data types for different use cases, with both **signed** and **unsigned** variants.  

---

### Signed Integer Types  

Signed integers can hold both positive and negative values.  

| Data Type | Description       | Minimum Value            | Maximum Value            |
|-----------|-------------------|--------------------------|--------------------------|
| `i8`      | 8-bit integer     | -128                     | 127                      |
| `i16`     | 16-bit integer    | -32,768                  | 32,767                   |
| `i32`     | 32-bit integer    | -2,147,483,648           | 2,147,483,647            |
| `i64`     | 64-bit integer    | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| `i128`    | 128-bit integer   | -170,141,183,460,469,231,731,687,303,715,884,105,728 | 170,141,183,460,469,231,731,687,303,715,884,105,727 |  

---

### Unsigned Integer Types  

Unsigned integers can hold only positive values, which allows them to have a larger range for positive numbers.  

| Data Type | Description       | Minimum Value | Maximum Value            |
|-----------|-------------------|---------------|--------------------------|
| `u8`      | 8-bit integer     | 0             | 255                      |
| `u16`     | 16-bit integer    | 0             | 65,535                   |
| `u32`     | 32-bit integer    | 0             | 4,294,967,295            |
| `u64`     | 64-bit integer    | 0             | 18,446,744,073,709,551,615 |
| `u128`    | 128-bit integer   | 0             | 340,282,366,920,938,463,463,374,607,431,768,211,455 |  

---

### Examples  

1. **Signed Integer Example**  
```lotus
x := i32(-12345)  // A signed 32-bit integer
print(x)          // Outputs -12345
```

2. **Unsigned Integer Example**  
```lotus
y := u16(54321)   // An unsigned 16-bit integer
print(y)          // Outputs 54321
```

3. **Default Integer Type**  
By default, *lotus* assigns the `i64` data type to integer literals if no type is specified  
```lotus
z := 123456       // Automatically inferred as i64
print(z)          // Outputs 123456
```

4. **Explicit Declaration**  
To ensure a specific data type, use the type constructor or type declaration syntax  
```lotus
a := i8(127)      // Explicitly declare as i8
print(a)          // Outputs 127
```

5. **Invalid Assignments**  
Attempting to assign a value outside the range of a type will cause a compilation error  
```lotus
b := i8(200)      // Error 200 exceeds the range of i8 (-128 to 127)
```

---

### Table Quick Reference for Integer Data Types  

| **Type** | **Bits** | **Signed** | **Minimum Value**                       | **Maximum Value**                       |
|----------|----------|------------|-----------------------------------------|-----------------------------------------|
| `i8`     | 8        | Yes        | -128                                    | 127                                     |
| `u8`     | 8        | No         | 0                                       | 255                                     |
| `i16`    | 16       | Yes        | -32,768                                 | 32,767                                  |
| `u16`    | 16       | No         | 0                                       | 65,535                                  |
| `i32`    | 32       | Yes        | -2,147,483,648                          | 2,147,483,647                           |
| `u32`    | 32       | No         | 0                                       | 4,294,967,295                           |
| `i64`    | 64       | Yes        | -9,223,372,036,854,775,808              | 9,223,372,036,854,775,807              |
| `u64`    | 64       | No         | 0                                       | 18,446,744,073,709,551,615             |
| `i128`   | 128      | Yes        | -170,141,183,460,469,231,731,687,303,715,884,105,728 | 170,141,183,460,469,231,731,687,303,715,884,105,727 |
| `u128`   | 128      | No         | 0                                       | 340,282,366,920,938,463,463,374,607,431,768,211,455 |

---

### Summary  

- Signed integers (`i8`, `i16`, etc.) are suitable for data with both positive and negative values.  
- Unsigned integers (`u8`, `u16`, etc.) provide larger positive ranges but do not support negative values.  
- The default type for integers in *lotus* is `i64`.  
- Always ensure that your values fall within the range of the specified data type to avoid errors.