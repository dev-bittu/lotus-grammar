### **Lists in *b2***

Lists in *b2* are ordered collections of items, which can be of any data type. They are mutable, meaning their content can be modified after creation. Lists are one of the most versatile data structures in *b2* and can hold any type of data, from numbers to strings, to other lists.

---

### **Creating a List**

In *b2*, lists can be created using square brackets `[]`. The syntax for creating a list is as follows:

1. **Empty List**:
   ```b2
   mylist := []  // or
   let mylist list = []  // or
   let mylist = []  // or
   let mylist list<any> = []  // This allows the list to hold any type of data.
   ```

2. **List of Integers**:
   ```b2
   let mylist list<int> = [1, 2, 4, 6]
   ```

In the second example, the list is specifically restricted to containing integers.

---

### **Accessing List Items**

Lists are ordered, so you can access individual elements by their index. Indexing in *b2* starts at `0`, meaning the first element of the list has an index of `0`.

```b2
let mylist list<int> = [1, 2, 4, 6]
print(mylist[0])  // Output: 1 (Accessing the first item)
print(mylist[2])  // Output: 4 (Accessing the third item)
```

You can also use negative indexing to access items from the end of the list:

```b2
print(mylist[-1])  // Output: 6 (Last item)
print(mylist[-2])  // Output: 4 (Second to last item)
```

---

### **Changing List Items**

To change a list item, you simply assign a new value to a specific index.

```b2
mylist[2] := 5  // Changing the third item to 5
print(mylist)   // Output: [1, 2, 5, 6]
```

---

### **Adding Items to a List**

You can add items to the end of a list using the `append()` method or by using the `+=` operator.

```b2
mylist.append(8)  // Adds 8 to the end of the list
print(mylist)     // Output: [1, 2, 5, 6, 8]

mylist += [9]     // Another way to append
print(mylist)     // Output: [1, 2, 5, 6, 8, 9]
```

---

### **Removing Items from a List**

You can remove items from a list using the `remove()` method, which removes the first occurrence of a specified value, or `pop()`, which removes and returns an item at a specific index (default is the last item).

```b2
mylist.remove(5)  // Removes the first occurrence of 5
print(mylist)     // Output: [1, 2, 6, 8, 9]

mylist.pop()      // Removes and returns the last item
print(mylist)     // Output: [1, 2, 6, 8]
```

To remove an item by index:

```b2
mylist.pop(1)     // Removes the item at index 1 (the second item)
print(mylist)     // Output: [1, 6, 8]
```

---

### **Looping Through a List**

You can loop through the items of a list using a `for` loop.

```b2
for item in mylist:
    print(item)  // Prints each item in the list
```

You can also loop using the `enumerate()` function to get both index and value:

```b2
for index, item in enumerate(mylist):
    print(f"Index {index}: {item}")
```

---

### **Sorting a List**

You can sort a list in ascending or descending order using the `sort()` method.

```b2
mylist := [6, 3, 8, 1, 4]
mylist.sort()  // Sorts in ascending order
print(mylist)  // Output: [1, 3, 4, 6, 8]

mylist.sort(descending=True)  // Sorts in descending order
print(mylist)  // Output: [8, 6, 4, 3, 1]
```

---

### **Copying a List**

To make a copy of a list, you can use the `copy()` method or slicing.

```b2
let mycopy := mylist.copy()
print(mycopy)  // Creates a shallow copy of the list

let mycopy := mylist[:]  // Another way to copy
print(mycopy)  // Output: Same as mylist
```

---

### **Joining Lists**

To join two or more lists together, you can use the `+` operator or the `extend()` method.

```b2
let list1 := [1, 2, 3]
let list2 := [4, 5, 6]

let joined := list1 + list2  // Join lists using '+'
print(joined)  // Output: [1, 2, 3, 4, 5, 6]

list1.extend(list2)  // Extend list1 with list2
print(list1)  // Output: [1, 2, 3, 4, 5, 6]
```

---

### **List Methods**

Here are some commonly used list methods in *b2*:

| Method               | Description                                        | Example                                  |
|----------------------|----------------------------------------------------|------------------------------------------|
| `append(value)`       | Adds an item to the end of the list                | `mylist.append(7)`                       |
| `remove(value)`       | Removes the first occurrence of a value            | `mylist.remove(7)`                       |
| `pop(index)`          | Removes and returns an item at the specified index | `mylist.pop(2)`                          |
| `sort()`              | Sorts the list in ascending order                  | `mylist.sort()`                          |
| `sort(descending=True)` | Sorts the list in descending order                | `mylist.sort(descending=True)`           |
| `copy()`              | Creates a shallow copy of the list                 | `mycopy := mylist.copy()`                |
| `extend(list)`        | Adds all elements of a list to the end of another list | `mylist.extend([7, 8])`               |
| `reverse()`           | Reverses the order of the list                     | `mylist.reverse()`                       |
| `index(value)`        | Returns the index of the first occurrence of a value | `mylist.index(5)`                      |
| `count(value)`        | Returns the count of occurrences of a value        | `mylist.count(5)`                        |

---

### **Example Usage**

```b2
// Creating a list
let fruits list<string> = ["apple", "banana", "cherry"]

// Accessing list items
print(fruits[1])  // Output: banana
print(fruits[-1])  // Output: cherry

// Changing list items
fruits[1] := "blueberry"
print(fruits)  // Output: ["apple", "blueberry", "cherry"]

// Adding items to a list
fruits.append("orange")
print(fruits)  // Output: ["apple", "blueberry", "cherry", "orange"]

// Removing items from a list
fruits.remove("cherry")
print(fruits)  // Output: ["apple", "blueberry", "orange"]

// Looping through a list
for fruit in fruits:
    print(fruit)  // Output: apple blueberry orange

// Sorting a list
fruits.sort()
print(fruits)  // Output: ["apple", "blueberry", "orange"]

// Copying a list
let fruitsCopy := fruits.copy()
print(fruitsCopy)  // Output: ["apple", "blueberry", "orange"]

// Joining lists
let moreFruits := ["grape", "melon"]
let allFruits := fruits + moreFruits
print(allFruits)  // Output: ["apple", "blueberry", "orange", "grape", "melon"]
```

---

### **Conclusion**

Lists in *b2* are flexible and provide a range of functionalities for working with ordered collections of items. From accessing and modifying individual elements to sorting and joining lists, these features make lists powerful tools in data management and manipulation.