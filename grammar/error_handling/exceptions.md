# Error Handling in Lotus
Lotus adopts a Go-like approach to error handling, ensuring simplicity and explicitness in dealing with errors. This method encourages developers to handle errors gracefully while keeping the language performant and beginner-friendly.

---

## **Overview**
In Lotus, functions that might encounter errors return a tuple containing:
1. The actual result (if any).
2. An error value (`null` if no error occurred).

This explicit error handling design makes it easy to:
- Identify and propagate errors.
- Avoid hidden exceptions or implicit behavior.

---

## **Basic Syntax**

### **Function Returning an Error**
```lotus
def divide(a int, b int) (int, error) {
    if b == 0 {
        return 0, "division by zero"
    }
    return a / b, null
}
```

### **Handling Errors**
```lotus
let result, err = divide(10, 0)
if err != null {
    print("Error:", err)
} else {
    print("Result:", result)
}
```

---

## **Error Propagation**
When a function encounters an error, it can propagate it to the caller using explicit return values.

### **Example**
```lotus
def read_file(filename str) (str, error) {
    // Simulate an error
    return "", "file not found"
}

def load_config() (str, error) {
    let content, err = read_file("config.txt")
    if err != null {
        return "", err
    }
    return content, null
}

def main(){
    let config, err = load_config()
    if err != null {
        print("Failed to load config:", err)
        exit(1)
    }
}
```

---

## **Best Practices**

1. **Check Errors Immediately**: Always check for errors right after a function call.
   ```lotus
   let value, err = some_function()
   if err != null {
       // Handle the error
   }
   ```

2. **Use Meaningful Error Messages**: Return descriptive error strings to make debugging easier.
   ```lotus
   return 0, "invalid input: b cannot be zero"
   ```

3. **Propagate Errors**: If you cannot handle an error, pass it up the call stack.
   ```lotus
   return "", err
   ```

4. **Group Error Constants**: For common error types, define constants for reuse.
   ```lotus
   const FILE_NOT_FOUND = "file not found"
   const INVALID_INPUT = "invalid input"
   ```

---

## **Advanced Techniques**

### **Error Wrapping**
Add context to errors before propagating them.
```lotus
let content, err = read_file("config.txt")
if err != null {
    return "", "load_config: " + err
}
```

### **Custom Error Types**
For more complex scenarios, you can define custom error types.
```lotus
struct CustomError {
    code int
    message str
}

def some_function() (int, CustomError?) {
    return 0, CustomError(404, "resource not found")
}

let result, err = some_function()
if err != null {
    print("Error Code:", err.code, "Message:", err.message)
}
```

---

## **Conclusion**

The Go-like approach to error handling in Lotus ensures:
- Explicit and clear error management.
- Minimal performance overhead.
- Flexibility for developers across various domains.

By adhering to this structured method, developers can write robust and maintainable code while leveraging Lotus's simplicity and performance.

