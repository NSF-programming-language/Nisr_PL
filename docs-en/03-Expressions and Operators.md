<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

<p align="center">
  <img alt="Typing" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=700&color=FFC72C&center=true&vCenter=true&width=650&lines=Designed+for+Everyone%2C+Built+for+the+Future;Where+Beginners+Start+and+Developers+Grow;A+Simple+Language+for+Big+Ideas;Write+Less%2C+Create+More+%E2%80%94+With+NISR+PL;Powerful+for+Experts%2C+Friendly+for+Beginners;Code+in+Your+Language+%E2%80%94+NISR+Speaks+Many;Multilingual+Language+for+Global+Developers;Learning+to+Code+Has+Never+Been+This+Simple;From+Zero+to+Pro+%E2%80%94+The+NISR+Way;Teach%2C+Learn%2C+Build+%E2%80%94+All+with+NISR+PL" />
</p>


<p align="center">
  <a href="https://Github.com/Nisr-programming-language/Nisr_PL">
    <img src="https://img.shields.io/badge/Try%20NISR-Online-green?style=for-the-badge" />
  </a>
</p>

---


## ➕ Operators and Expressions

**Operators** in **NISR** allow you to perform **calculations**, **compare values**, **combine conditions**, and **manipulate data**.  
This chapter introduces all major operator categories with simple and clear examples.

---

## 1. ➗ Arithmetic Operators

**Arithmetic operators** are used for standard mathematical operations on **Number** types.

- **+ (Addition):** Combines two numbers.  
  > Example: `10 + 5` results in **15**

- **- (Subtraction):** Finds the difference between two numbers.  
  > Example: `80 - 10` results in **70**

- **\* (Multiplication):** Multiplies two numbers.  
  > Example: `10 * 80` results in **800**

- **/ (Division):** Divides two numbers.  
  > Example: `80 / 80` results in **1**

- **% (Modulus):** Returns remainder of a division.  
  > Example: `82 % 10` results in **2**

- **\*\* (Exponentiation):** Raises a number to a power.  
  > Example: `10 ** 2` results in **100**

---

## 📚 String, List, and Tuple Arithmetic

NISR extends the `+` and `*` operators to work with **strings, lists, and tuples**.

### ✔ Concatenation (`+`)
Combines two `strings`, `lists`, or `tuples`.

### ✔ Repetition (`*`)
Repeats a `string`, `list`, or `tuple`.

```nisr
str1 = "hello"
str2 = ", world"

str3 = str1 + str2   # Concatenation
print(str3)          # Output: hello, world

str4 = str1 * 3      # Repetition
print(str4)          # Output: hellohellohello

list1 = [1, 2, 3]
list2 = [4, 5]

print(list1 + list2) # Output: [1, 2, 3, 4, 5]

tuple1 = (1, 2)
tuple2 = (3, 4)

print(tuple1 + tuple2) # Output: (1, 2, 3, 4)
```

## 2. ⚖ Comparison Operators

**Comparison operators** compare two values and return a Boolean result (`true` or `false`).

- == — Equal

  Example: `3 == 3`

- != — Not Equal

  Example: `2 != 1`

- \> — Greater Than

  Example: `5 > 2`

- \>= — Greater Than or Equal

  Example: `5 >= 2`

- < — `Less Than`

  Example: `1 < 5`

- <= — Less Than or Equal

  Example: `1 <= 5`


```
a = 10
b = 5

print(a == b) # Output: false
print(a > b)  # Output: true
```

## 3. 🔁 Assignment Operators

**Assignment** operators assign values to variables.

- = — Basic assignment

- += — Add and assign

- -= — Subtract and assign

- /= — Divide and assign

```
x = 10
x += 5
print(x) # Output: 15

y = 6
y -= 3
print(y) # Output: 3  

```

## 4. 🔐 Logical Operators

**Logical operators** combine conditional expressions.

- && — Logical AND (true only if both are true)

- || — Logical OR (true if at least one is true)

- ! — Logical NOT (inverts Boolean value)

or **you can also use them as text form**:

- AND — Logical AND (true only if both are true)

- OR — Logical OR (true if at least one is true)

- NOT — Logical NOT (inverts Boolean value)

  
✔ NISR Truthiness Rules

Non-Boolean values behave as follows:

- &&(AND) returns the last truthy value

- ||(OR) returns the first truthy value

- !(NOT) returns true for empty lists

```
x = []
print(!x) # Output: true   # empty list = false → inverted = true
```

## 5. ⚙ Bitwise Operators

**Bitwise operators** work on the binary representation of integers.

- & — AND

  Example: `3 & 2` → 2

- | — OR

  Example: `3 | 2` → 3

- ^ — XOR

  Example: `3 ^ 2` → 1

- ~ — NOT

  Formula: `~x = -(x + 1)`
  Example: `~2` → -3

- << — Left Shift (multiply by 2 each shift)

  Example: `3 << 1` → 6

- \>> — Right Shift (divide by 2 each shift)

  Example: `6 >> 1` → 3

## 🔧 Bitwise Examples

Bitwise AND (&)

```
var1 = 3   # 0011
var2 = 2   # 0010

result = var1 & var2
print(result) # Output: 2
```

Bitwise OR (|)

```
var1 = 3
var2 = 2

result = var1 | var2
print(result) # Output: 3
```

Bitwise XOR (^)

```
var1 = 3
var2 = 2

result = var1 ^ var2
print(result) # Output: 1
```

Bitwise NOT (~)

```
var1 = 2

result = ~var1
print(result) # Output: -3
```
Left Shift (<<)

```
var1 = 3

result = var1 << 1
print(result) # Output: 6
```

Right Shift (>>)

```
var1 = 6

result = var1 >> 1
print(result) # Output: 3
```


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

<p align="center">
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💬 Give Feedback-blue?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/🐞 Report Bug-red?style=for-the-badge" />
  </a>
  <a href="https://forms.gle/kjmtNFNrPeScw4ox5">
    <img src="https://img.shields.io/badge/💡 Suggestions-yellow?style=for-the-badge" />
  </a>
  <a href="mailto:nisrprogramminglanguage@gmail.com">
    <img src="https://img.shields.io/badge/✉️ Email Us-green?style=for-the-badge" />
  </a>
  <a href="https://t.me/Nisr_PL">
    <img src="https://img.shields.io/badge/📱 Telegram-blue?style=for-the-badge" />
  </a>
</p>

---
