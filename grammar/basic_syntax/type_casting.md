### Specifying a Variable Type in *mylang*

In *mylang*, you can specify the type of a variable through **casting**. This allows you to convert values from one type to another. *mylang* uses constructor functions for casting, which work by converting one data type into another. This is especially useful when you want to ensure a variable has a specific type.

### Casting Constructor Functions

- **`i64()`**: Constructs an integer from a number, a float (by truncating decimals), or a string (if the string represents an integer).
- **`f32()`**: Constructs a float from an integer, a float, or a string (if the string represents a valid float or integer).
- **`str()`**: Constructs a string from various data types, including strings, integers, and floats.

### Example: Casting Integers
The `i64()` constructor can be used to convert various types into an integer:

```mylang
let x i64 = i64(1)    // x will be 1
let y i64 = i64(2.8)  // y will be 2 (decimal part is truncated)
let z i64 = i64("3")  // z will be 3 (string "3" is converted to integer)
```

### Example: Casting Floats
The `f32()` constructor converts values into a float type:

```mylang
let x f32 = f32(1)     // x will be 1.0 (converted from integer)
let y f32 = f32(2.8)   // y will be 2.8
let z f32 = f32("3")   // z will be 3.0 (string "3" is converted to float)
let w f32 = f32("4.2") // w will be 4.2
```

### Example: Casting Strings
The `str()` constructor converts values into strings:

```mylang
let x str = str("s1")  // x will be "s1"
let y str = str(2)     // y will be "2" (integer 2 is converted to string)
let z str = str(3.0)   // z will be "3.0" (float 3.0 is converted to string)
```

---

### Summary of Casting Constructors:

| Constructor | Converts To | Example                                |
|-------------|-------------|----------------------------------------|
| `i64()`     | Integer     | `i64(1)`, `i64(2.8)`, `i64("3")`      |
| `f32()`     | Float       | `f32(1)`, `f32(2.8)`, `f32("3")`      |
| `str()`     | String      | `str("s1")`, `str(2)`, `str(3.0)`      |

Casting allows you to flexibly work with different data types in *mylang* and ensure that variables are of the correct type for your logic.