
## 📝**String Manipulation in Nisr**

**Strings** in **NISR** represent sequences of characters, defined using either **single** `\( '' \)` or **double** `\( "" \)` quotes. They are fundamental for all text processing tasks in the language.

## **1. 🏗 Creation and Core Properties**

## **1. Creating Strings**

**Strings** are initialized by simply assigning text enclosed in quotes to a variable. **NISR** accepts both single and double quotes.

**Example:**

```
    txt = "hello world"
    name = 'Alem'
    Print (txt, name)
    // Output: hello world Alem
```

## **2. Finding the Length of a String** **(** len\(\) **)**

Use the built-in function **len(\)** to determine the number of characters in a string.

- **Spaces** are counted as characters.

**Example:**

```
    str1 = "hello team nisr"
    Print (len(str1))
    // Output: 15
```

## **3. String Immutability**

**Strings** in **NISR** are **immutable**. This means once a string object is created, its content cannot be altered. Reassigning the variable replaces the entire string object.

**Example:**

```
    name = "nahom"
    name = "Alem" # The variable now references a new string "Alem"
    Print (name)
    // Output: Alem
```

**2. **🔍** Accessing and Slicing Content**

**3. String Indexing**

Indexing all rows accessing a single character using its position. **NISR** uses **0-based** **indexing**.

● **Positive Indexing \(from the start\):**

```
    str1 = "hello"
    Print(str1[0])
    // Output: h
```

● **Negative Indexing \(from the end\):**

```
    str1 = "hello"
    Print (str1[-1])
    // Output: o
```

## **4. String Slicing**

**Slicing** extracts a substring. The character at the end index is **not included** in the result.

**Syntax:** 

> string\[start:end\]

**Example:**

```
    str1 = "hello world"
    Print (str1[0:5])
    // Output: hello
```

**3. **🛠** Transformation and Utility Methods**

## **6. Changing Case** **(** upper\(\) **&** lower\(\) **)**

These methods provide basic case **conversion functionality**.

● upper\(\) **:** Converts al characters to uppercase.

● lower\(\) **:** Converts al characters to lowercase.

● **Example:**

```
    str1 = "Hello World"
    Print(str1.upper())
    // Output: HELLO WORLD

    Print (str1.lower())
    // Output: hello world
```

## **7.** **Removing Spaces strip\(\)**

The **strip\(\)** method removes **leading** and **trailing whitespace characters** \(`spaces`, `tabs`, etc.\) from the string.

**Example:**

```
    str1 = "    Hello World   "
    Print (str1.strip())
    // Output: Hello World
```

**8. startswith\(\) & endswith\(\)**

These utility methods check if a string **begins** or **ends** with a specified substring and return a boolean value \( `true` **or** `false` \).

● **Example:**

```
    str1 = "Hello World"
    Print(str1.startswith("H")) # Returns true
    Print(str1.endswith("World")) # Returns true
    Print(str1.startswith("lol")) # Returns false
```

**9.** replace\(\)**

The **replace\(\)** method substitutes all occurrences of a specified substring with another string.

● **Example:**

```
    str1 = "selam"
    Print (str1.replace("selam", "world"))
    // Output: world
```

## **4. **➕** Operators and Formatting**

## **10. String Comparison**

**NISR** compares strings lexicographicaly using their underlying **Unicode values**.

● Comparison operators \( `==` , `\!=` , `>` , `<` , etc.\) are used to **evaluate** order.

**Note: ** **Uppercase letters** have **lower Unicode** values than **lowercase letters** \( `A` < `B` but `a` > `Z` \).

**Example:**

```
    str1 = "A"
    str2 = "B"
    if str1 <= str2 {
       Print ("equal")
    }
    // Output: equal (because "A" comes before "B")
```

## **11. String Concatenation**

Use the addition operator `\( \+ \)` to join strings together end-to-end.

**Example:**

```
    str1 = "hello"
    str2 = "Nisr team"
    str3 = str1 + " " + str2
    Print (str3)
    // Output: hello Nisr team
```

## **12. String Multiplication**

Use the **multiplication operator** `\( \* \)` with an integer to repeat a string a specified number of times.

● **Example:**

```
    str1 = "hi"
    str2 = str1 * 6
    Print (str2)
    // Output: hi hi hi hi hi hi
```

## **13. String Formatting in Nisr**

**NISR** uses the special syntax `\#\{ \}` for **embedding variables**, **expressions**, or **function calLs directly into a string literal**.

**Basic Example:**

```
    name = "Abrham"
    age = 40
    Print("#\{name} is \#{age}")
    // Output: Abrham is 40
```

**Formatting with Function Calls:**

```
    fun display() { return 10000 }
```

```

    Print("Value: \#{display()}")
    // Output: Value: 10000
```


---



