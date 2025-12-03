
## 🧾**Lists and Tuples in Nisr**

**Lists and tuples** are two fundamental collection types in **Nisr**.

Both allow storing **multiple values**, but they behave differently:

● **Lists** → changeable, dynamic \(mutable\)

● **Tuples** → fixed, unchangeable \(immutable\)

## **1. Lists in Nisr**

A **list** is an ordered, **mutable \(changeable\)** collection of items. **Lists** use square brackets `\[\]`.

`Lists` can store any data type, including **mixed types** \(`integers`, `strings`, `booleans`, `floats`, `even other lists` or `tuples`\).

## **1.1 Creating Lists**

Examples:

```
numbers = [1, 2, 3, 4]
names = ["Aman", "Liya", "Sara"]
mixed = [21, "Hello", true, 5.9]
```

**1.2 Nested Lists**

A **list** can contain **another list**, creating complex structures:

```
nested = [
[1, 2, 3],
["a", "b"],
[true, false]
]

Print (nested[0]) ; [1, 2, 3]
Print (nested[1][1]) ; b
```

## **1.3 Accessing List Elements \(Indexing\)**

● Lists use **0-based indexing**.

● The first element is at index 0.

● You access elements using `\[index\]`.

Example:

```
fruits = ["apple", "banana", "orange"]

Print (fruits[0]) ; apple
Print (fruits[2]) ; orange
```

## **1.4 Updating List Items**

Since **lists** are mutable, you can modify elements after creation:

```
fruits = ["apple", "banana", "orange"]
Print (fruits[0]) ; apple

fruits[0] = "grape" ; Update first element
Print (fruits[0]) ; grape
```

## **1.5 Adding Items \(append\)**

Use the **append\(\)** method to add an item to the **end** of the list.

```
numbers = [1, 2]
numbers.append(3)

Print(numbers) ; [1, 2, 3]
```

## **1.6 Inserting Items \(insert\)**

Use the **insert\(index, item\)** method to add an item at a **specific index**.

```
fruits = ["banana", "orange"]
fruits.insert(0, "apple")

Print (fruits) ; ["apple", "banana", "orange"]
```

**1.7 Removing Items \(remove\)**

Use the **remove\(item\)** method to delete the first occurrence of a specific value.

```
colors = ["red", "green", "blue"]
colors.remove("green")

Print (colors) ; ["red", "blue"]
```

## **1.8 Slicing Lists**

**Slicing** is used to get a subset \(part\) of a list.

**Syntax: list\[start:end\]**

● The **start** index is included.

● The **end** index is **excluded**.

Example:

```
data = [10, 20, 30, 40, 50]
subset = data[1:4] ; From index 1 (20) up to (but not including) index 4 (50)

Print (subset) ; [20, 30, 40]
```

## **2. Tuples in Nisr**

A **tuple** is an **ordered**, **immutable \(unchangeable\)** collection of items. **Tuples** use parentheses `\(\)`.

They are often used for fixed data structures where the content should not change.

## **2.1 Creating Tuples**

**Example:**

```
coordinates = (10, 20)
months = ("Jan", "Feb", "Mar")
```

Tuple with **one** item:

If you have only one item, you must include a comma `\(,\)` after the item.

```
single_item = (100,) ; This is a tuple
not_a_tuple = (100) ; This is just an integer!

Print (typeof(single_item)) ; tuple
Print (typeof(not_a_tuple)) ; int
```

## **2.2 Nested Tuples**

**Tuples** can contain other **tuples** or **lists**:

```
nested_tuple = (
(1, 2),
(3, 4, 5),
("a", "b")
)

Print (nested_tuple[1]) ; (3, 4, 5)
Print (nested_tuple[2][0]) ; "a"
combo = (1, [10, 20], "X")
Print (combo[1][0]) ; 10
```

## **2.3 Accessing Tuple Items**

**Tuples** use the same **0-based indexing** as lists:

**Example: **
```
colors = ("red", "green", "blue")

Print (colors[0]) ; red
```

## **2.4 Tuple Concatenation**

**Tuples** can be combined using `\+`, which creates a **new tuple** \(since the originals cannot change\).

**Example: **

```
t1 = (1, 2)
t2 = (3, 4)

Print(t1 + t2) ; (1, 2, 3, 4)
```

## **2.5 Tuple Methods**

**Tuples** have fewer methods because they are immutable. **Nisr** supports:

1. **count\(value\)**: Returns the number of times a specified value occurs in a tuple.

2. **len\(tuple\)**: Returns the number of items in the tuple.

Example:

```
t = (1, 2, 2, 3)
Print(t.count(2)) ; 2

t2 = (10, 20, 30)
Print (len(t2)) ; 3
```

## **2.6 Returning a tuple in a function** 

**Tuples** are often used to return multiple values from a function:

```
fun get_range() {
return (1, 10)
}

Print (get_range()) ; (1, 10)
```


🗃**NISR Dictionary Manipulation**

Dictionaries in NISR are collections that store data in **key-value pairs**. They are highly effective for fast lookups, organization, and modification of related information.

**1. **⚙** Dictionary Fundamentals**

**1. What Is a Dictionary?**

A dictionary is declared using curly braces \( \{\} \) with each item consisting of a key: value pair.

● **Key Requirements:** Keys must be **hashable** \(immutable/constant values\).

● ✅ **Valid Keys:** Integers, floats, strings, and tuples.

● ❌ **Invalid Keys:** Lists \(mutable\) and other dictionaries.

● **Example:**

```
    dict1 = {
        "name": "Abe",
        "age": 30,
        10: "nisr5.0"
    }

    Print(dict1)
    // Output may vary: { "name": "Abe", 10: "nisr5.0", "age": 30}
```

Note: Dictionary output order may shuffle because dictionaries are generally unordered collections.

**2. Accessing Dictionary Values**

Values are accessed using the corresponding key inside square brackets \( \[\] \).

● **Example:**

```
    Print(dict1["name"])
    // Output: Abe
```

**3. Checking Dictionary Size ( len() )**

The built-in function len\(\) returns the total number of key-value pairs in the dictionary.

● **Example:**

```
    Print(len(dict1))
    // Output: 3
```

**2. **📝** Modification and Creation**

**4. Updating Dictionary Values**

To change a value for an **existing key**, assign a new value to that key.

● **Example:**

```
    dict1["name"] = "Kidan"
    Print(dict1)
    // Output: { "name": "Kidan", "age": 30, 10: "nisr5.0" }
```

**5. Adding New Key-Value Pairs**

To add a new entry, assign a value to a **new key** that doesn't yet exist in the dictionary.

- **Logic:**

  ● If the key exists: The value is **updated** (see point 4).

  ● If the key does not exist: A new pair is **added**.

● **Example:**

```
    dict1["members"] = 7
    Print(dict1)
    // Output: { "members": 7, "name": "Kidan", 10: "nisr5.0", "age": 30 }
```

**3. **🧩** Built-in Dictionary Methods**

NISR dictionaries include several helpful built-in methods for safer access and manipulation.

**6.1** get\(\) **– Safe Access to Keys**

The get\(\) method provides a safe way to access values:

● Returns the value associated with the key if it exists.

● Returns null if the key does not exist.

● Optionally returns a provided **default value** if the key is missing.

● **Examples:**

```
    // Using previous dict1: { "name": "Kidan", "age": 30, 10: "nisr5.0}
    Print(dict1.get("name"))         // Output: Kidan
    Print(dict1.get("kkk"))         // Output: null (key doesn't exist)
    Print(dict1.get("kkk", 100))    // Output: 100 (returns default value)
```

**6.2** set\(\) **– Add a New Entry**

The set\(\) method adds a new key-value pair and returns the value that was added.

● **Example:**

```
    a = dict1.set("version", 2)
    Print(dict1, a)
    // Output: { "version": 2, ..., "age": 30 }
```

**6.3** delete\(\) **– Remove a Key**

The delete\(\) method removes a specified key-value pair and returns a boolean status: true if the key existed and was deleted, or false if it was not found.

● **Example:**

```
    dict1 = { "name": "Abe", "age": 30, 10: "nisr5.0" }
    s = dict1.delete(10)

    Print(dict1, s)
    // Output: { "name": "Abe", "age": 30 } true

     s = dict1.delete(100) // 100 doesn't exist
     Print(s)
    // Output: false
```

**6.4** update\(\) **– Merging Dictionaries**

The update\(\) method allows you to merge another dictionary or a single key-value pair into the existing dictionary. It returns true on success.

● **Merging two dictionaries:**

```
    dict1 = { "name":"Abe", "age":30 }
    dict2 = { 20:30, "grade": 10 }
    w = dict1.update(dict2)

    Print(dict1, w)
    // Output: { "grade":10, "name": "Abe", 20:30, "age":30 } true
```

● **Merging a single key-value pair:**

```
    w = dict1.update("city": "Addis")

    Print(dict1, w)
    // Output: { "city": "Addis", ..., "grade":10 } true
```

**6.5** size\(\) **– Alternative Length Check**

The size\(\) method is another way to retrieve the number of entries, equivalent to len\(\) .

● **Example:**

```
    dict1 = { "name":"Abe", "age":30 }
    Print(dict1.size())
    // Output: 2
```

**6.6** clear\(\) **– Remove All Items**

The clear\(\) method completely removes all key-value pairs, resulting in an empty dictionary.

● **Example:**

```
    Print(dict1.clear())
    // Output: {}
```

**4. **🔑** Retrieval Methods**

**6.7. Dictionary Return Methods**

These methods return lists containing components of the dictionary.

● keys\(\) **:** Returns a List of all keys.

```
    dict1 = { "name": "Abe", "age": 30, 10: "nisr5.0" }
    Print(dict1.keys())
    // Output: ["name", "age", 10]
```

● values\(\) **:** Returns a List of all values.

```
    Print(dict1.values())
    // Output: ["Abe", 30, "nisr5.0"]
```

● items\(\) **:** Returns a List of key-value pairs.

```
    Print(dict1.items())
    // Output: ["name":"Abe", "age":30, 10:"nisr5.0"]
```

**6.8** has\(\) **– Checking If a Key Exists**

Use the has\(key\) method to check for the presence of a key, which returns a boolean.

● **Example:**

```
    if dict1.has(555) {
       Print(true)
    } else {
       Print(false)
    }
    // Output: false
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

