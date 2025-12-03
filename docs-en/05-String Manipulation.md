# 📝 String Manipulation in NISR

**Strings** in **NISR** represent sequences of characters, defined using either single (`''`) or double (`""`) quotes.
They are essential for all text-processing tasks in the language.

## 1. 🏗 Creation and Core Properties
## 1.1 Creating Strings

Strings are created by assigning text enclosed in quotes to a variable.
Both single and double quotes are supported.

```
txt = "hello world"
name = 'Alem'
Print(txt, name)
// Output: hello world Alem
```
## 1.2 Finding the Length of a String (len())

Use `len()` to get the number of characters in the string.

👉 **Spaces count as characters**.
```
str1 = "hello team nisr"
Print(len(str1))
// Output: 15
```
## 1.3 String Immutability

Strings in **NISR** are **immutable**, meaning:

- You **cannot** modify a string after creation.

- Reassigning the variable creates a new string object.

```
name = "nahom"
name = "Alem"   # Now refers to a new string
Print(name)
// Output: Alem
```
## 2. 🔍 Accessing and Slicing Content
## 2.1 String Indexing

Strings support **0-based indexing**, allowing you to access individual characters.

🔹 Positive Indexing (from the start)
```
str1 = "hello"
Print(str1[0])
// Output: h
```
🔹 Negative Indexing (from the end)
```
str1 = "hello"
Print(str1[-1])
// Output: o
```
## 2.2 String Slicing

Slicing extracts a substring.
The **end index is excluded**.

Syntax:
```
string[start:end]
```


Example:
```
str1 = "hello world"
Print(str1[0:5])
// Output: hello
```

## 3. 🛠 Transformation and Utility Methods
##3.1 Changing Case (upper() & lower())

- `upper()` → converts all characters to uppercase

- `lower()` → converts all characters to lowercase

```
str1 = "Hello World"
Print(str1.upper())
// Output: HELLO WORLD

Print(str1.lower())
// Output: hello world

```

## 3.2 Removing Spaces — strip()

Removes **leading** and **trailing** whitespace (`spaces`, `tabs`, etc.).

```
str1 = "    Hello World   "
Print(str1.strip())
// Output: Hello World
```

## 3.3 startswith() & endswith()

Checks if a string `starts` or `ends` with a given substring.
Returns `true` or `false`.

```
str1 = "Hello World"
Print(str1.startswith("H"))       // true
Print(str1.endswith("World"))     // true
Print(str1.startswith("lol"))     // false
```

## 3.4 replace()

Replaces all occurrences of a substring with another.

```
str1 = "selam"
Print(str1.replace("selam", "world"))
// Output: world
```

## 4. ➕ Operators and Formatting
## 4.1 String Comparison

**NISR** compares strings **lexicographically** using Unicode values.

👉 **Uppercase letters have lower Unicode values than lowercase letters**
(e.g., `"A" < "a"`)

```
str1 = "A"
str2 = "B"

if str1 <= str2 {
    Print("equal")
}
// Output: equal

```
## 4.2 String Concatenation (+)

Use `+` to join two or more strings.

```
str1 = "hello"
str2 = "Nisr team"
str3 = str1 + " " + str2

Print(str3)
// Output: hello Nisr team
```

## 4.3 String Multiplication (*)

Repeat a string multiple times.

```
str1 = "hi"
str2 = str1 * 6
Print(str2)
// Output: hi hi hi hi hi hi

```

## 5. 🧩 String Formatting in NISR

**NISR** uses the syntax `#{ }` to embed variables, expressions, or function calls directly inside string literals.

5.1 Basic Formatting
```
name = "Abrham"
age = 40
Print("#{name} is #{age}")
// Output: Abrham is 40
```
5.2 Formatting with Function Calls
```
fun display() { 
    return 10000 
}

Print("Value: #{display()}")
// Output: Value: 10000
```



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


