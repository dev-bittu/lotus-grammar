### **The `__iter__` and `__next__` Methods in MyLang**

In MyLang, `__iter__` and `__next__` are special methods used to create iterable objects. An object is considered iterable if it implements the `__iter__` method, and the `__next__` method is used to iterate through the elements of that object.

---

### **Key Concepts**

1. **Iterable Object**: An object that implements the `__iter__` method and returns an iterator.
2. **Iterator**: An object that implements the `__next__` method, which returns the next element in the sequence.

---

### **How It Works**
- **`__iter__`**: Should return the iterator object itself. This method is called when the iteration is initialized (e.g., in a `for` loop).
- **`__next__`**: Should return the next value in the sequence. If there are no more items to return, it should raise a `StopIteration` exception.

---

### **Example: Creating an Iterable Class**

```lotus
class MyNumbers {
    let start i32 = 0
    let end i32 = 10
}

// Initialize the iterable object
def (mynum &MyNumbers) __iter__() &MyNumbers {
    mynum.start = 0
    return mynum
}

// Define the next item in the sequence
def (mynum &MyNumbers) __next__() int {
    if mynum.start < mynum.end {
        let current = mynum.start
        mynum.start += 1
        return current
    } else {
        throw StopIteration()
    }
}
```

---

### **Using the Iterable**
The object can now be used in a `for` loop or manually iterated with `__next__`:

```lotus
let nums = MyNumbers()

// Using the object in a for loop
for num in nums {
    print(num) 
}
// Output: 0, 1, 2, ..., 9

// Manual iteration
let iterator = nums.__iter__()
try {
    while true {
        print(iterator.__next__())
    }
} catch StopIteration {
    print("Iteration complete.")
}
```

---

### **Customizing Iteration**
You can customize the range, step, or sequence by modifying the logic in `__iter__` and `__next__`.

#### **Example: Custom Step Size**
```lotus
class MyNumbers {
    let start = 0
    let end = 10
    let step = 2
}

def (mynum &MyNumbers) __iter__() &MyNumbers {
    mynum.start = 0
    return mynum
}

def (mynum &MyNumbers) __next__() int {
    if mynum.start < mynum.end {
        let current = mynum.start
        mynum.start += mynum.step
        return current
    } else {
        throw StopIteration()
    }
}

// Usage
let nums = MyNumbers()
for num in nums {
    print(num)
}
// Output: 0, 2, 4, 6, 8
```

---

### **Combining with Generators**
Using `__iter__` and `__next__`, you can replicate generator-like behavior in custom classes.

---

### **Key Points**
1. **`__iter__`**:
   - Called when iteration begins.
   - Should return the iterator object (usually `self`).
   
2. **`__next__`**:
   - Called to fetch the next item.
   - Must raise `StopIteration` when the sequence ends.

3. **Use Cases**:
   - Implementing custom sequences.
   - Generating infinite or conditional sequences.

4. **Integration**:
   - Fully compatible with `for` loops and manual iteration.

By implementing these methods, your custom objects can seamlessly integrate with MyLang's iteration protocols, enabling efficient and reusable iteration.