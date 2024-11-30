### **Arrays in *b2***

Arrays in *b2* are fixed-size, ordered collections of elements, where each element can be of a specific data type. Arrays are similar to lists but differ in that their size is fixed at the time of creation. Once an array is initialized, you cannot change its size, but you can modify its individual elements.

---

### **Creating an Array**

Arrays in *b2* are created using the `array<type, size>()` syntax, where `type` represents the data type of the elements in the array, and `size` specifies the number of elements the array will hold. Here are a few ways to create an array:

1. **Array with Mixed Data Types (using `any` type)**:
   ```b2
   myarr := array<any, 3>("string", True, 78)
   ```
   In this example, the array can hold three elements of mixed data types: a string, a boolean, and an integer.

2. **Array of Integers**:
   ```b2
   let myarr = array<i32, 3>(23, 24, 12)
   ```
   This creates an integer array with 3 elements initialized with values `23`, `24`, and `12`.

3. **Array of Integers with Default Values**:
   ```b2
   let myarr array<i32, 3>  // Creates an integer array of size 3 with default values (0 for i32)
   ```
   Here, an array of size `3` is initialized, but no values are explicitly provided. The elements will default to `0` for integers.

---

### **Accessing Array Items**

Accessing array elements is done via their indices, similar to lists. Indices start from `0`.

```b2
let myarr = array<i32, 3>(23, 24, 12)
print(myarr[0])  // Output: 23 (First item)
print(myarr[2])  // Output: 12 (Third item)
```

You can also use negative indexing to access elements from the end of the array:

```b2
print(myarr[-1])  // Output: 12 (Last item)
print(myarr[-2])  // Output: 24 (Second to last item)
```

---

### **Changing Array Items**

You can modify the elements of an array by assigning a new value to a specific index. However, note that arrays in *b2* are fixed in size, so you cannot add or remove elements once created.

```b2
myarr[1] = 30  // Change the second item to 30
print(myarr)    // Output: array(23, 30, 12)
```

---

### **Adding Items to an Array**

Unlike lists, arrays in *b2* have a fixed size, meaning you cannot dynamically add elements to them after initialization. However, you can update or modify existing elements.

---

### **Removing Items from an Array**

Similar to adding items, you cannot remove items from an array since the size is fixed. However, you can set an element to a default or `null` value if needed.

```b2
myarr[2] = 0   // Set the third item to 0 (effectively removing it)
print(myarr)   // Output: array(23, 30, 0)
```

---

### **Looping Through an Array**

You can loop through the elements of an array using a `for` loop.

```b2
for item in myarr {
    print(item)  // Output: 23, 30, 12
}
```

You can also loop through the array using the `enumerate()` function to get both the index and the item:

```b2
for index, item in enumerate(myarr) {
    print(f"Index {index}: {item}")
}
```

---

### **Sorting an Array**

Unlike lists, arrays in *b2* do not support sorting directly since their size is fixed. However, you can create a new array from the sorted list if necessary:

```b2
let sortedArr = array<i32, 3>(12, 23, 30)
let sortedCopy = sortedArr.sort()  // Returns a new sorted array
print(sortedCopy)  // Output: array(12, 23, 30)
```

---

### **Copying an Array**

Arrays can be copied by directly assigning the array to another variable. This creates a shallow copy of the array.

```b2
let myarrCopy = myarr  // Copies the array
print(myarrCopy)        // Output: array(23, 30, 12)
```

Note that since arrays are fixed-size, copying does not require resizing.

---

### **Joining Arrays**

To join two arrays together, you can use the `+` operator. This creates a new array with elements from both arrays.

```b2
let arr1 = array<i32, 3>(1, 2, 3)
let arr2 = array<i32, 3>(4, 5, 6)
let joinedArr = arr1 + arr2  // Joins arr1 and arr2
print(joinedArr)              // Output: array(1, 2, 3, 4, 5, 6)
```

---

### **Array Methods**

Here are some commonly used methods for working with arrays in *b2*:

| Method               | Description                                            | Example                                       |
|----------------------|--------------------------------------------------------|-----------------------------------------------|
| `sort()`             | Sorts the array in ascending order                     | `myarr.sort()`                                |
| `copy()`             | Creates a shallow copy of the array                     | `let myarrCopy := myarr.copy()`               |
| `index(value)`       | Returns the index of the first occurrence of a value    | `let idx := myarr.index(24)`                  |
| `count(value)`       | Returns the number of occurrences of a value            | `let count := myarr.count(24)`                |
| `reverse()`          | Reverses the order of elements in the array             | `myarr.reverse()`                             |

---

### **Example Usage**

```b2
// Creating an array
let myarr = array<i32, 3>(23, 24, 12)
print(myarr)  // Output: array(23, 24, 12)

// Accessing array items
print(myarr[0])  // Output: 23
print(myarr[-1])  // Output: 12

// Changing array items
myarr[1] = 30
print(myarr)  // Output: array(23, 30, 12)

// Looping through an array
for item in myarr {
    print(item)  // Output: 23, 30, 12
}

// Sorting an array (if applicable)
let sortedArr = array<i32, 3>(12, 23, 30)
let sortedCopy = sortedArr.sort()
print(sortedCopy)  // Output: array(12, 23, 30)

// Copying an array
let myarrCopy = myarr.copy()
print(myarrCopy)  // Output: array(23, 30, 12)

// Joining arrays
let arr1 = array<i32, 3>(1, 2, 3)
let arr2 = array<i32, 3>(4, 5, 6)
let joinedArr = arr1 + arr2
print(joinedArr)  // Output: array(1, 2, 3, 4, 5, 6)
```

---

### **Conclusion**

Arrays in *b2* are fixed-size collections that offer efficient access and manipulation of their elements. They are a suitable choice when the number of elements is known ahead of time and when the size of the collection does not need to change. Arrays provide several useful methods for sorting, copying, and interacting with the elements, making them a powerful tool for managing data in *b2* programs.