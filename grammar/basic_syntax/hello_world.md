# Hello World in Mylang

Welcome to the first example of programming with **Mylang**! This guide will walk you through creating a simple "Hello, World!" program, which demonstrates the foundational syntax for defining functions, outputting text, and understanding the basics of Mylang.

## Overview of "Hello, World!"

The "Hello, World!" program outputs the text "Hello, World!" to the console. It's a traditional beginner program that introduces the structure and syntax of a language. In Mylang, this program includes a function declaration, a print statement, and comments.

## Program Example

Here’s the code for a "Hello, World!" program in Mylang:

```plaintext
package main

// Main function is the entry point
fn main() (int) {
    // Output a greeting message
    print("Hello, World!");
    return 0;
}
```

### Program Breakdown

1. **Comments**:
   Comments in Mylang help annotate code without affecting its execution. Mylang supports:

   - **Single-line comments**: Begin with `//`. For example:
```plaintext
// This is a single-line comment
```
   - **Multi-line comments**: (if available) look like:
```plaintext
/* This is a
multi-line comment 
*/
```

2. **Function Declaration**:  
   Functions in Mylang start with the `fn` keyword. Every Mylang program begins with the `main` function:

```plaintext
fn <function_name>(<args>) (<return types>) {
   <statements>
}
```

   - `main`: The entry point, called automatically when the program runs.
   - `{ ... }`: Encloses the function body containing the executable statements.

3. **Print Statement**:  
   The `print` function displays text or variable data on the console:

```plaintext
print(<expression>);
```

   In our example, `print("Hello, World!");` outputs `"Hello, World!"` to the console.

4. **String Literals**:  
   Text data, or string literals, are wrapped in double quotes (`"`), such as `"Hello, World!"`.

---

## Detailed Grammar Rules

This section covers the essential grammar rules in Mylang as applied in the "Hello, World!" example:

1. **Function Definition Rule**:

   - **Syntax**:
```plaintext
    fn <identifier>() {
        <statements>
    }
```
   - **Explanation**:
     - `fn`: Declares a function.
     - `<identifier>`: Function name (e.g., `main`).
     - `()`: Parentheses where parameters go if needed (none here).
     - `{}`: Curly braces enclosing the function's body.
     - `<statements>`: Each line in the function body ends with a semicolon (`;`).

2. **Print Statement Rule**:

   - **Syntax**:
```plaintext
print(<string_literal>);
```
   - **Explanation**:
     - `print`: Outputs text or variables.
     - `<string_literal>`: Text to print, wrapped in double quotes.

3. **String Literal Rule**:

   - **Syntax**:
```plaintext
    "<text>"
```
   - **Explanation**:
     - Enclose strings in double quotes. For example, `"Hello, World!"`.

4. **Comments Rule**:
   - **Single-line Comments**:
```plaintext
    // Single-line comment
```
   - **Multi-line Comments**:
```plaintext
    /* Multi-line
        comment */
```

---

## Execution Flow

1. **Define the `main` Function**: Program execution starts with the `main()` function.
2. **Execute Print Statement**: The `print("Hello, World!");` command outputs the specified string to the console.
3. **End Program**: When all statements in `main()` execute, the program ends.

---

## Running the Program

To execute the "Hello, World!" program in Mylang:

1. **Save the Code**: Save the code in a `.myl` file (e.g., `hello_world.myl`).
2. **Compile or Interpret**: Run the program using the Mylang compiler or interpreter. Example commands:
```bash
mylang run hello_world.mylang
```
Or to build and execute:
```bash
mylang build -o hello_world.exe hello_world.mylang
./hello_world.
```
3. **Expected Output**:
```plaintext
Hello, World!
```

## Common Errors

- **Missing Semicolon**: Statements end with a semicolon (`;`). Omitting this causes syntax errors.
- **Mismatched Braces**: Every opening `{` must have a closing `}`.
- **Case Sensitivity**: Mylang is case-sensitive, so `Main` and `main` are different. Always use `main` for the entry point.

---

## Additional Mylang Features

1. **Anonymous Function**: Mylang supports anonymous functions:

```plaintext
fn(<args>) {
   print("Hello");
}
```

2. **String Formatting**:
   - Regular string: `"hello"`
   - Tab character: `"hello\tworld"` outputs `"hello    world"`
   - Raw string (ignores escape sequences): `r"hello\tworld"` outputs `"hello\tworld"`
   - f-strings for variable insertion:
```plaintext
f"hello {name}"  // outputs "hello <value_of_name_var>"
```
   - Using `format` method:
```plaintext
"hello {}".format(name)  // outputs "hello <value_of_name_var>"
```

---

## Summary

The "Hello, World!" example introduces Mylang's core structure:

- **Function Declarations**: Use `fn` to define functions.
- **Print Statements**: Use `print()` to output text.
- **Syntax Rules**: Familiarize yourself with comments, string literals, and function syntax.

With this foundation, you're ready to explore Mylang's more advanced features and start coding with confidence. Happy coding!
