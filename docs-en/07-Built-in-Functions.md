---
# 🦅**NISR PROGRAMMING LANGUAGE**
---

# NISR Built-In Functions

These are my personal notes on the built-in functions available in
**NISR**. We wrote them to keep track of how the most common functions
behave, especially for console input/output, checking lengths, and
converting values between different data types.

---

## 1. Console I/O Functions

### 🔹 Print()

The `Print()` function displays values on the screen.

**Syntax**
```nisr
Print(object1, object2, ..., sep=" ", end="\n")
```

Examples

```
Print("Hello World")
Print(1, 2, 3)
Print(1, 2, 3, sep="*")
Print("hello world", end="Nisr5.0")
Print("hello world", end="\n")
```
## 🔹 input()

The `input()` function allows the user to type something into the console.

Examples
```
res = input()
res = input("Can I get your name: ")
```
## 2. Inspection Function
## 🔹 len()

Used to check how many items are inside a list, tuple, dictionary, or string.

Example
```
list1 = [1, 2, 3, 4, [6, 7, 8, 9]]
Print(len(list1))      ; Output: 5
Print(len(list1[4]))   ; Output: 4
```

## 3. Type Conversion Functions

NISR provides built-in functions to convert between data types.

- `int()` – Convert a value to an integer

- `float()` – Convert a value to a floating-point number

- `string()` – Convert a value to a string

- `list()` – Convert a string or tuple to a list

- `tuple()` – Convert a string or list to a tuple

## 🔹 int()

- Converts **values** into **integers**.

Examples

```
Print(int("42"))    ; Output: 42
Print(int(3.99))    ; Output: 3
Print(int(true))    ; Output: 1
```
## 🔹 float()

- Converts **values** into **floating-point numbers**.

Examples

```
Print(float("3.14"))   ; Output: 3.14
Print(float(10))       ; Output: 10.0
Print(float(false))    ; Output: 0.0

```
## 🔹 string()

- Converts **values** into **strings**.

Examples

```
Print(string(42))      ; Output: "42"
Print(string(3.14))    ; Output: "3.14"
Print(string(true))    ; Output: "true"
```
## 🔹 list()

- Converts **strings** or **tuples** into lists.

Examples

```
Print(list("NISR"))    ; Output: ["N", "I", "S", "R"]
Print(list((1, 2, 3))) ; Output: [1, 2, 3]
```
## 🔹 tuple()

Converts **strings** or **lists** into tuples.

Examples
```
Print(tuple([1, 2, 3])) ; Output: (1, 2, 3)
Print(tuple("NISR"))    ; Output: ("N", "I", "S", "R")
```


---


### 📘Learn more : 
- [Getting Started](01-Getting%20Started.md)
- [Basic Syntax](02-Basic%20Syntax.md)
- [Expressions and Operators](03-Expressions%20and%20Operators.md)
- [List, Tuple and Dictionary](04-List,%20Tuple%20and%20Dictionary.md)
- [String Manipulation](05-String%20Manipulation.md)
- [Control Flow and Error Handling](06-Control%20Flow%20and%20Error%20Handling.md)
- [Built-in-Functions](07-Built-in-Functions.md)
- [Functions](08-Functions.md)
- [Libraries and Modules](09-Libraries%20and%20Modules.md)
- [Obect Oriented Programming](10-Object%20Oriented%20Programming.md)
- [Language Configuration](11-Language%20Configuration.md)

---
