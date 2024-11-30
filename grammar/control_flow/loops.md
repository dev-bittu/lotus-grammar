### `while` Loop in **b2**

The `while` loop is used to execute a block of code as long as the condition is `true`. The condition is evaluated before each iteration, and if it's `true`, the code inside the loop is executed. Once the condition becomes `false`, the loop stops.

In **b2**, loops are defined using curly braces `{}` to enclose the block of code that should be repeated.

### Basic Syntax

```b2
while condition {
    // Code to execute as long as the condition is true
}
```

### Key Points:
- The condition is evaluated before every iteration of the loop.
- If the condition is `true`, the loop executes the code inside the block.
- The loop continues running until the condition becomes `false`.
- It is important to ensure that the condition eventually becomes `false` to avoid creating an infinite loop.

### Example: Basic `while` Loop

```b2
count := 0
while count < 5 {
    print(count)
    count = count + 1
    // OR count++
    // OR count += 1
}
```

**Output:**
```
0
1
2
3
4
```

### Explanation:
- Initially, `count` is set to 0.
- The condition `count < 5` is checked. Since it's `true`, the code inside the loop is executed.
- The value of `count` is printed, and then incremented by 1.
- This process repeats until `count` is no longer less than 5.

### Infinite Loop

If the condition in a `while` loop never becomes `false`, the loop will continue forever, creating an **infinite loop**.

#### Example of Infinite Loop (Dangerous!):

```b2
while true {
    print("This loop will never stop!")
}
```

**Note:** This kind of loop should be avoided unless there is a way to break out of the loop (such as using `break`).

### `break` Statement

The `break` statement is used to exit the `while` loop before the condition becomes `false`. It allows you to stop the loop when a certain condition is met.

#### Example with `break`:

```b2
count := 0
while count < 10 {
    if count == 5 {
        break // Exits the loop when count is 5
    }
    print(count)
    count := count + 1
}
```

**Output:**
```
0
1
2
3
4
```

### `continue` Statement

The `continue` statement is used to skip the rest of the code inside the loop for the current iteration and proceed to the next iteration of the loop.

#### Example with `continue`:

```b2
count := 0
while count < 5 {
    count = count + 1
    if count == 3 {
        continue // Skips the printing of count when it is 3
    }
    print(count)
}
```

**Output:**
```
1
2
4
5
```

In this example, when `count` reaches 3, the `continue` statement is executed, which causes the loop to skip the `print(count)` statement and proceed to the next iteration.

---

### `for` Loop in **b2**

The `for` loop in **b2** is used to iterate over a sequence (like a list, tuple, string, or dictionary) and execute a block of code for each item in the sequence. The loop automatically iterates through each element in the sequence, making it ideal for looping over collections.

The `for` loop is defined using curly braces `{}` and follows a specific syntax to iterate through elements in a sequence.

### Basic Syntax

```b2
for item in sequence {
    // Code to execute for each item
}
```

### Key Points:
- **item**: The variable that holds the current element from the sequence in each iteration.
- **sequence**: The collection (like a list, tuple, set, or string) that you want to loop through.
- The loop continues until it has iterated through all items in the sequence.
- Unlike the `while` loop, the `for` loop does not require an explicit condition check; it automatically loops through the collection.

### Example 1: Basic `for` Loop (Iterating through a List)

```b2
fruits := ["apple", "banana", "cherry"]
for fruit in fruits {
    print(fruit)
}
```

**Output:**
```
apple
banana
cherry
```

### Explanation:
- The `for` loop iterates through each item in the `fruits` list.
- In each iteration, the variable `fruit` takes the value of the current item in the list, and `print(fruit)` displays it.

### Example 2: `for` Loop with a Range (Iteration over a Range of Numbers)

In **b2**, you can use a `range` to create a sequence of numbers, which is useful for looping a specific number of times.

```b2
for i in range(5) {
    print(i)
}
```

**Output:**
```
0
1
2
3
4
```

### Explanation:
- The `range(5)` generates a sequence of numbers from 0 to 4, and the loop prints each number in the sequence.

### Example 3: Iterating over a Dictionary

Dictionaries contain key-value pairs, and you can loop through both the keys and values using a `for` loop.

```b2
person := {
    "name": "John",
    "age": 36,
    "city": "New York"
}
for key, value in person {
    print(key, value)
}
```

**Output:**
```
name John
age 36
city New York
```

### Explanation:
- In each iteration, `key` gets the key of the current item, and `value` gets the corresponding value.
- The `for` loop iterates through each key-value pair in the `person` dictionary.

### Example 4: `for` Loop with Multiple Variables (Unpacking)

If the sequence is an iterable with multiple elements (such as a list of tuples), you can use unpacking to assign multiple variables during each iteration.

```b2
pairs := [(1, "apple"), (2, "banana"), (3, "cherry")]
for num, fruit in pairs {
    print(num, fruit)
}
```

**Output:**
```
1 apple
2 banana
3 cherry
```

### Explanation:
- The list `pairs` contains tuples. The `for` loop unpacks each tuple into `num` and `fruit` variables, allowing you to access both the number and the fruit in each iteration.

### Example 5: `for` Loop with an Index

If you want to access both the index and the item in the sequence, you can use a combination of `range` and the sequence length.

```b2
fruits := ["apple", "banana", "cherry"]
for i in range(len(fruits)) {
    print(i, fruits[i])
}
```

**Output:**
```
0 apple
1 banana
2 cherry
```

### Explanation:
- The `range(len(fruits))` generates a sequence of indices, and `fruits[i]` is used to access the item at each index.

### Example 6: `for` Loop with a Conditional (`if` inside the loop)

You can also use `if` conditions inside a `for` loop to execute specific actions based on certain criteria.

```b2
numbers := [1, 2, 3, 4, 5]
for num in numbers {
    if num % 2 == 0 {
        print(num, "is even")
    }
}
```

**Output:**
```
2 is even
4 is even
```

### Explanation:
- The `for` loop iterates through each number in the list `numbers`.
- The `if` statement checks if the number is even (`num % 2 == 0`), and if true, it prints that the number is even.

### Example 7: Nested `for` Loop

You can also use nested `for` loops, where one `for` loop is inside another.

```b2
rows := 3
columns := 4
for i in range(rows) {
    for j in range(columns) {
        print(i, j)
    }
}
```

**Output:**
```
0 0
0 1
0 2
0 3
1 0
1 1
1 2
1 3
2 0
2 1
2 2
2 3
```

### Explanation:
- The outer loop iterates over the `rows`, and for each iteration of the outer loop, the inner loop iterates over the `columns`, printing the row and column indices.

### `break` and `continue` with `for` Loops

- **`break`**: Exits the loop entirely, skipping further iterations.
- **`continue`**: Skips the current iteration and moves to the next iteration of the loop.

#### Example with `break`:

```b2
numbers := [1, 2, 3, 4, 5]
for num in numbers {
    if num == 3 {
        break  // Exits the loop when num is 3
    }
    print(num)
}
```

**Output:**
```
1
2
```

#### Example with `continue`:

```b2
numbers := [1, 2, 3, 4, 5]
for num in numbers {
    if num == 3 {
        continue  // Skips the current iteration when num is 3
    }
    print(num)
}
```

**Output:**
```
1
2
4
5
```
