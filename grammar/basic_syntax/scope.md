### **Scope in Lotus**

In Lotus, **scope** refers to the region in a program where a variable, function, or object is accessible. Understanding scope is crucial to manage variable visibility, avoid name conflicts, and optimize memory usage.

---

### **Types of Scope in Lotus**

1. **Global Scope**  
2. **Local Scope**  
3. **Class/Instance Scope**  
4. **Static Scope**  
5. **Block Scope**

---

### **1. Global Scope**

Variables or functions declared in the global scope are accessible throughout the program unless shadowed by local variables.

#### **Example**
```lotus
let global_var = 100

def ShowGlobalVar() {
    print(global_var)  // Access global variable
}

ShowGlobalVar()  // Output: 100
```

- **Key Points**:
  - Declared outside any function, class, or block.
  - Accessible anywhere unless redefined in a narrower scope.

---

### **2. Local Scope**

Variables declared within a function or block are only accessible within that specific function or block.

#### **Example**
```lotus
def LocalScopeDemo() {
    let local_var i32 = 50
    print(local_var)  // Accessible here
}

LocalScopeDemo()

// print(local_var)  // Error: local_var is not defined in the global scope
```

- **Key Points**:
  - Limited to the enclosing function or block.
  - Reduces the risk of unintended modifications.

---

### **3. Class/Instance Scope**

#### **Example**
```lotus
class MyClass {
    let instance_var i32 = 10
}

def (obj MyClass) ShowInstanceVar() {
    print(obj.instance_var)  // Access instance-specific variable
}

let my_instance = MyClass()
my_instance.ShowInstanceVar()  // Output: 10
```

- **Key Points**:
  - Variables are tied to a specific instance of the class.
  - Accessed through the object using `self`.

---

### **4. Static Scope**

Static variables belong to the class rather than any specific instance. They retain their value across instances and function calls.

#### **Example**
```lotus
class MyClass {
    static static_var i32 = 0
}

def IncrementStaticVar() {
    MyClass.static_var += 1
    print(MyClass.static_var)
}

IncrementStaticVar()  // Output: 1
IncrementStaticVar()  // Output: 2
```

- **Key Points**:
  - Declared with the `static` keyword.
  - Shared among all instances of the class.
  - Useful for counting instances or shared states.

---

### **5. Block Scope**

Variables declared inside loops, conditional statements, or other blocks are only accessible within that block.

#### **Example**
```lotus
if true {
    let block_var int = 20
    print(block_var)  // Accessible here
}

// print(block_var)  // Error: block_var is not accessible outside the block
```

- **Key Points**:
  - Limited to the specific block.
  - Enhances code readability and prevents accidental variable reuse.

---

### **Scope Shadowing**

A variable in a narrower scope (e.g., local) can shadow a variable with the same name in a broader scope (e.g., global).

#### **Example**
```lotus
let var_name int = 100

def ShadowScope() {
    let var_name int = 50  // Shadows the global var_name
    print(var_name)  // Output: 50
}

ShadowScope()
print(var_name)  // Output: 100
```

---

### **Scope and Lifetime**

- **Scope**: Where a variable can be accessed.
- **Lifetime**: How long a variable exists in memory.
  - **Global variables** persist throughout the program's execution.
  - **Local variables** exist only during function execution.
  - **Static variables** persist for the program's lifetime but are scoped to the class.

---

### **Best Practices**

1. **Use Local Scope Where Possible**:
   - Reduces memory usage and avoids unintended side effects.
2. **Avoid Overusing Global Variables**:
   - Can lead to conflicts and harder-to-debug code.
3. **Leverage Static Variables for Shared State**:
   - Use them for counters, caches, or shared configurations.
4. **Name Variables Intuitively**:
   - Avoid shadowing unintentionally by naming variables descriptively.

---

### **Conclusion**

Understanding scope in Lotus helps developers write clean, efficient, and bug-free code by controlling variable accessibility and lifetime effectively. By leveraging the different scopes—global, local, class, static, and block—developers can build maintainable and organized programs.