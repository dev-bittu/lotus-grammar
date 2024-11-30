### **Inheritance and Interfaces in MyLang**

Inheritance allows a class (child) to acquire properties and methods of another class (parent). Interfaces define a contract that classes must implement. MyLang supports:

- **Class inheritance** using the `extends` keyword.  
- **Interface implementation** using the `impl` keyword.

---

### **Class Inheritance**
A class can inherit from another class to reuse its properties and methods. The child class can also override methods from the parent class.

#### **Syntax**
```b2
class Parent {
    let name string = "Parent"
}

class Child extends Parent {
    let child_name string = "Child"
}
```

---

#### **Example**
```b2
class Parent {
    let name string = "Parent"

    def (p Parent) greet() {
        print("Hello from " + p.name)
    }
}

class Child extends Parent {
    let child_name string = "Child"
}

// Child-specific method
def (c Child) showChildName() {
    print("Child name: " + c.child_name)
}

// Overriding Parent's method
def (c Child) greet() {
    print("Hello from the Child class!")
}
```

#### **Usage**
```b2
let parent = Parent()
parent.greet() // Output: Hello from Parent

let child = Child()
child.greet()        // Output: Hello from the Child class!
child.showChildName() // Output: Child name: Child
```

---

### **Interface Implementation**
Interfaces define a set of methods that a class must implement. A class can implement multiple interfaces using the `impl` keyword.

#### **Syntax**
```b2
interface Animal {
    def sound() str
    def move() str
}

class Dog impl Animal {
    let name string = "Dog"
}
```

#### **Example**
```b2
interface Animal {
    def sound() str
    def move() str
}

class Dog impl Animal {
    let name string = "Dog"
}

// Implementing interface methods
def (d Dog) sound() str {
    return "Bark"
}

def (d Dog) move() str {
    return "Run"
}
```

#### **Usage**
```b2
let dog Animal = Dog()
print(dog.sound()) // Output: Bark
print(dog.move())  // Output: Run
```

---

### **Combining Inheritance and Interfaces**
MyLang allows a class to extend a base class and implement multiple interfaces simultaneously.

#### **Example**
```b2
class Vehicle {
    let type string = "Generic Vehicle"
}

interface Fuel {
    def refuel() str
}

interface Electric {
    def charge() str
}

class Car extends Vehicle impl Fuel, Electric {
    let brand string = "Car Brand"
}

// Implementing interface methods
def (c Car) refuel() str {
    return "Refueling the car!"
}

def (c Car) charge() str {
    return "Charging the car!"
}

// Overriding Vehicle's property
def (c Car) getType() str {
    return "Car"
}
```

#### **Usage**
```b2
let car = Car()
print(car.refuel()) // Output: Refueling the car!
print(car.charge()) // Output: Charging the car!
print(car.getType()) // Output: Car
```

---

### **Key Features of Inheritance and Interfaces in MyLang**
1. **Class Inheritance (`extends`):**
   - Reuse methods and variables from parent classes.
   - Override methods in the child class.
   - Supports single inheritance.

2. **Interfaces (`impl`):**
   - Define a contract with method signatures.
   - A class must implement all methods of an interface.
   - Supports multiple interface implementations.

3. **Separation of Concerns:**
   - Classes define data and behavior.
   - Interfaces focus on behavior contracts.

MyLang ensures flexibility and modularity by supporting both **inheritance** and **interfaces**, allowing developers to build scalable and maintainable code.