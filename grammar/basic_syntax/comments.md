### Comments in lotus

Comments in *lotus* can be used to  
- Explain the code.  
- Improve code readability.  
- Temporarily prevent code execution for testing or debugging.  

### Single-Line Comments  
Single-line comments start with `//`. Anything after `//` is ignored by the compiler.  

**Example:**  
```lotus
pkg main

def main() {
    // This is a single-line comment
    print("Hello, World!")
}
```

Single-line comments can also be placed at the end of a line  
```lotus
pkg main

def main() {
    print("Hello, World!")  // This is a comment
}
```

### Multiline Comments  
Multiline comments are enclosed within `/*` and `*/`.  

**Example:**  
```lotus
/* This is a comment
   written in
   multiple lines */
print("Hello, World!")
```

### Alternative Multiline Comments  
Multiline strings (using triple quotes) can be used as comments. As long as the string is not assigned to a variable, it will be ignored by the compiler.  

**Example:**  
```lotus
pkg main

def main() {
    """
    This is a comment
    written in
    multiple lines
    """
    print("Hello, World!")
}
```

This allows flexibility in writing detailed comments without affecting the program execution.