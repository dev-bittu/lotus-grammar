# Exporting in lotus

In **lotus**, variables, functions, classes, interfaces, and other entities follow a simple and intuitive exporting mechanism to control visibility and accessibility across packages. The system ensures flexibility without introducing unnecessary verbosity or complexity.

---

## **Basic Rules for Exporting**
1. **Public by Default:**  
   All entities (variables, functions, classes, interfaces, etc.) are **public by default** and can be accessed from outside the package.

2. **Private Prefix (_):**  
   Any entity prefixed with an underscore (`_`) is **private** to the package and will not be exported.  
   - Example:  
     ```lotus
     let (
         some_var = 42       // Public
         _private_var = 23   // Private
     )
     const (
         CONST_VAR = 3.14    // Public
         _CONST_VAR = "lotus"   // Private
     )
     ```

3. **Explicit Control with `pkg.lt`:**  
   Each package can include a special file named `pkg.lt` (similar to Python’s `__init__.py`) to explicitly define what to **include** or **exclude** from being exported.  
   - You can **either** include or exclude but not both within a single `pkg.lt` file.
   - The rules defined in `pkg.lt` apply **only** to entities that are not explicitly marked as private with `_`.

---

## **Using `pkg.lt`**
The `pkg.lt` file is optional but provides fine-grained control for exporting. It must reside in the package directory.

### **Including Entities**
When you list entities in the `pkg.lt` file, only the specified ones are exported, and everything else becomes private.  

- **Example:**
  ```lotus
  // pkg.lt
  export [
      some_var
      CONST_VAR
      SomeClass
  ]
  ```
  - In this example:
    - `some_var`, `CONST_VAR`, and `SomeClass` are exported.
    - Everything else in the package is private.

### **Excluding Entities**
You can list entities to explicitly exclude them from being exported.

- **Example:**
  ```lotus
  // pkg.lt
  exclude [
      _private_var
      CONST_VAR
      InternalClass
  ]
  ```
  - In this example:
    - `_private_var`, `CONST_VAR`, and `InternalClass` are not exported.
    - Everything else in the package is public.

---

## **Priority of Rules**
1. **Private Prefix (`_`)**  
   Entities prefixed with `_` are always private, even if listed in `include` in `pkg.lt`.

   - Example:  
     ```lotus
     let _never_exported = 42
     ```
     This variable will **never** be exported, even if explicitly included in `pkg.lt`.

2. **`pkg.lt` File**  
   The rules defined in `pkg.lt` apply only to entities that are not explicitly marked with `_`.

---

## **Why This Approach?**
The design ensures:
- **Simplicity:** No verbose syntax is required for controlling visibility.  
- **Consistency:** Naming conventions like `_` are easy to understand.  
- **Flexibility:** The `pkg.lt` file allows explicit control for larger packages.  
- **Readability:** Developers can quickly identify public vs. private entities without additional annotations.

---

## **How Other Languages Handle Exporting**
Here’s how other languages deal with exporting, influencing lotus's design:  

| Language       | Exporting Mechanism                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Python**     | Prefix `_` for private members; explicit imports in `__init__.py`.                                                                                      |
| **Go**         | Public entities start with an uppercase letter; private ones start with lowercase.                                                                      |
| **Rust**       | Explicit `pub` keyword for public entities; private by default.                                                                                         |
| **JavaScript** | Use `export` keyword to define public entities; private ones are simply not exported.                                                                   |
| **C++**        | Public/private keywords define access levels within classes; exporting from libraries requires manual configuration (e.g., using `__declspec(dllexport)`). |
| **Java**       | Uses `public`, `protected`, `private` access modifiers; packages require explicit imports.                                                              |

---

## **Best Practices**
1. Use `_` for truly private entities to avoid accidental misuse.
2. Prefer using `pkg.lt` for larger packages where fine-grained control is necessary.
3. Keep your exported API surface minimal to reduce complexity for users of your package.
4. Always document public exports for clarity.
