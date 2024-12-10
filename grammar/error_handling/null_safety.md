# Null Safety in lotus

Null values are often a source of bugs, particularly null pointer exceptions. lotus addresses this issue with **null safety**, making it easier for developers to work with nullable variables while minimizing the risk of errors. The language uses the `?` syntax to denote nullable types, ensuring clarity and control.

---

## Declaring Nullable Variables

In lotus, you can declare a nullable variable using the `?` syntax after the type. By default, non-nullable variables must always hold a value.

### Example:
```lotus
let name str? = null // Nullable variable
let age i32 = 25      // Non-nullable variable
```

- A nullable variable (`str?`) can either hold a value or be `null`.
- A non-nullable variable (`i32`) must always hold a valid value.

---

## Explicit Null Unwrapping

To access the value of a nullable variable, you can use the `!` operator. This asserts that the variable is not null at runtime.

### Example:
```lotus
let name str? = "John"
print(name!.length) // Output: 4
```

### Error Handling:
If the variable is `null` and you attempt to unwrap it using `!`, a **runtime error** is thrown.

```lotus
let name str? = null
print(name!.length) // Runtime error: null pointer exception
```

---

## Null Checking

Before using a nullable variable, you can check whether it is `null`. This ensures safety and prevents runtime errors.

### Example:
```lotus
let name str? = "Alice"

if name != null {
    print(name.length) // Output: 5
} else {
    print("Name is null")
}
```

### Null Coalescing:
Use the `??` operator to provide a default value when a nullable variable is `null`.

```lotus
let name str? = null
print(name ?? "Anonymous") // Output: Anonymous
```

---

## Nullable Function Parameters

Functions in lotus can accept nullable parameters by marking their types with `?`.

### Example:
```lotus
def greet(name str?) {
    if name != null {
        print("Hello, " + name)
    } else {
        print("Hello, guest!")
    }
}

greet("Jane") // Output: Hello, Jane
greet(null)   // Output: Hello, guest!
```

---

## Returning Nullable Types

Functions can return nullable types when a value might not always be present.

### Example:
```lotus
def findUser(id i32) str? {
    if id == 1 {
        return "Alice"
    }
    return null
}

let user = findUser(2)
print(user ?? "User not found") // Output: User not found
```

---

## Advantages of lotus's Null Safety

1. **Minimal Syntax**: The `?` and `!` operators provide an intuitive and concise way to handle nulls.
2. **Compile-Time Safety**: The type system enforces null checks wherever required, reducing bugs.
3. **Runtime Control**: Explicit unwrapping with `!` places responsibility on the developer, ensuring clarity in null assumptions.

---

## Common Patterns for Null Safety

### 1. Using Default Values
```lotus
let name str? = null
let finalName = name ?? "Default Name"
print(finalName) // Output: Default Name
```

### 2. Early Returns
```lotus
def printLength(name str?) {
    if name == null {
        print("No name provided")
        return
    }
    print(name.length)
}

printLength(null) // Output: No name provided
printLength("Eve") // Output: 3
```

### 3. Chaining Nullables
You can safely chain nullable operations using `if` or the `?` operator (to be explored further in extensions).

```lotus
let user str? = "Alice"
if user != null {
    print(user.toUpperCase())
}
```

---

## Summary

lotus’s null safety provides a modern and concise approach to managing nullability, reducing common pitfalls like null pointer exceptions. By leveraging the `?`, `!`, and `??` operators, developers can write safer and cleaner code while maintaining control over nullable values.