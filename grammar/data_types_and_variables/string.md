### **String in *mylang***

In *mylang*, strings are sequences of characters and are defined by enclosing text in double quotes (`" "`). Strings are commonly used to represent textual data and can be manipulated in various ways.

#### **Creating a String**
A string is created by simply assigning a sequence of characters enclosed in double quotes to a variable:

```mylang
let myString str = "Hello, World!"
```

---

### **String Operations in *mylang***

#### **1. String Slicing**
String slicing allows you to extract a substring from a given string using indices.

- **Slice From the Start**  
  By omitting the start index, the slice will start from the first character:
  
  ```mylang
  let b str = "Hello, World!"
  print(b[:5])  // Output: "Hello"
  ```

- **Slice To the End**  
  By omitting the end index, the slice will continue to the end of the string:
  
  ```mylang
  let b str = "Hello, World!"
  print(b[2:])  // Output: "llo, World!"
  ```

- **Negative Indexing**  
  Negative indices count from the end of the string. `-1` represents the last character, `-2` the second-to-last character, and so on.
  
  ```mylang
  let b str = "Hello, World!"
  print(b[-5:-2])  // Output: "orl"
  ```

---

#### **2. String Modifying**
Strings in *mylang* are immutable, meaning you cannot directly change individual characters. However, you can create new strings based on modifications.

- **Changing Part of a String**  
  You can modify a string by slicing it and combining it with new content:
  
  ```mylang
  let b str = "Hello, World!"
  let modified str = b[:7] + "Universe!"
  print(modified)  // Output: "Hello, Universe!"
  ```

---

#### **3. String Concatenation**
You can join two or more strings using the `+` operator:

```mylang
let greeting str = "Hello"
let name str = "Alice"
let message str = greeting + " " + name
print(message)  // Output: "Hello Alice"
```

You can also concatenate multiple strings:

```mylang
let part1 str = "Hello"
let part2 str = " "
let part3 str = "World!"
let fullMessage str = part1 + part2 + part3
print(fullMessage)  // Output: "Hello World!"
```

---

#### **4. String Formatting**
String formatting allows you to embed variables inside strings.

- **Using `+` for Formatting:**
  
  ```mylang
  let name str = "Alice"
  let age i64 = 30
  let formatted str = "Name: " + name + ", Age: " + str(age)
  print(formatted)  // Output: "Name: Alice, Age: 30"
  ```

- **Using Template Strings (if supported):**
  (In *mylang*, template strings allow embedding variables directly in the string.)

  ```mylang
  let name str = "Alice"
  let age i64 = 30
  let formatted str = `Name: ${name}, Age: ${age}`
  print(formatted)  // Output: "Name: Alice, Age: 30"
  ```

---

#### **5. Escape Characters**
Escape characters allow special characters to be included in a string without causing errors.

- **Newline**: `\n`  
  Adds a newline at that point in the string.
  
  ```mylang
  let text str = "Hello\nWorld!"
  print(text)  // Output:
  // Hello
  // World!
  ```

- **Tab**: `\t`  
  Adds a tab space in the string.
  
  ```mylang
  let text str = "Name:\tAlice"
  print(text)  // Output: "Name:    Alice"
  ```

- **Backslash**: `\\`  
  To print a backslash, escape it using another backslash.
  
  ```mylang
  let text str = "This is a backslash: \\"
  print(text)  // Output: "This is a backslash: \"
  ```

- **Quotation Marks**: `\"` or `\'`  
  Used for escaping double quotes `"` or single quotes `'` inside strings.
  
  ```mylang
  let text str = "He said, \"Hello!\""
  print(text)  // Output: He said, "Hello!"
  ```

---

#### **6. String Methods**
*mylang* provides several built-in methods for string manipulation:

- **Length of String** (`len()`): Returns the length of the string.

  ```mylang
  let myStr str = "Hello, World!"
  let length i64 = len(myStr)
  print(length)  // Output: 13
  ```

- **Lowercase** (`lower()`): Converts all characters in the string to lowercase.

  ```mylang
  let myStr str = "Hello, World!"
  let lowerCase str = myStr.lower()
  print(lowerCase)  // Output: "hello, world!"
  ```

- **Uppercase** (`upper()`): Converts all characters in the string to uppercase.

  ```mylang
  let myStr str = "Hello, World!"
  let upperCase str = myStr.upper()
  print(upperCase)  // Output: "HELLO, WORLD!"
  ```

- **Replace Substring** (`replace(old, new)`): Replaces occurrences of a substring with another string.

  ```mylang
  let myStr str = "Hello, World!"
  let newStr str = myStr.replace("World", "Alice")
  print(newStr)  // Output: "Hello, Alice!"
  ```

- **Find Substring** (`find()`): Finds the index of the first occurrence of a substring.

  ```mylang
  let myStr str = "Hello, World!"
  let index i64 = myStr.find("World")
  print(index)  // Output: 7 (index of 'World' in "Hello, World!")
  ```

- **Split String** (`split(delim)`): Splits a string into a list of substrings based on a delimiter.

  ```mylang
  let myStr str = "apple,banana,cherry"
  let fruits list = myStr.split(",")
  print(fruits)  // Output: ["apple", "banana", "cherry"]
  ```

---

Got it! I'll only include a table when it enhances the clarity or usefulness of the information. Here's the updated version with tables for escape sequences and string methods to make them more accessible.

---

### **Escape Sequences in *mylang***

Escape sequences allow you to insert special characters into strings that would otherwise be difficult to represent. Below is a list of commonly used escape sequences:

| Escape Sequence | Description                        | Example Output         |
|-----------------|------------------------------------|------------------------|
| `\n`            | Newline (line break)               | `Hello\nWorld!` → "Hello\nWorld!" |
| `\t`            | Horizontal tab                     | `Name:\tAlice` → "Name:    Alice" |
| `\\`            | Backslash                          | `This is a backslash: \\` → "This is a backslash: \" |
| `\"`            | Double quote                       | `He said, \"Hello!\"` → "He said, \"Hello!\"" |
| `\'`            | Single quote                       | `It\'s easy` → "It's easy" |

Escape sequences are helpful for formatting strings with special characters, ensuring they are correctly displayed in output.

---

### **String Methods in *mylang***

String methods provide various functions to manipulate or query strings. Here are some of the most useful string methods available in *mylang*:

| Method           | Description                                          | Example Output              |
|------------------|------------------------------------------------------|-----------------------------|
| `len()`          | Returns the length of the string.                    | `"Hello".len()` → 5         |
| `lower()`        | Converts all characters in the string to lowercase.  | `"Hello".lower()` → "hello" |
| `upper()`        | Converts all characters in the string to uppercase.  | `"Hello".upper()` → "HELLO" |
| `replace()`      | Replaces all occurrences of a substring with another string. | `"Hello, World!".replace("World", "Alice")` → "Hello, Alice!" |
| `find()`         | Returns the index of the first occurrence of a substring. | `"Hello, World!".find("World")` → 7 |
| `split()`        | Splits the string into a list based on a delimiter.  | `"apple,banana,cherry".split(",")` → `["apple", "banana", "cherry"]` |

Strings in *mylang* are versatile and provide various functions to help with string manipulation. Whether you need to slice, modify, concatenate, or format strings, *mylang* provides an easy-to-use syntax.