# ft_printf

A custom implementation of the printf function in C, created as part of the curriculum at 42 School. This project demonstrates core concepts of variadic functions, string formatting, and memory management while replicating the behavior of the standard printf function.

---

## Features

### Supported Conversions
- %c: Print a single character.
- %s: Print a string (handles NULL as "(null)").
- %p: Print a pointer address in hexadecimal (e.g., 0x1a2b3c).
- %d / %i: Print signed integers in base 10.
- %u: Print unsigned integers in base 10.
- %x / %X: Print numbers in lowercase/uppercase hexadecimal (base 16).
- %%: Print a literal % character.

### Edge Cases Handled
- Null Strings: Prints "(null)" for %s if the string is NULL.
- Zero Pointers: Prints "(nil)" for %p if the pointer is 0.
- Memory Safety: All allocated memory is properly freed.

---

## Installation

1. Clone the Repository:
   git clone git@github.com:mapleinred/42-ft_printf.git
   cd 42-ft_printf

2. Compile the Library:
   Run "make" to build the static library libftprintf.a:
   make

3. Use in Your Project:
   Include the header ft_printf.h in your code and link the library during compilation:
   gcc your_program.c -L. -lftprintf -o your_program

---

## Usage

Call ft_printf exactly like the standard printf:
#include "ft_printf.h"

int main() {
    ft_printf("Hello, %s! %d in hex is %x.\n", "world", 42, 42);
    return 0;
}

Output:
Hello, world! 42 in hex is 2a.

---

## Learning Outcomes

- Variadic Functions: Mastery of va_list, va_arg, and va_end to handle variable arguments.
- Memory Management: Safe use of malloc and free to avoid leaks.
- Recursion: Implemented in hexadecimal conversion for pointers and integers.
- Low-Level I/O: Direct use of write for output.
- Code Organization: Modular design with helper functions for each conversion.

---

## Purpose

This project was developed to:
- Deepen understanding of the printf function’s internal mechanics.
- Practice writing structured, extensible, and norm-compliant code (per 42 School’s guidelines).
- Prepare for future C projects by creating a reusable library.

---

## How This Helps in Job Search

- Proficiency in C: Demonstrates strong grasp of core C concepts, including pointers, memory, and system calls.
- Problem-Solving: Shows ability to reverse-engineer and replicate complex functionality.
- Attention to Detail: Handles edge cases and adheres to strict coding standards.
- Code Quality: Highlights clean, modular, and documented code—key traits for collaborative work.

---

## Notes

- Bonus Features: This implementation covers the mandatory requirements. Flags like #, +, and width specifiers are not included.
- Testing: Thoroughly tested against printf for consistency. Contributions to test coverage are welcome.