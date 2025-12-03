
# NISR Built-In Functions

These are my personal notes on the built-in functions available in
**NISR**. I wrote them to keep track of how the most common functions
behave, especially for console input/output, checking lengths, and
converting values between different data types.

## 1. Console I/O Functions

### Print()

The `Print()` function is what I use to display values on the screen.

**Syntax:**

    Print(object1, object2, ..., sep=" ", end="\n")

**Examples:**

    Print("Hello World")
    Print(1, 2, 3)
    Print(1, 2, 3, sep="*")
    Print("hello world", end="Nisr5.0")
    Print("hello world", end="\n")

### input()

The `input()` function allows the user to type something into the
console.

**Examples:**

    res = input()
    res = input("Can I get your name: ")

## 2. Inspection Function

### len()

Used to check how many items are inside a list, tuple, dictionary, or
string.

**Example:**

    list1 = [1, 2, 3, 4, [6, 7, 8, 9]]
    Print(len(list1), len(list1[4]))

## 3. Type Conversion Functions

NISR includes the following conversion functions:

-   int()
-   float()
-   string()
-   list()
-   tuple()

### int()

Converts values into integers.

### float()

Converts values into floats.

### string()

Converts values into strings.

### list()

Turns tuples or strings into lists.

### tuple()

Turns lists or strings into tuples.

