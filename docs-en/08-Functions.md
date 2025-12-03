
## 📝Functions in NISR

**Functions** are fundamental building blocks in **NISR**, enabling you to **encapsulate logic**, organize your code, and promote **reuse**.

## **1. ⚙ Function Declaration & Syntax**

**Functions** are reusable blocks of code that perform specific tasks.

In **NISR**:

• **Functions** are declared using the keyword `fun` .

• **Parameters** are written inside parentheses `\(\)` .

• **Function** bodies use braces `\{\}` .

• The **return** keyword sends a value back to the caller `\(optional\)`.

**General Syntax**

```
fun function_name(parameters) {
    # Function logic
    return expression ; Optional
}
```

## **1.1 📣 Function with No Parameter and No Return Value**

Used when a function only performs an action \(like printing to the console\).

**Example**

```
fun display() {
    Print("hello world")
}

display() ; function calling

; Output: hello world
```

## **1.2 📥 Function with Parameter but No Return Value**

Used when the function requires input to perform its task but does not produce an output value for the caller.

**Example**

```
fun greet(name) {
    Print("hello", name)
}

greet("Natan")

; Output: hello Natan
```

## **1.3 📤  Function with Return Value but No Parameters**

Returns a calculated or stored value to the caller but takes no input to operate.

**Example**

```
fun get_value() {
    return 1000
}

Print(get_value())

; Output: 1000
```

## **1.4 🔄 Function with Parameter and Return Value**

The most common function type: it takes specific **input parameters** and returns a **resultant value** after execution.

**Example**

```
fun add(a, b) {
    return a + b
}

Print(add(600, 80))

; Output: 680
```

## **2.🔑 Arguments in NISR Functions**

**Arguments** are the actual values passed to the function when it is called.

**2.1 **🥇** Positional Arguments**

The order of **arguments** matters. The **first value** passed corresponds to the **first parameter**, and so on.

**Example: **

```
fun multiply(a, b) {
    return a * b
}

result = multiply(100, 300) ; 100 goes to 'a', 300 goes to 'b'
Print(result)

; Output: 30000
```

**2.2 🎁 Default Arguments**

You can assign default values to **parameters**. If the caller does not provide a value for that parameter, **NISR** uses the **default**.

**Default parameters** make functions adaptable without overloading.

**Caution:** Default values are evaluated once at function definition.

**Example**

```
fun power(x, y = 2) {
    return x ** y

}

Print(power(10)) ; y uses default value 2. Output: 100

Print(power(10, 3)) ; y uses value 3. Output: 1000
```

## **2.3 🏷 Keyword Arguments**

The **caller** specifies which parameter receives which value by using the parameter name. The order of arguments does **NOT** matter.

• **Keyword arguments** make function calls self-documenting.

• Useful when functions have many optional parameters.

**Example**

```
fun div(x, y) {
    return x / y
}

Print(div(y = 2, x = 10)) ; Order is reversed, but the result is correc

; Output: 5
```

## **3. 🧩 Advanced Function Concepts**

## **3.1 **⬆** Higher-Order Functions**

You can pass **one function** into another as a **parameter**.

**Example**

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

This is useful for **writing calculators**, **creating callbacks**, or **reusing logic** with different functions.

## **3.2 🏰 Nested Functions**

A **nested function** is defined inside another function. It is used to **encapsulate logic** or **create closures**.

**Example**

```
fun outer() {
    fun inner() {
        Print("Inner function called")
      }
      inner()
}

outer() ; Output: Inner function called

# inner() would not be accessible here
```

## **3.3 🔁 Recursion**

A **recursive function** calls itself. It must have a termination condition to avoid an **infinite loop**.

**Example: Factorial Calculation: **

```
fun factorial(n) {
    if n <= 1 {
       return 1
    }
    return n * factorial(n - 1)
}

print(factorial(5)) ; Output: 120

```

## ➕ Operators and Expressions

**Operators** in **NISR** allow you to perform **calculations**, **compare values**, **combine conditions**, and **manipulate data**. This chapter introduces all major operator categories with simple examples.

## 1. ➗ Arithmetic Operators

**Arithmetic operators** are used for standard mathematical operations on **Number** types.

- **+ (Addition):** Combines two numbers.  
  > Example: 10 + 5 results in 15.

- **- (Subtraction):** Finds the difference between two numbers.  
  > Example: 80 - 10 results in 70.

- **\* (Multiplication):** Multiplies two numbers.  
  > Example: 10 * 80 results in 800.

- **/ (Division):** Divides two numbers.  
  > Example: 80 / 80 results in 1.

- **% (Modulus/Remainder):** Returns the remainder of a division.  
  > Example: 82 % 10 results in 2.

- **\*\* (Exponentiation):** Raises the left operand to the power of the right operand.  
  > Example: 10 ** 2 results in 100.

---

## String, List and Tuple Arithmetic

**NISR** extends the `+` and `*` operators to collection types:

- **Concatenation (+):** Combines two `strings`, `lists`, or `tuples`.
- **Repetition (\*):** Repeats a `string`, `list`, or `tuple` a specified number of times.

```
str1 = "hello"
str2 = ", world"

str3 = str1 + str2 ; Concatenation
Print(str3) ; Output: hello, world

str4 = str1 * 3 ; Repetition
Print(str4) ; Output: hellohellohello

list1 = [1, 2, 3]
list2 = [4, 5]

Print(list1 + list2) ; Output: [1, 2, 3, 4, 5]

tuple1 = (1, 2)
tuple2 = (3, 4)

Print(tuple1 + tuple2) ; Output: (1, 2, 3, 4)
```

---

## 2. ⚖ Comparison Operators

**Comparison operators** compare two values and return a **Boolean** result: `true` or `false`.

- **==:** Checks if two operands are equal.  
  > Example: 3 == 3

- **!=:** Checks if two operands are not equal.  
  > Example: 2 != 1

- **> :** Checks if the left operand is greater than the right operand.  
  > Example: 5 > 2

- **>=:** Checks if the left operand is greater than or equal to the right operand.  
  > Example: 5 >= 2

- **< :** Checks if the left operand is less than the right operand.  
  > Example: 1 < 5

- **<=:** Checks if the left operand is less than or equal to the right operand.  
  > Example: 1 <= 5

```
a = 10
b = 5

Print(a == b) ; Output: false
Print(a > b)  ; Output: true
```

---

## 3. 🔁 Assignment Operators

**Assignment operators** are used to assign values to variables.

- **= (Assignment):** `x = 5` assigns the value on the right to the variable on the left.
- **+= (Add and Assign):** `x += 3` → `x = x + 3`
- **-= (Subtract and Assign):** `x -= 3` → `x = x - 3`
- **\*= (Multiply and Assign):** `x *= 3` → `x = x * 3`
- **/= (Divide and Assign):** `x /= 3` → `x = x / 3`
- **%= (Modulus and Assign):** `x %= 3` → `x = x % 3`
- **\*\*= (Exponentiate and Assign):** `x **= 2` → `x = x ** 2`

```
x = 10
x += 5
Print(x) ; x is now 15

y = 2
y **= 3
Print(y) ; y is now 8 (2*2*2)
```

---

## 4. 🔐 Logical Operators

Logical operators are used to combine **conditional statements** and return a **Boolean** result.

- **&& (Logical AND):** True only if **both** operands are true.
- **|| (Logical OR):** True if **at least one** operand is true.
- **! (Logical NOT):** Inverts the Boolean value.

### NISR Truthiness (Non-Boolean Logic)

**NISR** evaluates "truthiness" of non-Boolean values:

- `&&` returns the **last truthy value**.
- `||` returns the **first truthy value**.
- `!` returns `true` for **empty lists**.

> Example: Logical NOT on a list  
```
x = []
Print(!x) ; Output: true (because the list is empty)
```

---

# 5. ⚙ Bitwise Operators

Bitwise operators perform operations on the individual **binary bits** of integers.

- **& (AND):** 1 if both bits are 1.  
  > Example: 3 & 2 results in 2.

- **| (OR):** 1 if at least one bit is 1.  
  > Example: 3 | 2 results in 3.

- **^ (XOR):** 1 only when bits differ.  
  > Example: 3 ^ 2 results in 1.

- **~ (NOT):** Inverts all bits (`~x = -(x + 1)`).  
  > Example: ~2 results in -3.

- **<< (Left Shift):** Multiplies by 2 per shift.  
  > Example: 3 << 1 results in 6.

- **>> (Right Shift):** Divides by 2 per shift (positive numbers).  
  > Example: 6 >> 1 results in 3.

---

### Bitwise Examples

**a) Bitwise AND (&)**  
```
var1 = 3 ; 0011
var2 = 2 ; 0010

result = var1 & var2
Print(result) ; Output: 2
```

**b) Bitwise OR (|)**  
```
var1 = 3 ; 0011
var2 = 2 ; 0010

result = var1 | var2
Print(result) ; Output: 3
```

**c) Bitwise XOR (^)**  
```
var1 = 3 ; 0011
var2 = 2 ; 0010

result = var1 ^ var2
Print(result) ; Output: 1
```

**Bitwise Negation (~)**  
```
var1 = 2 ; 0010

result = ~var1
Print(result) ; Output: -3
```

**Left Shift (<<)**  
```
var1 = 3 ; 0011

result = var1 << 1
Print(result) ; Output: 6
```

**Right Shift (>>)**  
```
var1 = 6 ; 0110

result = var1 >> 1
Print(result) ; Output: 3
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


