# Lotus Grammar
This repository defines the grammar for **Lotus**, a compiled programming language designed to combine the best features of various languages. Lotus aims to provide:

- Simple syntax similar to Python, making it easy to write and read.
- Performance optimized like C/C++ for speed and efficiency.
- Static typing like Go, providing safety and performance benefits at compile-time.
- A robust compiler experience like Rust, ensuring great optimization and error detection.

Lotus compiles to an intermediate form (similar to Java class files) that runs on the **Lotus Virtual Machine (MVM)**. This approach offers:

- **Garbage Collection** for memory management.
- **Dynamic-to-Static Type Conversion** to improve performance and ensure type safety.
- **Cross-Platform Support**, enabling Lotus applications to run on various platforms.
- **Improved Compilation Time** thanks to the optimized intermediate representation.

## Overview
Lotus is designed with both beginner users and advanced developers in mind. It is an experimental language that emphasizes simplicity, ease of use, and performance. The grammar definitions in this repository serve as the foundation for Lotus, allowing future development of parsers, compilers, and interpreters.

### Features
- **Simple Syntax**: Lotus is designed to be easy to write and read, inspired by languages like Python but with the power of compiled languages.
- **Faster Performance**: Offers C/C++-like performance, thanks to a compiled execution model.
- **Static Typing**: Static types are enforced at compile-time for reliability and speed, similar to Go.
- **Good Compiler**: Lotus features a compiler designed for error detection, optimization, and performance improvements, inspired by Rust's tooling.


## File Structure
- [LEARN_IN_5_MIN.md](LEARN_IN_5_MIN.md) - Learn lotus lang in 5 min

## Learn in 5 minutes
```lotus
// Single-line comments start with double forward-slashes

"""
This can also work as a multiline comment.
Or for unparsable, broken code
"""

# Variables
let (
    letter char = 'n'            # Declare with type annotation
    lang = "N" + "im"            # Concatenation
    nLength int = lang.length()  # Method for length
    boat float                   # Declare without assignment
    truth bool = false           # Boolean
)

# Immutable variables
const (
    legs int = 400             # Constants are immutable
    arms int = 2_000           # Use underscores for readability
    aboutPi float = 3.15
)

# Conditional Compilation
when compileBadCode {
    const debug bool = true
    const input = stdin.readLine() # Compile-time if
}

# Data Structures

# Tuples
let child (str, int) = ("Rudiger", 2)
let today (str, float) = ("Sunny", 25.3)

# Sequences
let drinks = ["Water", "Juice", "Chocolate"]
drinks.add("Milk")

if "Milk" in drinks {
    print("We have Milk and ", drinks.length - 1, " other drinks")
}

let myDrink = drinks[2]

# class
class Person {
    let name str
    let salary i32

    fn __init__(name: str, salary: i32) {
        this.name = name
        this.salary = salary
    }
}

# Enumerations
enum Color { 
    Red,
    Blue,
    Green 
}
enum Direction { 
    North,
    West,
    East,
    South 
}

let orient Direction = Direction.North
let pixel Color = Color.Green

# Iteration
for i, elem in ["Yes", "No", "Maybe so"] {
    print(elem, " is at index: ", i)
}

for k, v in [("You", 100), ("Me", 9000)] {
    print(v)
}

let myString = """
an <example>
`string` to
play with
"""

for line in myString.split("\n") {
    print(line)
}

# Procedures
enum Answer { 
    Yes, 
    No 
}

fn ask(question str) Answer {
    print(question, " (y/n)")
    while true {
        let response = stdin.readLine()
        if response in ["y", "Y", "yes", "Yes"] {
            return Answer.Yes
        } else if response in ["n", "N", "no", "No"] {
            return Answer.No
        } else {
            print("Please be clear: yes or no")
        }
    }
}

fn addSugar(amount int = 2) {
    assert(amount > 0 and amount < 9000, "Crazy Sugar")
    for a in 1..amount {
        print(a, " sugar...")
    }
}

match ask("Would you like sugar in your tea?") {
    case Answer.Yes:
        addSugar(3)
    case Answer.No:
        print("Oh do take a little!")
        addSugar()
}
```

## Contributing
We welcome contributions to enhance Lotus's grammar! Here’s how you can help:
1. **Fork the Repository**
2. **Create a Branch** for your feature or bug fix.
3. **Commit Your Changes** with descriptive messages.
4. **Open a Pull Request** to merge your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
