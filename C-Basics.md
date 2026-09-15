# C-Basics

## 1. Data Types

| Data Type | Description |
|-----------|-------------|
| `int` | Stores whole numbers (no decimal point), typically 4 bytes, e.g. 10, -25 |
| `float` | Stores single-precision floating-point (decimal) numbers, typically 4 bytes |
| `double` | Stores double-precision floating-point numbers, typically 8 bytes, more accurate than float |
| `char` | Stores a single character, e.g. 'A', '9', '$', typically 1 byte |
| `bool` | Stores a logical value: true or false (requires `#include <stdbool.h>` in C) |
| `void` | Represents "no value" or "no type" — used for functions that return nothing, or generic pointers |

## 2. Format Specifiers

| Specifier | Meaning |
|-----------|---------|
| `%d` | Signed decimal integer |
| `%u` | Unsigned decimal integer |
| `%o` | Unsigned octal (base 8) integer |
| `%x` | Unsigned hexadecimal integer (lowercase letters, e.g. a-f) |
| `%X` | Unsigned hexadecimal integer (uppercase letters, e.g. A-F) |
| `%f` | Floating-point number (decimal notation) |
| `%e` | Floating-point number in scientific/exponential notation |
| `%c` | Single character |
| `%s` | String (sequence of characters) |
| `%ld` | Long signed decimal integer |

## 3. Input/Output Functions

**scanf()**
Reads formatted input from the keyboard and stores it into variables using format specifiers. Example: `scanf("%d", &age);` reads an integer typed by the user and stores it in the variable `age`.

**printf()**
Prints formatted output to the screen using format specifiers. Example: `printf("Age: %d", age);` displays the value of `age` on the screen.

**getchar()**
Reads a single character from the keyboard input (including whitespace and newline characters) and returns it. Example: `char c = getchar();`

**putchar()**
Prints a single character to the screen. Example: `putchar(c);` displays the character stored in `c`.

**fgets()**
Reads a full line of text (including spaces) from input, up to a specified number of characters or until a newline is found. Safer than `gets()` because it limits how much it reads. Example: `fgets(name, 50, stdin);`

**puts()**
Prints a string to the screen and automatically adds a newline at the end. Example: `puts("Hello, world!");`

## 4. Escape Sequences

| Escape Sequence | Meaning | Example |
|------------------|---------|---------|
| `\n` | New line | `printf("Hi\n");` moves to the next line after printing "Hi" |
| `\t` | Horizontal tab | `printf("A\tB");` prints A, then a tab space, then B |
| `\\` | Backslash character | `printf("C:\\Users");` prints `C:\Users` |
| `\"` | Double quote character | `printf("She said \"hello\"");` prints `She said "hello"` |
| `\'` | Single quote character | `printf("It\'s mine");` prints `It's mine` |
| `\0` | Null character (marks end of a string) | Used internally to terminate strings in C |

## 5. Precision

Precision for floating-point output is specified by adding a period (`.`) followed by a number between the `%` sign and the format specifier (`f` or `e`). This number tells `printf()` how many digits to display after the decimal point.

For example:
- `printf("%.2f", 3.14159);` displays `3.14` (2 digits after the decimal point)
- `printf("%.4f", 3.14159);` displays `3.1416` (4 digits, rounded)
- `printf("%.0f", 3.14159);` displays `3` (no decimal digits at all)

If no precision is specified, `printf()` defaults to 6 digits after the decimal point.
