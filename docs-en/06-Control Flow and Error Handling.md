## **🔁 Control Statements and Loops in NISR**

This chapter covers the essential **control flow** structures in **NISR**, allowing your programs to make decisions and repeat actions.

**1. ✅ Control Statements**

**Control statements** allow your program to execute specific blocks of code based on conditions.

NISR uses a clean syntax where:

• Conditions are written without parentheses.

• The code block is enclosed in curly braces \{\} .

**1.1 💡 if Statement**

The `if` statement runs a block of code only when its condition evaluates to `true`.

**Syntax**
```
if condition \{

    \# code to run if condition is true

\}
```
**Example: **

```
age = 18
if age >= 18 {
    Print("Adult")
}

; Output: Adult
```

**1.2 ⚖ if...else Statement**

This statement runs one block when the condition is `true` , and a different block when the condition is `false`.

**Syntax**
```
if condition \{

    \# true block

\} else \{

    \# false block

\}
```
**Example: **

```
age = 15
if age >= 18 {
    Print("Adult")
} else {
      Print("Child")
}

; Output: Child
```

**1.3**🚦 if...elseif...else **Statement**

Used to check multiple conditions sequentialy. Once a condition is `true` , the corresponding block is executed, and the rest are skipped.

**Syntax**
```
if condition1 \{

    \# code for condition1

\} elseif condition2 \{

    \# code for condition2

\} else \{

    \# code if none of the above are true

\}
```
**Example: **

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

**1.4 **🧱** Nested Control Statements**

You can place **control statements** inside one another to check dependent conditions.

**Example**

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

## **2. **🔄** Loops and Iteration**

**Loops** are used to repeat a block of code multiple times.

## **2.1🌀 for Loop**

The `for` loop is used to iterate over sequences **\(like lists or strings\)** or **ranges of numbers**.

🔢**The** range\(\) **function**

The **range\(\)** function generates a sequence of numbers used for iteration. It has **three** forms:

• **range\(stop\)** : **Starts at** `0`, **ends at** stop `- 1` .

• **range\(start, stop\)** : **Starts at** start , **ends at** stop `- 1`.

• **range\(start, stop, step\)** : **step** controls the **increment** or **decrement**.

**Note:** The **stop** value is always excluded from the sequence. The **step** value cannot be `0` .

**Examples of** range\(\): 

1.  **range\(stop\)**

```
        for a in range(3) {
            Print(a)
        }

; Output: 0, 1, 2
```

2. **range\(start, stop\)**

```
for i in range(2, 4) {
    Print\(i)
}

; Output: 2, 3
```

🛑**The break Statement**

The `break` statement immediately **stops** the execution of the loop it is inside.

**Example:** `break` in a **for** loop: 

```
for a in range(5) {
    if a == 3 {
       break
       }
    Print(a)
}

; Output: 0, 1, 2
```

## ⏭ **The Continue Statement**

The `continue` statement stops the current iteration of the loop and moves the control to the next iteration.

**Example:** `continue` in a **for** loop.

```
for a in range(5) {
    if a == 3 {
      continue
      }
      Print(a)
}

; Output: 0, 1, 2, 4 (3 is skipped)
```

**2.2⏳ while Loop**

A **while** loop repeats a block of code as long as its condition remains `true`.

**Syntax: **

```
while condition \{

    \# code to repeat

\}
```

**Example: **

```
count = 1
while count <= 3 {
      Print(count)
      count = count + 1 ; This ensures the loop terminates
}

; Output: 1, 2, 3
```

**Caution:** Ensure that the loop condition eventualy becomes `false` . An unchanging condition will result in an **infinite loop**.

## **🛑/⏭ break and continue in while Loops**

The `break` and `continue` statements function the same way in **while** loops as they do in **for** loops.

**Example:** `break` in a **while** loop

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

---
