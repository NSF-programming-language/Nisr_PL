
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

