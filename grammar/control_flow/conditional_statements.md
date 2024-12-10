### `if`, `else`, and `elif` in **lotus**

In **lotus**, the `if`, `else`, and `elif` statements are used to make decisions based on conditions. The blocks of code are enclosed in curly braces `{}` to define their scope, and conditions are followed by the block of code inside curly braces.

### `if` Statement

The `if` statement checks whether a condition is `true`. If it is, the code inside the curly braces is executed.

#### Syntax:
```lotus
if condition {
    // Code to execute if the condition is true
}
```

#### Example:
```lotus
age := 18
if age >= 18 {
    print("You are an adult.")
}
```

**Output:**  
`You are an adult.`

### `else` Statement

The `else` statement provides an alternative block of code that is executed if the `if` condition is `false`. The `else` block must come after the `if` block.

#### Syntax:
```lotus
if condition {
    // Code to execute if the condition is true
} else {
    // Code to execute if the condition is false
}
```

#### Example:
```lotus
age := 16
if age >= 18 {
    print("You are an adult.")
} else {
    print("You are a minor.")
}
```

**Output:**  
`You are a minor.`

### `elif` Statement

The `elif` (short for "else if") statement checks multiple conditions. If the first `if` condition is `false`, the program moves on to the `elif` condition, and so on. The first `true` condition will execute its associated block. If none of the conditions are `true`, the `else` block will execute.

#### Syntax:
```lotus
if condition1 {
    // Code to execute if condition1 is true
} elif condition2 {
    // Code to execute if condition1 is false and condition2 is true
} else {
    // Code to execute if none of the above conditions are true
}
```

#### Example:
```lotus
age := 25
if age < 13 {
    print("You are a child.")
} elif age >= 13 and age <= 19 {
    print("You are a teenager.")
} else {
    print("You are an adult.")
}
```

**Output:**  
`You are an adult.`

### Combining `if`, `elif`, and `else`

You can combine `if`, `elif`, and `else` to handle more complex decision-making scenarios.

#### Example:
```lotus
temperature := 30
if temperature < 10 {
    print("It's cold.")
} elif temperature >= 10 and temperature < 20 {
    print("It's mild.")
} elif temperature >= 20 and temperature < 30 {
    print("It's warm.")
} else {
    print("It's hot.")
}
```

**Output:**  
`It's warm.`

### Nested `if` Statements

You can nest `if` statements inside other `if` statements to create more complex logic.

#### Example:
```lotus
age := 25
has_id := true
if age >= 18 {
    if has_id {
        print("You can enter the club.")
    } else {
        print("You need an ID to enter.")
    }
} else {
    print("You are too young to enter the club.")
}
```

**Output:**  
`You can enter the club.`

### Summary
- The `if` statement executes a block of code if the condition is `true`.
- The `else` statement provides an alternative block of code that is executed if the `if` condition is `false`.
- The `elif` statement is used to check multiple conditions. It allows for multiple branches, where only the first `true` condition will be executed.
- The blocks of code are enclosed in curly braces `{}` to define the scope of the condition and the actions.
- Logical operators like `and`, `or`, and `not` can be used in conditions to combine multiple expressions.

This is the correct **lotus** syntax for conditional statements!