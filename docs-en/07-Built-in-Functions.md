<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

<p align="center">
  <img alt="Typing" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=700&color=FFC72C&center=true&vCenter=true&width=650&lines=Designed+for+Everyone%2C+Built+for+the+Future;Where+Beginners+Start+and+Developers+Grow;A+Simple+Language+for+Big+Ideas;Write+Less%2C+Create+More+%E2%80%94+With+NISR+PL;Powerful+for+Experts%2C+Friendly+for+Beginners;Code+in+Your+Language+%E2%80%94+NISR+Speaks+Many;Multilingual+Language+for+Global+Developers;Learning+to+Code+Has+Never+Been+This+Simple;From+Zero+to+Pro+%E2%80%94+The+NISR+Way;Teach%2C+Learn%2C+Build+%E2%80%94+All+with+NISR+PL" />
</p>


<p align="center">
  <a href="https://Github.com/Nisr-programming-language/Nisr_PL">
    <img src="https://img.shields.io/badge/Try%20NISR-Online-green?style=for-the-badge" />
  </a>
</p>

---

# NISR Built-In Functions

These are my personal notes on the built-in functions available in
**NISR**. We wrote them to keep track of how the most common functions
behave, especially for console input/output, checking lengths, and
converting values between different data types.

---

## 1. Console I/O Functions

### 🔹 Print()

The `print()` function displays values on the screen.

**Syntax**
```nisr
print(object1, object2, ..., sep=" ", end="\n")
```

Examples

```
print("Hello World")
print(1, 2, 3)
print(1, 2, 3, sep="*")
print("hello world", end="Nisr5.0")
print("hello world", end="\n")
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
print(len(list1))      # Output: 5
print(len(list1[4]))   # Output: 4
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
print(int("42"))    # Output: 42
print(int(3.99))    # Output: 3
print(int(true))    # Output: 1
```
## 🔹 float()

- Converts **values** into **floating-point numbers**.

Examples

```
print(float("3.14"))   # Output: 3.14
print(float(10))       # Output: 10.0
print(float(false))    # Output: 0.0

```
## 🔹 string()

- Converts **values** into **strings**.

Examples

```
print(string(42))      # Output: "42"
print(string(3.14))    # Output: "3.14"
print(string(true))    # Output: "true"
```
## 🔹 list()

- Converts **strings** or **tuples** into lists.

Examples

```
print(list("NISR"))    # Output: ["N", "I", "S", "R"]
print(list((1, 2, 3))) # Output: [1, 2, 3]
```
## 🔹 tuple()

Converts **strings** or **lists** into tuples.

Examples
```
print(tuple([1, 2, 3])) # Output: (1, 2, 3)
print(tuple("NISR"))    # Output: ("N", "I", "S", "R")
```

## ❌ Invalid Type Conversions

Some **built-in conversion functions** may fail when the provided input does not match the expected format. When a conversion cannot be performed safely, the runtime returns a clear and descriptive error.

**Invalid Numeric Conversion:**
```
int("hello1")
```

**Result:**
```
Error: invalid numeric format
```

This occurs because the string `"hello1"` contains **non-numeric characters** and cannot be interpreted as a **valid integer**.


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

<p align="center">
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💬 Give Feedback-blue?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/🐞 Report Bug-red?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💡 Suggestions-yellow?style=for-the-badge" />
  </a>
  <a href="mailto:nisrprogramminglanguage@gmail.com">
    <img src="https://img.shields.io/badge/✉️ Email Us-green?style=for-the-badge" />
  </a>
  <a href="https://t.me/Nisr_PL">
    <img src="https://img.shields.io/badge/📱 Telegram-blue?style=for-the-badge" />
  </a>
</p>

---
