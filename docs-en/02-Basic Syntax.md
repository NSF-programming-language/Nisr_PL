<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

<p align="center">
  <img alt="Typing" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=700&color=FFC72C&center=true&vCenter=true&width=650&lines=Designed+for+Everyone%2C+Built+for+the+Future;Where+Beginners+Start+and+Developers+Grow;A+Simple+Language+for+Big+Ideas;Write+Less%2C+Create+More+%E2%80%94+With+NISR+PL;Powerful+for+Experts%2C+Friendly+for+Beginners;Code+in+Your+Language+%E2%80%94+NISR+Speaks+Many;Multilingual+Language+for+Global+Developers;Learning+to+Code+Has+Never+Been+This+Simple;From+Zero+to+Pro+%E2%80%94+The+NISR+Way;Teach%2C+Learn%2C+Build+%E2%80%94+All+with+NISR+PL" />
</p>


<p align="center">
  <a href="https://github.com/NSF-programming-language/Nisr_PL/releases/download/v0.0.4/NISR.PL.zip">
    <img src="https://img.shields.io/badge/Try-NISR-green?style=for-the-badge" />
  </a>
</p>


# 📘 NISR — Basic Syntax Reference

This section provides a clean and comprehensive overview of NISR’s basic syntax, including variables, comments, printing, conditionals, loops, functions, classes, and importing libraries.
All examples use real NISR syntax.

## 🖨️ 1. Print() Function
Multiple Values
```
print("Hello", "World")
```
Custom Separator
```
print("hello", "world", sep="*")
```
Expressions
```
print(10 ** 2)
```
## 📌 2. Variable Declaration

In **NISR**, variables are created simply by assignment.

Examples
```
x = 10
name = "Nisr"
price = 19.99
isActive = true
```

- No keyword is required.

- Types are detected automatically.

## 🗒 3. Comments

**Comments** help you describe your code. They are ignored by the compiler.

- Single-line comment:`#`

- Multiline comment: `/* ... */`

Examples
```
# This is a single line comment

/*
This is
a Multiline
Comment
*/
```
## 🖥 4. Printing Output

Use `print()` to display text or values.

Simple Print
```
print("Hello World")
```
Multiple Values
```
print("Hello", "World")
```
Custom Separator
```
print("A", "B", "C", sep="-")
# Output: A-B-C
```
Arithmetic Inside Print
```
print(10 + 5)    # Output: 15
print(6 * 6)     # Output: 36
print(10 ** 2)   # Output: 100
```
## 📦 5. Variables & Declaration (Detailed Reference)

**Variables** act as symbolic names for values.

## 5.1 Declaring Variables

**NISR** is dynamically typed. Variables are created when assigned.
```
X = "name"
print(X) # Output: name

x = 4        # Integer
x = "Sally"  # Now String
```
## 5.2 Naming Rules

Variable names must:

- Start with a letter (A–Z, a–z) or underscore _

- Be case-sensitive

- Not use keywords (true, false, fun, if, etc.)

- Not include special characters (@, !, -, etc.)

❌ Invalid Examples
```
1name = "hello"    # cannot start with number
user-age = 20      # hyphen not allowed
```
## 5.3 Variable Scope
```
a = "Outside block" # Global scope

fun block_example() {
    b = "Inside block" # Local scope
    print(b)
}

block_example() # Output: Inside block

print(a) # Output: Outside block
# print(b) # ERROR: b is not available globally

```
## 📊 6. NISR Data Types

## 6.1 Fundamental Types

String
```
"Hello"
'World'
```
Number

Supports integers and floats.
```
100
3.14159
```
Boolean
```
is_retired = true
```
## 6.2 Collection Types
A. List

Ordered, changeable, zero-indexed:
```
numbers = [1, 2, 3, 4, 5]
user_info = [21, "Marry", true, 56.9]
```
B. Tuple

Immutable collection:
```
tuple1 = (3, 4, 5, 6, 16)
```
C. Dictionary

Key–value pairs:
```
person = {
    1: 90,
    "name": "Haben",
    true: [3, 4, 6, 7]
}

print(person["name"]) # Output: Haben
```
## 🔄 7. Dynamic Typing

**NISR** checks variable type at runtime.
```
name = 80
print(name) # Output: 80

name = "Haben"
print(name) # Output: Haben
```
## 🧮 8. Conditional Statements

**NISR** uses parentheses for conditions and braces {} for blocks.

## 8.1 if...else
Syntax
```
if condition {
    # code
}
else {
    # code
}
```
Example
```
age = 18

if age >= 18 {
   print("Adult")
}
else {
   print("Child")
}
```
## 8.2 if...elseif...else
```
if condition {
    # code
}
elseif condition {
    # code
}
else {
    # code
}
```
Example
```
age = 18

if age >= 18 {
   print("Adult")
}
elseif age >= 13 {
   print("Teenager")
}
else {
   print("Child")
}
```
## 🔁 9. Loops

**NISR** provides:

- for loop

- while loop

- Supports `break` and `continue`

## 9.1 For Loop
```
for a in (1, 2, 3, 4) {
    print(a)
}
```
Using `break`
```
for a in (1, 2, 3, 4, 5) {
    if a == 3 {
        break
    }
    print(a)
}
```
Using `continue`
```
for a in (1, 2, 3, 4, 5) {
    if a == 3 {
        continue
    }
    print(a)
}
```
## 9.2 While Loop
```
i = 1

while i <= 5 {
    print(i)
    i = i + 1
}
```
`break` in while
```
i = 1

while true {
    if i > 3 {
        break
    }
    print(i)
    i = i + 1
}
```
`continue` in while
```
i = 0

while i < 5 {
    i = i + 1
    if i == 3 {
        continue
    }
    print(i)
}
```
## 🧩 10. Functions in NISR

**Functions** encapsulate logic and promote reuse.

## 10.1 Defining Functions
Using `fun`
```
fun greet(name) {
    print("Hello, " + name)
}
```

 Function with no parameters
```
fun say_hello() {
    print("Hello!")
}
```

## 10.2 Calling Functions
```
greet("Sara")
```
## 10.3 Return Values
```
fun add(a, b) {
    return a + b
}

sum = add(3, 4) # sum = 7
```
## Default Parameters
```
fun greet(name = "User") {
    print("Hello, " + name)
}

greet()        # Hello, User
greet("Helen") # Hello, Helen
```
## 🏷️ 11. Class Declaration

**NISR** supports object-oriented programming.

## 11.1 Class Without Inheritance
```
class Person {

    fun Person(name, age) {
        this.name = name
        this.age = age
    }

    fun show() {
        print("Name:", this.name, "Age:", this.age)
    }
}
```
## 11.2 Class With Inheritance
```
class Student(Person, Human) {

    fun Student(name, age, grade) {
        this.name = name
        this.age = age
        this.grade = grade
    }

    fun showGrade() {
        print("Grade:", this.grade)
    }
}
```
Details :
- [Obect Oriented Programming](10-Object%20Oriented%20Programming.md)

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
