### **Polymorphism in Lotus**

Polymorphism is one of the key principles of Object-Oriented Programming (OOP). In Lotus, **polymorphism** allows objects of different classes to be treated as objects of a common superclass. This enables writing flexible and reusable code that works with objects of different types in a uniform way.

---

### **Types of Polymorphism**

1. **Compile-Time Polymorphism (Method Overloading)**:
   - Allows multiple methods in the same scope to have the same name but different parameters.
   - The method to be executed is determined at compile time based on the arguments provided.

2. **Run-Time Polymorphism (Method Overriding)**:
   - Enables a subclass to provide a specific implementation of a method already defined in its superclass.
   - The method to be executed is determined at runtime based on the object's type.

---

### **Method Overloading**

Lotus supports **method overloading** by defining multiple versions of a function with the same name but different parameter counts or types.

#### **Example: Method Overloading**
```lotus
def CalculateArea(length i32, width i32) i32 {
    return length * width
}

def CalculateArea(radius f32) f32 {
    return 3.14 * radius * radius
}

// Usage
let rect_area = CalculateArea(5, 10)  // Calls the first function
print(rect_area)  // Output: 50

let circle_area = CalculateArea(7.5)  // Calls the second function
print(circle_area)  // Output: 176.625
```

---

### **Method Overriding**

Lotus supports **method overriding** where a subclass can redefine methods from its parent class to provide a specialized behavior.

#### **Example: Method Overriding**
```lotus
class Animal {
    def Speak() str {
        return "Some generic animal sound"
    }
}

class Dog extends Animal {
    def Speak() str {
        return "Woof Woof!"
    }
}

class Cat extends Animal {
    def Speak() str {
        return "Meow!"
    }
}

// Usage
let animals list<Animal> = [Dog(), Cat(), Animal()]

for animal in animals {
    print(animal.Speak())
}
// Output:
// Woof Woof!
// Meow!
// Some generic animal sound
```

---

### **Polymorphism with Interfaces**

Polymorphism in Lotus also works through **interfaces**, where different classes implement the same interface but provide different behaviors.

#### **Example: Polymorphism with Interfaces**
```lotus
interface Shape {
    def Area() f32
}

class Rectangle impl Shape {
    let length f32
    let width f32

    def (rect Rectangle) Area() f32 {
        return rect.length * rect.width
    }
}

class Circle impl Shape {
    let radius f32

    def (circle Circle) Area() f32 {
        return 3.14 * circle.radius * circle.radius
    }
}

// Usage
let shapes Shape = [Rectangle(5, 10), Circle(7)]

for shape in shapes {
    print(shape.Area())
}
// Output:
// 50.0
// 153.86
```

---

### **Polymorphism with Functions**

You can use polymorphism in functions by designing them to work with parent classes or interfaces.

#### **Example: Function Accepting Multiple Types**
```lotus
def DescribeAnimal(animal Animal) {
    print(animal.Speak())
}

DescribeAnimal(Dog())  // Output: Woof Woof!
DescribeAnimal(Cat())  // Output: Meow!
```

---

### **Key Points**
1. **Flexibility**:
   - Polymorphism enables functions and methods to handle objects of different types in a unified way.

2. **Code Reusability**:
   - By working with base classes or interfaces, you can avoid writing separate code for each object type.

3. **Extensibility**:
   - New classes can be added without changing existing polymorphic code, making the system more extensible.

4. **Compile-Time Polymorphism**:
   - Achieved through method overloading.

5. **Run-Time Polymorphism**:
   - Achieved through method overriding and interface implementation.

---

### **Conclusion**
Polymorphism in Lotus allows for designing clean, efficient, and scalable code. By leveraging method overloading, overriding, and interface-based polymorphism, developers can create robust applications that are easy to maintain and extend.