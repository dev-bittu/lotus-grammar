# Namespaces in lotus
Namespaces in **lotus** are designed to provide clear, modular, and collision-free code organization. They help group related entities (variables, functions, classes, etc.) and facilitate their usage in larger projects. lotus's namespace mechanism is intuitive, aligning with the goal of keeping the language simple and beginner-friendly.

---

## **What Are Namespaces?**
A **namespace** is a logical grouping of code entities (functions, classes, variables, etc.) that helps avoid naming conflicts and organizes code more efficiently. In lotus, namespaces are typically defined at the pkg level, where each pkg automatically acts as a namespace.

For example:  
```lotus
pkg utils

def add(a i32, b i32) i32 {
    return a + b
}
```
Here, `utils` is the namespace. To access `add` from another pkg, you’ll reference it as `utils.add`.

---

## **Defining a Namespace**
Namespaces in lotus are defined using the `pkg` keyword, which specifies the pkg name at the top of the file.  
- Example:  
  ```lotus
  pkg math

  def multiply(a i32, b i32) i32 {
      return a * b
  }
  ```

---

## **Using a Namespace**
To use a namespace, you import the corresponding pkg into your code. lotus supports importing specific items or entire namespaces for convenience.

### **Importing a pkg**
Use the `import` keyword to bring a namespace into your code:
```lotus
pkg main

import "github.com/dev-bittu/lotuslib/math"

def main() {
    let result = math.multiply(5, 3)
    print(result) // Output: 15
}
```

### **Alias a Namespace**
You can use an alias to simplify long namespace paths:
```lotus
pkg main

import "github.com/dev-bittu/lotuslib/math" as m

def main() {
    let result = m.multiply(5, 3)
    print(result) // Output: 15
}
```

---

## **Nested Namespaces**

Namespaces in lotus can be nested by organizing your code in directories. The directory structure determines the hierarchy of the namespaces.

### **Example Directory Structure**
```
lotuslib/
    math/
        basic.lt
        advanced.lt
```

### **Accessing Nested Namespaces**
```lotus
import (
    "github.com/dev-bittu/lotuslib/math/basic" as basicmath
    "github.com/dev-bittu/lotuslib/math/advanced" as advmath
)

def main() {
    let result1 = basicmath.add(5, 3)
    let result2 = advmath.sqrt(16)

    print(result1, result2) // Output: 8, 4
}
```

---

## **Namespace Rules**
1. **Global Uniqueness:**  
   Each pkg must have a unique namespace determined by its `pkg` declaration.
   
2. **Default Namespace:**  
   If no `pkg` is specified, the file belongs to the `main` pkg.

3. **Fully Qualified Names:**  
   You can always refer to entities using their fully qualified names if there's ambiguity.

4. **Imports Are Local:**  
   Imported namespaces are only accessible in the files where they are explicitly imported.

---

## **Handling Name Conflicts**

If two imported namespaces have conflicting names, use aliases to differentiate them.

### **Example:**
```lotus
import (
    "github.com/dev-bittu/mathlib/basic" as basicmath
    "github.com/dev-bittu/physicslib/basic" as basicphysics
)

def main() {
    let mathResult = basicmath.add(3, 4)
    let physicsResult = basicphysics.force(10, 5)

    print(mathResult, physicsResult)
}
```

---

## **Why Use Namespaces?**
Namespaces in lotus offer the following benefits:
- **Avoid Naming Conflicts:** Prevents clashes between identifiers in large projects.
- **Improved Organization:** Groups related code into logical units.
- **Code Reusability:** Promotes modular design and reusable components.
- **Readability:** Makes it clear where a function or class originates.

---

## **Comparison with Other Languages**

| Language       | Namespace Approach                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------|
| **Python**     | Uses modules and pkgs; imports control access to namespaces.                                       |
| **C++**        | Uses `namespace` keyword to define namespaces explicitly.                                              |
| **Java**       | Uses pkgs with a folder structure and the `import` keyword for access.                             |
| **C#**         | Uses `namespace` keyword to organize classes and functions; resolves conflicts with aliases.           |
| **Rust**       | Uses modules and `use` statements to manage namespaces.                                                |
| **Go**         | Each file's `pkg` declaration defines the namespace, with all files in a folder sharing a pkg. |

---

## **Best Practices**
1. Use descriptive and concise pkg names to improve readability.
2. Prefer aliases for long pkg names to make code cleaner.
3. Avoid overusing static imports as they can reduce clarity.
4. Organize nested namespaces logically to reflect the functionality they provide.

---

Namespaces in lotus are designed to balance simplicity and power, making them easy to use while enabling robust code organization.