### **Sets in *lotus***

A **set** in *lotus* is a collection that is **unordered**, **unchangeable**, and does not allow duplicate values. Sets are used when you need to store unique items and don't require them to maintain order.

---

### **Key Features of Sets**
1. **Unordered**: Items in a set do not have a defined order. 
   - This means their position can change, and you cannot access them using indices.
2. **Unchangeable**: Once created, the items within a set cannot be changed. However, you can add new items or remove existing ones.
3. **No Duplicates**: Sets do not allow duplicate values. If duplicates are included during set creation, they are ignored.

---

### **Creating a Set**

Sets are defined using curly brackets `{}` or the `set()` constructor. They can hold any data type, and by default, they use the generic template `any`. You can also explicitly specify a data type for the set.

```lotus
// Creating a set with mixed types
let myset = {"apple", True, 42}  

// Creating an integer-only set
let intset = set<i32>(1, 2, 3, 4, 4)  // Duplicates will be ignored

// Using the set constructor
let newset = set("apple", "banana", "cherry")
```

---

### **Set Properties**

#### **1. Unordered**
The items in a set are not stored in any particular order, and this order can change each time the set is accessed.

```lotus
let myset = {"apple", "banana", "cherry"}
print(myset)  // Output order may vary: set("banana", "cherry", "apple")
```

#### **2. Unchangeable**
Individual items in a set cannot be updated after creation. You can add or remove items but not modify existing ones.

```lotus
myset := {"apple", "banana", "cherry"}
myset[1] = "grape"  // Error: Cannot modify items in a set
```

#### **3. No Duplicates**
Sets automatically remove duplicate values.

```lotus
let myset = {"apple", "banana", "apple"}
print(myset)  // Output: set("apple", "banana")
```

---

### **Common Set Operations**

#### **Get the Length of a Set**
Use `len()` to find the number of items in a set.

```lotus
let myset = {"apple", "banana", "cherry"}
print(myset.len())  // Output: 3
```

#### **Add Items to a Set**
Add new elements using `add()`.

```lotus
let myset = {"apple", "banana"}
myset.add("cherry")
print(myset)  // Output: set("apple", "banana", "cherry")
```

#### **Remove Items from a Set**
Use `remove()` to delete an item.

```lotus
let myset = {"apple", "banana", "cherry"}
myset.remove("banana")
print(myset)  // Output: set("apple", "cherry")
```

#### **Check for Membership**
Use the `in` keyword to check if an item exists in a set.

```lotus
let myset = {"apple", "banana"}
print("apple" in myset)  // Output: True
print("grape" in myset)  // Output: False
```

#### **Set Union**
Combine two sets using the `union()` method or `|` operator.

```lotus
let set1 = {"apple", "banana"}
let set2 = {"cherry", "apple"}
let union_set = set1.union(set2)
print(union_set)  // Output: set("apple", "banana", "cherry")
```

#### **Set Intersection**
Find common elements using the `intersection()` method or `&` operator.

```lotus
let set1 = {"apple", "banana"}
let set2 = {"banana", "cherry"}
let intersect = set1.intersection(set2)
print(intersect)  // Output: set("banana")
```

#### **Set Difference**
Find items in one set but not the other using the `difference()` method or `-` operator.

```lotus
let set1 = {"apple", "banana"}
let set2 = {"banana", "cherry"}
let diff = set1.difference(set2)
print(diff)  // Output: set("apple")
```

#### **Set Symmetric Difference**
Find items that are in either of the sets but not both using `symmetric_difference()` or `^` operator.

```lotus
let set1 = {"apple", "banana"}
let set2 = {"banana", "cherry"}
let sym_diff = set1.symmetric_difference(set2)
print(sym_diff)  // Output: set("apple", "cherry")
```

---

### **Looping Through a Set**

Use a `for` loop to iterate over the items in a set.

```lotus
let myset = {"apple", "banana", "cherry"}

for item in myset {
    print(item)
}
```

---

### **Joining Sets**

You can join two sets using `union()` or `update()`. The `update()` method adds the items from one set to another, modifying the first set in place.

```lotus
let set1 = {"apple", "banana"}
let set2 = {"cherry", "date"}

set1.update(set2)
print(set1)  // Output: set("apple", "banana", "cherry", "date")
```

---

### **Set Methods**

| **Method**              | **Description**                                                                 |
|--------------------------|---------------------------------------------------------------------------------|
| `add(value)`             | Adds a new element to the set.                                                  |
| `remove(value)`          | Removes the specified value. Throws an error if the value is not found.         |
| `discard(value)`         | Removes the specified value. Does not throw an error if the value is not found. |
| `union(other_set)`       | Returns a new set containing all unique elements from both sets.                |
| `intersection(other_set)`| Returns a new set with only the common elements of both sets.                   |
| `difference(other_set)`  | Returns a set containing items in the first set but not in the second set.       |
| `clear()`                | Removes all items from the set.                                                 |
| `len()`                  | Returns the number of elements in the set.                                      |

---

### **Set vs Other Collections**

| **Feature**         | **Set**                           | **List**                 | **Tuple**              | **Array**              |
|----------------------|-----------------------------------|--------------------------|------------------------|------------------------|
| **Ordered**          | No                               | Yes                      | Yes                    | Yes                    |
| **Changeable**       | No (items are immutable)         | Yes                      | No                     | Yes                    |
| **Allows Duplicates**| No                               | Yes                      | Yes                    | Yes                    |
| **Indexing**         | No                               | Yes                      | Yes                    | Yes                    |

Sets are best used when you need unique values and don't care about their order.