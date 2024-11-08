
# 🌟 ft_printf - 42 Project 🌟

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Language](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))

## 📝 Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Requirements](#requirements)
- [Design Suggestions](#design-suggestions)
- [Code Structure](#code-structure)
- [Installation](#installation)
- [How to Use](#how-to-use)
- [Examples](#examples)

---

## 🎯 About the Project

`ft_printf` is a simplified, custom implementation of the C standard library function `printf`. Created as part of the 42 School curriculum, this project aims to deepen understanding of variadic functions, memory management, and string manipulation in C. It was developed without using standard library functions for formatted output, ensuring all formatting and printing logic is custom-made.

## ✨ Features

- **Supports Multiple Specifiers:** Handles `%c`, `%s`, `%p`, `%d`, `%i`, `%u`, `%x`, `%X`, and `%%`.
- **Memory Safety:** Designed to avoid memory leaks and ensure stable behavior.
- **Modular Design:** Organized functions for readability and easy debugging.
- **Custom Conversion Functions:** Implements custom functions to handle formatting and printing with precision.

## ✅ Requirements

The main requirements for the ft_printf project typically include:

- Implement the following conversion specifiers: c, s, p, d, i, u, x, X, %.
- Handle flag characters: -, +, #, 0, and ' ' (space).
- Handle minimum field width.
- Handle precision.
- Handle the % conversion specifier.
- Return the number of characters printed (excluding the null byte used to end output to strings).
- Use a custom buffer management system to improve performance.
- Implement the project in C, following the guidelines and standards set by the 42 coding school.

## 💡 Design Suggestions

When approaching this project, consider the following design suggestions:

- Modular Structure: Break down the project into smaller, reusable functions that handle specific tasks, such as parsing format specifiers, converting data types, and managing the output buffer.
- Error Handling: Implement robust error handling to gracefully handle invalid input or unsupported features.
- Performance Optimization: Focus on efficient buffer management and minimizing unnecessary string operations to improve the overall performance of your ft_printf implementation.
- Readability and Maintainability: Write clean, well-documented code that is easy to understand and modify in the future.
- Test Coverage: Thoroughly test your implementation to ensure it meets all the requirements and handles edge cases correctly.

## 📂 Code Structure

| File                       | Description                                           |
|----------------------------|-------------------------------------------------------|
| `ft_printf.c`              | Main function handling variadic arguments and parsing |
| `ft_cas.c`                 | Helper functions for format parsing                   |
| `ft_putchar.c, ft_putstr.c`| Functions to print characters and strings             |
| `ft_putnbr.c`              | Functions to print integers, hexadecimals, etc.       |
| `ft_hexanbr.c`             | Functions to print hexadecimal numbers                |
| `Makefile`                 | Automated build script                                |

## 📥 Installation

To install and use `ft_printf` in your project, follow these steps:

```
git clone https://github.com/HoudaChairi/ft_printf.git
```
```
cd ft_printf
```
```
make
```

If you want to clean up object files after compiling, use ```make clean```.

To remove all generated files, including the library, use make ```fclean```.

## ⚙️ How to Use

You can use `ft_printf` just like the standard `printf` function:

```c
#include "ft_printf.h"

int main() {
    int result = ft_printf("Hello, %s! You have %d new messages.\n", "user", 42);
    return result;
}
```

## 📌 Examples

Here's how `ft_printf` behaves with different format specifiers:
```
ft_printf("Character: %c\n", 'A');             // Character: A
ft_printf("String: %s\n", "42 Network");       // String: 42 Network
ft_printf("Pointer: %p\n", (void *)&num);      // Pointer: 0x7ffeedcb
ft_printf("Integer: %d\n", 42);                // Integer: 42
ft_printf("Unsigned: %u\n", 3000000000);       // Unsigned: 3000000000
ft_printf("Hex (lower): %x\n", 255);           // Hex (lower): ff
ft_printf("Hex (upper): %X\n", 255);           // Hex (upper): FF
ft_printf("Percentage: %%\n");                 // Percentage: %
```
