<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

---


# 🔁 Control Statements and Loops in NISR

This chapter covers the essential **control flow** structures in **NISR**, allowing your programs to make decisions and repeat actions.

---

## 1. ✅ Control Statements

**Control statements** allow your program to execute specific blocks of code based on conditions.

NISR uses a clean syntax where:

- Conditions are written without parentheses.
- The code block is enclosed in curly braces `{ }`.

---

### 1.1 💡 if Statement

The `if` statement runs a block of code only when its condition evaluates to `true`.

**Syntax**
```nisr
if condition {
    # code to run if condition is true
}
```
Example

```
age = 18
if age >= 18 {
    Print("Adult")
}

; Output: Adult
```

## 1.2 ⚖ if...else Statement

This statement runs one block when the condition is `true`, and a different block when the condition is `false`.

Syntax
```
if condition {
    # true block
} else {
    # false block
}

```
Example
```
age = 15
if age >= 18 {
    Print("Adult")
} else {
    Print("Child")
}

; Output: Child

```
## 1.3 🚦 if...elseif...else Statement

Used to check multiple conditions sequentially. Once a condition is `true`, the corresponding block executes and the rest are skipped.

Syntax

```
if condition1 {
    # code for condition1
} elseif condition2 {
    # code for condition2
} else {
    # code if none of the above are true
}

```
Example
```
age = 18
if age > 18 {
    Print("Adult")
} elseif age == 18 {
    Print("Teenager")
} else {
    Print("Child")
}

; Output: Teenager
```

## 1.4 🧱 Nested Control Statements

You can place control statements inside one another to check dependent conditions.

Example
```
age = 24
has_ticket = true

if age > 18 {
    if has_ticket {
        Print("Allowed entry")
    } else {
        Print("Need ticket to enter")
    }
} else {
    Print("Too young to enter")
}

; Output: Allowed entry
```

## 2. 🔄 Loops and Iteration

**Loops** are used to repeat a block of code multiple times.

## 2.1 🌀 for Loop

The `for` loop is used to iterate over sequences (lists, strings) or ranges of numbers.

## 🔢 The range() function

The range() function generates a sequence of numbers used for iteration.
It has three forms:

- range(stop) – starts at 0, ends at stop - 1

- range(start, stop) – starts at start, ends at stop - 1

- range(start, stop, step) – step controls increment/decrement (cannot be 0)

**Note**: The stop value is excluded.

Examples of `range()`:
1. `range(stop)`
```
for a in range(3) {
    Print(a)
}

; Output: 0, 1, 2
```
2. `range(start, stop)`
```
for i in range(2, 4) {
    Print(i)
}

; Output: 2, 3
```
## 🛑 The break Statement

`break` immediately stops the loop.

Example
```
for a in range(5) {
    if a == 3 {
        break
    }
    Print(a)
}

; Output: 0, 1, 2
```

## ⏭ The continue Statement

`continue` skips the current iteration and moves to the next.

Example

```
for a in range(5) {
    if a == 3 {
        continue
    }
    Print(a)
}

; Output: 0, 1, 2, 4
```

## 2.2 ⏳ while Loop

A `while` loop runs as long as its condition is `true`.

Syntax

```
while condition {
    # code to repeat
}
```

Example

```
count = 1
while count <= 3 {
    Print(count)
    count = count + 1   ; This ensures the loop terminates
}

; Output: 1, 2, 3

```

**⚠ Caution**: If the condition never becomes `false`, the loop becomes infinite.

## 🛑 / ⏭ break and continue in while Loops

They function exactly the same as in `for` loops.

Example (break)

```
i = 1
while i <= 5 {
    if i == 4 {
        break
    }
    Print(i)
    i = i + 1
}

; Output: 1, 2, 3
```

---

### 📘 Learn more:
- [Getting Started](01-Getting%20Started.md)
- [Basic Syntax](02-Basic%20Syntax.md)
- [Expressions and Operators](03-Expressions%20and%20Operators.md)
- [List, Tuple and Dictionary](04-List,%20Tuple%20and%20Dictionary.md)
- [String Manipulation](05-String%20Manipulation.md)
- [Control Flow and Error Handling](06-Control%20Flow%20and%20Error%20Handling.md)
- [Built-in-Functions](07-Built-in-Functions.md)
- [Functions](08-Functions.md)
- [Libraries and Modules](09-Libraries%20and%20Modules.md)
- [Object Oriented Programming](10-Object%20Oriented%20Programming.md)
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
