### **MyLang Classes Documentation**

In MyLang, classes serve as templates for creating objects, encapsulating data (variables) and behaviors (methods). However, **functions cannot be defined within the body of the class itself**. Instead, all methods, including constructors (`__init__`) and destructors (`__dest__`), are declared outside the class body using a consistent syntax.

---

### **Class Variables**
1. **Public Variables:**  
Accessible from anywhere. Defined without a prefix.
```b2
let name string = ""
```

2. **Protected Variables:**  
Accessible only within the class and subclasses. Prefixed with `_`.
```b2
let _protected_var string = ""
```

3. **Private Variables:**  
Accessible only within the class. Prefixed with `__`.
```b2
let __private_var string = ""
```

4. **Static Variables:**  
Shared among all instances. Defined using the `static` keyword.
```b2
static count int = 0
```

---

### **Constructors and Destructors**
1. **Constructor (`__init__`):**  
Initializes an object’s attributes.  
Declared outside the class body.  
```b2
def (mcls &MyClass) __init__(name str) {
    mcls.name = name
    mcls.count += 1  // or MyClass.count += 1
}
```

2. **Destructor (`__dest__`):**  
Called when an object is deleted or goes out of scope.  
Declared outside the class body.  
```b2
def (mcls &MyClass) __dest__() {
    print(mcls.name + " is being destroyed")
}
```

---

### **Methods**
1. **Instance Methods:**
```b2
def (mcls MyClass) ShowInfo() {
    print("Name: " + mcls.name)
}
```

2. **Mutable Methods (Reference):**  
Use a reference (`&`) to modify the object’s properties.
```b2
def (mcls &MyClass) ChangePrivateVar(new_val str) {
    mcls.__private_var = new_val
}
```

3. **Static Methods:**  
```b2
def MyClass.StaticMethod() {
    print("Static count: " + MyClass.count.toString())
}
```

---

### **Operator Overloading**
Operators can be overloaded by defining specific methods outside the class body.  
Supported operators include:
- `__add__` for `+`
- `__sub__` for `-`
- `__eq__` for `==`
- `__lt__` for `<`

#### Example:
```b2
def (mcls MyClass) __add__(other MyClass) MyClass {
    let new_name string = mcls.name + other.name
    return MyClass(new_name)
}
```

---

### **String Representation**
1. **`__str__` Method:**  
Returns a human-readable string. Called by `print(obj)`.  
```b2
def (mcls MyClass) __str__() string {
    return "MyClass(name=" + mcls.name + ")"
}
```

2. **`__repr__` Method:**  
Returns a developer-friendly string. Called by `repr(obj)`.  
```b2
def (mcls MyClass) __repr__() string {
    return "MyClass('" + mcls.name + "')"
}
```

---

### **Function Overloading**
Methods with the same name but different parameter types or counts can coexist.

#### Example:
```b2
def (mcls MyClass) greet() {
    print("Hello!")
}

def (mcls MyClass) greet(name str) {
    print("Hello, " + name + "!")
}
```

---

### **Sample Class Implementation**
```b2
class MyClass {
    let name string  // str default value: ""
    let _protected_var string  // str default value: ""
    let __private_var string  // str default value: ""
    static count int  // int default value: 0
}

// Constructor
def (mcls &MyClass) __init__(name str) {
    mcls.name = name
    mcls.count += 1
}

// Instance Method
def (mcls MyClass) ShowInfo() {
    print("Name: " + mcls.name)
}

// Mutable Instance Method
def (mcls &MyClass) ChangePrivateVar(new_val str) {
    mcls.__private_var = new_val
}

// Destructor
def (mcls &MyClass) __dest__() {
    print("Object with name " + mcls.name + " is being destroyed")
}

// Overloaded Method
def (mcls MyClass) greet() {
    print("Hello!")
}

def (mcls MyClass) greet(name str) {
    print("Hello, " + name + "!")
}
```

---

### **Key Features**
1. **Encapsulation:**  
   Use public, protected, and private variables.
2. **Inheritance:**  
   Extend classes to reuse functionality.
3. **Polymorphism:**  
   Enabled by function and operator overloading.
4. **Static Context:**  
   Shared variables and methods.

MyLang’s class structure is designed to separate declaration and functionality, emphasizing clarity and modularity.