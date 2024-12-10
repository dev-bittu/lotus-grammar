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
- `grammar/` - Directory containing detailed Lotus grammar definitions.

## Contributing
We welcome contributions to enhance Lotus's grammar! Here’s how you can help:
1. **Fork the Repository**
2. **Create a Branch** for your feature or bug fix.
3. **Commit Your Changes** with descriptive messages.
4. **Open a Pull Request** to merge your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
