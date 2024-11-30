### `switch`/`case` in **b2**

The `switch`/`case` statement in **b2** is a control flow structure used to execute one out of several possible blocks of code, depending on the value of a given expression. It allows you to compare a variable or expression with different cases, making it more efficient than using multiple `if-else` statements when dealing with many possible conditions.

The `switch`/`case` structure is typically used to handle multiple conditions in a concise and readable way.

### Basic Syntax

```b2
switch expression {
    case value1:
        // Code to execute if expression equals value1
    case value2:
        // Code to execute if expression equals value2
    default:
        // Code to execute if expression does not match any case
}
```

### Key Components:
- **expression**: The value or expression you are evaluating. This is compared with each `case`.
- **case value**: Represents the possible values that `expression` might match. If a match is found, the corresponding block of code is executed.
- **default**: An optional block of code that will be executed if no `case` matches the expression.

### Example 1: Basic `switch`/`case`

```b2
day := 3
switch day {
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case 4:
        print("Thursday")
    case 5:
        print("Friday")
    default:
        print("Weekend")
}
```

**Output:**
```
Wednesday
```

### Explanation:
- The `switch` expression evaluates the value of `day` (which is `3` in this case).
- It matches `3` with `case 3`, and executes the corresponding code (`print("Wednesday")`).
- The `default` case will only be executed if no other cases match, but it is not executed here.

### Example 2: `switch`/`case` with String Matching

```b2
fruit := "banana"
switch fruit {
    case "apple":
        print("An apple a day keeps the doctor away.")
    case "banana":
        print("Bananas are rich in potassium.")
    case "orange":
        print("Oranges are high in vitamin C.")
    default:
        print("Unknown fruit.")
}
```

**Output:**
```
Bananas are rich in potassium.
```

### Explanation:
- The `switch` expression evaluates the value of `fruit` (which is `"banana"`).
- It matches `"banana"` with `case "banana"` and executes the corresponding code (`print("Bananas are rich in potassium.")`).
- If `fruit` had been any other value, the `default` case would have been executed.

### Example 3: `switch`/`case` with Multiple Conditions

You can group multiple `case` values together to execute the same block of code for different conditions.

```b2
month := 7
switch month {
    case 1, 2, 3:
        print("First quarter of the year.")
    case 4, 5, 6:
        print("Second quarter of the year.")
    case 7, 8, 9:
        print("Third quarter of the year.")
    case 10, 11, 12:
        print("Fourth quarter of the year.")
    default:
        print("Invalid month.")
}
```

**Output:**
```
Third quarter of the year.
```

### Explanation:
- The `month` variable is set to `7`, and it matches the case `7, 8, 9`, so the code for that block is executed (`print("Third quarter of the year.")`).
- By grouping multiple values in a `case` statement, you can reduce redundancy.

### Example 4: Using `switch`/`case` Without `default`

The `default` case is optional. If you don't need a fallback, you can omit it.

```b2
color := "blue"
switch color {
    case "red":
        print("Color is red")
    case "green":
        print("Color is green")
    case "blue":
        print("Color is blue")
}
```

**Output:**
```
Color is blue
```

### Explanation:
- The `color` variable is `"blue"`, which matches the `case "blue"`, and the corresponding message is printed.
- Since there's no `default` case, no message will be printed if `color` is not red, green, or blue.

### Example 5: `switch`/`case` with Expressions

You can also use expressions in `switch`/`case` to evaluate more complex conditions.

```b2
x := 10
switch x % 2 {
    case 0:
        print("Even number")
    case 1:
        print("Odd number")
}
```

**Output:**
```
Even number
```

### Explanation:
- The expression `x % 2` evaluates to `0` because `x` is `10` (an even number).
- It matches `case 0`, and the code for that block (`print("Even number")`) is executed.


### Case with Fallthrough:

The **`fallthrough`** keyword is used to allow execution to continue into the next case block. Without this keyword, once a matching case is found, the program will stop at that case, and subsequent cases will not be executed.

### Basic Syntax with Fallthrough:

```b2
switch expression {
    case value1:
        // Code to execute if expression equals value1
        fallthrough
    case value2:
        // Code to execute if expression equals value2
    default:
        // Code to execute if expression does not match any case
}
```

### Example 1: Basic Switch with Fallthrough

```b2
day := 3
switch day {
    case 1:
        print("Monday")
        fallthrough
    case 2:
        print("Tuesday")
        fallthrough
    case 3:
        print("Wednesday")
        fallthrough
    case 4:
        print("Thursday")
    default:
        print("Weekend")
}
```

**Output:**
```
Wednesday
Thursday
```

### Explanation:
- The `switch` expression evaluates the value of `day` (which is `3`).
- It matches `3` with `case 3` and executes the corresponding code (`print("Wednesday")`).
- Since **fallthrough** is used, execution continues into `case 4`, and `print("Thursday")` is executed.
- If no **fallthrough** was specified, the program would stop after printing `"Wednesday"`.

---

### Using Switch with enum

Let’s also use an example with a **custom enum-like** structure, which could be useful for more structured case handling.

In **b2**, there isn’t a direct `enum` type, but we can simulate it by using constants or a `struct`. Here’s an example using string constants to mimic enums:

```b2
// Defining day enum
enum day {
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY,
    SUNDAY
}

currentDay := day.WEDNESDAY

switch currentDay {
    case day.MONDAY:
        print("It's Monday, start of the week!")
        fallthrough
    case day.TUESDAY:
        print("It's Tuesday, still early in the week.")
        fallthrough
    case day.WEDNESDAY:
        print("It's Wednesday, we're halfway there!")
        fallthrough
    case day.THURSDAY:
        print("It's Thursday, almost there!")
    default:
        print("Weekend is approaching!")
}
```

**Output:**
```
It's Wednesday, we're halfway there!
It's Thursday, almost there!
```

### Explanation:
- The variable `currentDay` is set to `day.WEDNESDAY`.
- The `switch` matches the `WEDNESDAY` case and executes the corresponding statement.
- The **fallthrough** keyword allows execution to continue into the next case (`THURSDAY`), printing the corresponding message.
- Without **fallthrough**, the program would stop after printing the message for `Wednesday`.

---

### Key Points:
- **`fallthrough`** allows a switch statement to continue to the next case block, even if the current case has been matched.
- This feature is useful when multiple cases should share behavior, or when sequential logic is required in the case blocks.
- In the enum-like example, we used string constants to simulate an enum-like structure, making the `switch` more readable and expressive.
