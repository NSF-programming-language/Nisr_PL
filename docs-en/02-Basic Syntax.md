
---

## 🖨️ 4. Print() Function

### Multiple values:
```nisr
Print("Hello", "World")
```

### Custom separator:
```nisr
Print("hello", "world", sep="*")
```

### Expressions:
```nisr
Print(10 ** 2)
```

---

## **1.Variable Declaration**

In **Nisr**, variables are created by
assigning a value:

**Examples:**

```nisr
x = 10
name = "Nisr"
price = 19.99
isActive = true
```

- No keyword is required.

- The type is detected automatically based on the assigned value.

## **2. Comments**

**Comments** are used to explain code. They are ignored by the compiler.

**NISR** uses `;` for single-line comments and `#...#` for
multiline comments.

> ; This is a single line comment
>
>
>
> \#
>
> This is
>
> a Multiline
> Comment
>
> \#

## **3.Printing Output**

Use the Print() function to display text or values in the console.

**Simple Print**

> Print("Hello World")

**Multiple Values**

> Print("Hello", "World")

**Custom Separator**

> Print("A", "B", "C", sep="-")
>
> Output:  A-B-C

**Arithmetic Inside Print**


> Print(10 + 5)    ; output: 15
> Print(6 * 6)     ; output: 36
> Print(10 ** 2)   ; output: 100


## **1. 📌 Variables and Declaration (Reference)**

**Variables** serve as symbolic names for values in your **NISR** program.

## **1.1 Declaring Variables**

**NISR** is a dynamically-typed language and **does not require a declaration command**. A **variable** is created the
moment you first assign a value to it.

> Syntax: variable_name = value

```
 X = "name"
 Print(X) ; Output: name

; Variable type can change (Dynamic Typing)
 x = 4 ; x is now an Integer

x = "Sally" ; x is now a String
```

## **1.2 Variable Naming Rules**

** Variable names (identifiers)**  must adhere to the following rules:

## **Variable Naming Rules**

- **Start Character:** Must start with an underscore (`_`) or an alphabetic character (`A–Z`, `a–z`).

  - ❌ **Invalid Example:** Cannot start with a number  
    `1name = "hello"`

- **Case Sensitivity:** Variable names are case-sensitive (`Name` and `name` are different).

- **Keywords:** Reserved keywords (e.g., `true`, `false`, `if`, `fun`) cannot be used as variable names.

- **Disallowed Characters:** Cannot contain special characters such as `@`, `!`, `&`, etc.
  - ❌ **Invalid Example:** Hyphens are not allowed  
    `user-age = 20`

## **1.3 Variable Scope (Concept)**

**Variables** declared inside a function block are **local** and only
available within that block.
```
a = "Outside block" ; Global scope

fun block_example() {

    b = "Inside block" ; Local scope
    Print(b)

}

block_example() ; Output: Inside block

Print(a) ; Output: Outside block

; Print(b) ; ERROR: b is not defined in global scope
```

## **2. NISR Data Types (Reference)**

**NISR** supports fundamental and collection data types.

## **2.1 Fundamental Types**

- **String:** Zero or more characters enclosed in `double (" ")` or `single (' ')` quotes.

Examples: 
> "Hello", 'World'

- **Number:** Supports **integers** (whole numbers) and **floats**(decimal numbers).

Examples:
> _ 100, 3.14159

- **Boolean:** Represents truth values: true or false.

Example:
> _ is_retired = true

## **2.2 Collection Types**

## **A. List**

A **List** is an ordered, changeable collection of items, enclosed in
**square brackets** `(\[\])`. **Lists** are **zero-indexed** (the
first element is at index 0) and can hold mixed data types.

> numbers = \[1, 2, 3, 4, 5\]

> user_info = \[21, "Marry", true, 56.9\]

## **B. Tuple**

**Tuples** are similar to lists but are enclosed in **parentheses**
**(())** and are generally used for fixed (immutable) collections of
data.

**Example: **
> tuple1 = (3, 4, 5, 6, 16)

## **C. Dictionary**

**Dictionaries** store **key-value** **pairs** and are enclosed in
**curly braces** `{}`.

- **Keys** must be unique and can be `integers`, `strings`, or `booleans`.
- **Keys** cannot be **lists** or **tuples** (since they must be immutable/hashable).

**Example: **
```
person = { 1: 90,

 "name": "Haben",
 true: \[3, 4, 6, 7\]

}

Print(person\["name"\]) ;

Output: Haben
```
## **3. 🔄 Dynamic Typing (Concept)**

**NISR** is a **dynamically-typed** **language**. This means the type of a variable is checked at runtime, and a **variable** can change its data type at any point after being created.
```
name = 80 ; Type is Integer

Print(name) ;

Output: 80

name = "Haben"    ; Type changes to String
Print(name)       ; Output: Haben
```


## 🖨️ 4. Print() Function

### Multiple values:
```nisr
Print("Hello", "World")
```

### Custom separator:
```nisr
Print("hello", "world", sep="*")
```

### Expressions:
```nisr
Print(10 ** 2)
```

---

## **1.Variable Declaration**

In **Nisr**, variables are created by
assigning a value:

**Examples:**

```nisr
x = 10
name = "Nisr"
price = 19.99
isActive = true
```

- No keyword is required.

- The type is detected automatically based on the assigned value.

## **2. Comments**

**Comments** are used to explain code. They are ignored by the compiler.

**NISR** uses `;` for single-line comments and `#...#` for
multiline comments.

> ; This is a single line comment
>
>
>
> \#
>
> This is
>
> a Multiline
> Comment
>
> \#

## **3.Printing Output**

Use the Print() function to display text or values in the console.

**Simple Print**

> Print("Hello World")

**Multiple Values**

> Print("Hello", "World")

**Custom Separator**

> Print("A", "B", "C", sep="-")
>
> Output:  A-B-C

**Arithmetic Inside Print**


> Print(10 + 5)    ; output: 15
> Print(6 * 6)     ; output: 36
> Print(10 ** 2)   ; output: 100

## **4. Conditional Statements (if / elseif /
else)**

**Nisr** uses **braces** `{}` instead of indentation. A condition is
written inside parentheses, and the code block is inside braces { }.

A **Conditional Statement** allows you to execute specific blocks of
code depending on whether a condition is `True` or `False`.

**a) if...else Statement**

Use the `if` statement to run code if a condition is `True`. Use the optional `else` clause to run code if the condition is `False`.

**General Syntax: **

```
 if (condition) {
    \# code

 }

 else {
    \# code

 }
```

**Example: **

```
age = 18

if (age >= 18) {
   Print("Adult")
}

else {
    Print("child")
}

```

You can also use **elseif** to test multiple conditions in sequence:

**General Syntax**

```
if (condition) {
  # code
}

elseif (condition) {
   # code
}

else {
  # code
}

```

**Example: **

```
age = 18

if (age >= 18) {
   Print("Adult")
}
elseif (age >= 13) {
   Print("Teenager")
}
else {
   Print("Child")
}
```

## **5. Loops in Nisr**

**Nisr** supports two types of loops:

 • **For loop**
 • **While loop**

Use `for` loop when you know how many times to repeat.

Use `while` loop when you want to repeat until a condition is no longer true.

Both loops support:

• **break;→** stops the entire loop immediately.

• **continue;→** skips the current iteration and moves to the next one.

## **5.1 For Loop**

The `for` loop iterates through sequences like `tuples` or `lists`.

**Syntax: **

```
for item in (values) {
    # code
}
```

**Example:**

```
for a in (1, 2, 3, 4) {
    Print(a)
}
```

**Using `break` in for loop: **

```
for a in (1, 2, 3, 4, 5) {
    if (a == 3) {
        break;
    }
    Print(a)
}
```

**Output:**

```
1
2
```

**Using `continue` in for loop: **

```
for a in (1, 2, 3, 4, 5) {
    if (a == 3) {
        continue;
    }
    Print(a)
}
```

**Output:**

```
1
2
4
5
```

## **5.2** **While** **Loop**

The whileloop repeats as long as the condition is `true`.

**Syntax: **

```
while (condition) {
    # code
}
```

**Example: **

```
i = 1

while (i <= 5) {
    Print(i)
    i = i + 1
}
```

**Using `break` in while loop: **

```
i = 1

while (true) {
    if (i > 3) {
        break;
    }
    Print(i)
    i = i + 1
}
```

**Output:**

```
1
2
```

**Using `continue` in while loop**

```
i = 0

while (i < 5) {
    i = i + 1

    if (i == 3) {
        continue;
    }

    Print(i)
}
```

**Output:**

```
1
2
4
5
```

## **6) Functions in NISR**

**Functions** are fundamental building blocks in **NISR**, enabling you to **encapsulate logic**, organize your code, and promote **reuse**.

## **1) Defining Functions**

In **NISR**, functions are declared using a clean and readable syntax.

You can define functions **with** **or** **without** **the**
**<u>fun</u> keyword**, giving flexibility in coding style while
maintaining readability.

**1.1 Using the `fun` Keyword**

The `fun` keyword explicitly declares a function.
Preferred in **formal or larger codebases** for clarity.

**Syntax**
```
fun functionName(parameters) {

 \# code
 return value

}

```
**Example: **
```
fun greet(name) {
    print("Hello, " + name)

}
```

In the example above, the function greet takes **one parameter (name)** and prints a personalized greeting.

## **1.2 Without the funKeyword**

For simpler scripts or personal projects, you can define a function
directly:

```
greet(name) {

print("Hello, " + name) }
```

This style uses fewer words, making the code easier to write and faster
to develop.

## **1.3 Omitting Parentheses**

**NISR** allows parameterless functions to omit parentheses:

```
fun say_hello {
    print("Hello!")

}
```
**Example: **
```
welcome {

    print("Welcome to NISR") }

```

**Note**: Omitting parentheses is allowed only when the function takes
no parameters. Including them is optional but encouraged in complex
codebases.

## **2) Calling Functions**

Invoke a function by using its name followed by parentheses, passing
arguments if required:

```
greet("Sara")
```

## **3) Return Values**

**Functions** use the `return` keyword to send a value back to the caller. If `return` is omitted, the function returns `None` by default.

```
fun add(a, b) {
       return a + b

}

sum = add(3, 4) ; sum is now 7
```

**Return values** can be of any type — `numbers`, `strings`, `boolean`,
`collections`, or `even other functions`.

**Note**: 

You can return early from a function using `return` as soon as a result is determined. Useful in **conditional logic** or **input validation**.

**Default Parameters**

**NISR** allows default values for function parameters, used when the
caller omits that argument.

```
fun greet(name = "User") {
    print("Hello, " + name)

}


greet() ; Output: Hello, User
greet("Helen") ; Output: Hello, Helen

```

 • Required parameters must come before parameters with defaults.
 • Default values are evaluated once at function definition. Avoid mutable defaults unless intended.
 • Default parameters make functions adaptable without overloading.

## **7. Class Declaration**

Nisr supports object-oriented programming.

## **7.1** **Class** **Without** **Inheritance**

```
class Person {

 ; creating a constructer

 fun Person(name, age) {

         this.name = name

         this.age = age }

 ; creating method
 fun show() {

     Print("Name:", this.name, "Age:", this.age)

    }

}
```

## **7.2 Class With Inheritance**

```
class Student(Person, Human) {

   fun Student(name, age, grade) {

       this.name = name

       this.age = age

       this.grade = grade

 }

 fun showGrade() {

     Print("Grade:", this.grade)

    }

}
```

## **8.Importing Libraries**

**Nisr** allows importing built-in libraries and your own project files.

## **8.1 Importing a Single built-in Library**

> import math

**Example: **
```
 Print(math.square(5))
```

## **8.2 Importing Multiple Files From a Folder**

Suppose your project structure looks like this:

```
 utils/

       strings.ns

       numbers.ns

       dates.ns
```

Instead of writing:
```
 import utils.strings
 import utils.numbers
 import utils.dates
```

**Nisr** allows a cleaner way of importing:

> import utils(strings, numbers, dates)

## **8.3 Importing From Nested Folders (Sub-folders)**

**Example folder structure: **

```
 main_folder/
            data/
                users.ns
```

To `import` **users.ns** inside data:

> import main_folder(data.users)

## **8.4 Importing Your Own File in the Same Directory**

Example:

```
 helper.ns

 main.ns
```

To `import` **helper.ns** Inside main.ns write:

> import helper

---


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
