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

