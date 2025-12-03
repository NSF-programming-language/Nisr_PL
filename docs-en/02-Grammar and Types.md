
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

