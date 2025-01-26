## **1.4 — Variable Assignment and Initialization in Lotus**   

### **Defining Variables in Lotus**  
Here’s a simple program that defines a single integer variable named `x`, and two additional integer variables `y` and `z`:

```lotus
pkg main

fn main() {
    let x i32    // define an integer variable named x
    let y, z i32 // define two integer variables, y and z

    return
}
```

### **Variable Assignment**  

After defining a variable, you can assign a value to it using the `=` operator. This process is called **assignment**.

```lotus
let width i32 // define an integer variable named width
width = 5     // assign the value 5 to variable width

// Now, variable width holds the value 5.
```

In Lotus, assignment copies the value on the right-hand side of the `=` operator to the variable on the left-hand side.  

Here’s an example where we use assignment multiple times to change the value of a variable:  

```lotus
pkg main

fn main() {
    let width i32  // define a variable named width
    width = 5      // assign 5 to width

    print(width)   // prints 5

    width = 7      // reassign width to 7
    print(width)   // prints 7
}
```

Output:  
```
5
7
```

When executed, this program demonstrates that variables in Lotus can hold only one value at a time, and a new assignment overwrites the previous value.

---

### **Variable Initialization**  

In Lotus, you can define and assign a value to a variable in a single statement. This is called **initialization**.  

```lotus
let width i32 = 5 // define and initialize variable width with 5
print(width)      // prints 5
```

### **Key Insight**  
Initialization provides an **initial value** for a variable, combining definition and assignment into one step.

---

### **Different Forms of Initialization in Lotus**  

Lotus supports various forms of initialization:  

```lotus
let a i32         // default-initialization (value: 0)

// Basic initialization:
let b i32 = 5     // direct-initialization
let c int? = null // nullable initialization
```

For uninitialized variables (like `a`), Lotus ensures they are set to a default value (e.g., `0` for numbers). This prevents undefined behavior caused by uninitialized variables.

---

### **Best Practices in Lotus**  

1. **Initialize your variables upon creation:**  
   Prefer defining and initializing variables in a single statement.  
   ```lotus
   let width = 5     // preferred
   let width i32 = 5 // preferred
   width := 5
   ```

2. **Avoid complex initialization on the same line:**  
   Each variable should have its own initializer.  
   ```lotus
   let a i32 = 4, b i32 = 5 // not prefered
   let (  // prefered
    a i32 = 4, 
    b = 5     
   )
   ```

3. **Use value-initialization for nullable types:**  
   ```lotus
   let name str? = null // initialize as null
   ```

4. **Understand the difference between `=` (assignment) and `==` (equality check):**  
   ```lotus
   if width == 5 {
       print("Width is 5")
   }
   ```