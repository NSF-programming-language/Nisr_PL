
---
# 🦅**NISR PROGRAMMING LANGUAGE**
---

# 📝 Functions in NISR

**Functions** are fundamental building blocks in **NISR**, enabling you to **encapsulate logic**, organize your code, and promote **reuse**.

---

## 1. ⚙ Function Declaration & Syntax

**Functions** are reusable blocks of code that perform specific tasks.

In **NISR**:

- Declared using the keyword `fun`.  
- Parameters are written inside parentheses `()`.  
- Function bodies use braces `{}`.  
- The `return` keyword sends a value back to the caller *(optional)*.

**General Syntax**
```nisr
fun function_name(parameters) {
    # Function logic
    return expression ; Optional
}

```
## 1.1 📣 Function with No Parameter and No Return Value

Used when a function only performs an action (like printing to the console).

```
fun display() {
    Print("hello world")
}

display() ; function calling

; Output: hello world
```
## 1.2 📥 Function with Parameter but No Return Value

Used when the function requires input to perform its task but does not produce an output for the caller.

```
fun greet(name) {
    Print("hello", name)
}

greet("Natan")

; Output: hello Natan
```

## 1.3 📤 Function with Return Value but No Parameters

Returns a calculated or stored value to the caller but takes no input.

```
fun get_value() {
    return 1000
}

Print(get_value())

; Output: 1000
```

## 1.4 🔄 Function with Parameter and Return Value

The most common function type: takes input **parameters** and returns a result.

```
fun add(a, b) {
    return a + b
}

Print(add(600, 80))

; Output: 680
```

## 2. 🔑 Arguments in NISR Functions

**Arguments** are the actual values passed to a function when it is called.

## 2.1 🥇 Positional Arguments

The order of **arguments** matters: the first value passed corresponds to the first parameter, and so on.
```
fun multiply(a, b) {
    return a * b
}

result = multiply(100, 300) ; 100 goes to 'a', 300 goes to 'b'
Print(result)

; Output: 30000
```
## 2.2 🎁 Default Arguments

Assign default values to **parameters**. If the caller does not provide a value, **NISR** uses the default.

```
fun power(x, y = 2) {
    return x ** y
}

Print(power(10))    ; y uses default 2 → Output: 100
Print(power(10, 3)) ; y uses value 3 → Output: 1000
```

## 2.3 🏷 Keyword Arguments

Specify which parameter receives which value using the parameter name. The order of arguments does NOT matter.
```
fun div(x, y) {
    return x / y
}

Print(div(y = 2, x = 10)) ; Order is reversed, result is correct

; Output: 5
```

## 3. 🧩 Advanced Function Concepts
## 3.1 ⬆ Higher-Order Functions

You can pass **one function** into another as a **parameter**.
```
fun add(x, y) {
    return x + y
}

fun operate(fun_name, x, y) {
    return fun_name(x, y)
}

result = operate(add, 10, 20)

Print(result)

; Output: 30

```
- Useful for writing **calculators**, **callbacks**, or **reusing logic**.

## 3.2 🏰 Nested Functions

A **nested function** is defined inside **another function**. It encapsulates **logic** or **creates closures**.

```
fun outer() {
    fun inner() {
        Print("Inner function called")
    }
    inner()
}

outer() ; Output: Inner function called

# inner() is not accessible here
```
## 3.3 🔁 Recursion

A **recursive function** calls itself. Must have a termination condition to avoid an **infinite loop**.

Example: Factorial Calculation

```
fun factorial(n) {
    if n <= 1 {
       return 1
    }
    return n * factorial(n - 1)
}

Print(factorial(5)) ; Output: 120
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

