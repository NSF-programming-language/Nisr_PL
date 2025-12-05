<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

<p align="center">
  <img alt="Typing" src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=700&color=FFC72C&center=true&vCenter=true&width=650&lines=Designed+for+Everyone%2C+Built+for+the+Future;Where+Beginners+Start+and+Developers+Grow;A+Simple+Language+for+Big+Ideas;Write+Less%2C+Create+More+%E2%80%94+With+NISR+PL;Powerful+for+Experts%2C+Friendly+for+Beginners;Code+in+Your+Language+%E2%80%94+NISR+Speaks+Many;Multilingual+Language+for+Global+Developers;Learning+to+Code+Has+Never+Been+This+Simple;From+Zero+to+Pro+%E2%80%94+The+NISR+Way;Teach%2C+Learn%2C+Build+%E2%80%94+All+with+NISR+PL" />
</p>


<p align="center">
  <a href="https://Github.com/Nisr-programming-language/Nisr_PL">
    <img src="https://img.shields.io/badge/Try-NISR-green?style=for-the-badge" />
  </a>
</p>

---


# 📦 Lists, Tuples, and Dictionaries in Nisr

## 🧾 Lists and Tuples in Nisr

**Lists** and **tuples** are two fundamental collection types in **Nisr**.

- Lists → changeable, dynamic (mutable)

- Tuples → fixed, unchangeable (immutable)

## 1. 📋 Lists in Nisr

A **list** is an **ordered**, **mutable collection** of items.

**Lists** use square brackets: `[]`.

`Lists` can store **any data type**, including:

- integers

- strings

- booleans

- floats

- even other lists or tuples

## 1.1 🛠 Creating Lists

```
numbers = [1, 2, 3, 4]
names = ["Aman", "Liya", "Sara"]
mixed = [21, "Hello", true, 5.9]
```

## 1.2 📚 Nested Lists

**Lists** can contain **other lists**:

```
nested = [
    [1, 2, 3],
    ["a", "b"],
    [true, false]
]

print(nested[0])       # [1, 2, 3]
print(nested[1][1])   # b
```

## 1.3 🎯 Accessing List Elements (Indexing)

- Lists use 0-based indexing

- First element → index `0`

- Use brackets: `[index]`
```
fruits = ["apple", "banana", "orange"]

print(fruits[0])   # apple
print(fruits[2])   # orange
```

## 1.4 ✏ Updating List Items

**Lists** are **mutable**, meaning you can modify them:

```

fruits = ["apple", "banana", "orange"]
print(fruits[0])        # apple

fruits[0] = "grape"
print(fruits[0])        # grape
```
## 1.5 ➕ Adding Items (append)

```
numbers = [1, 2]
numbers.append(3)

print(numbers) # [1, 2, 3]
```

## 1.6 🔼 Inserting Items (insert)

```
fruits = ["banana", "orange"]
fruits.insert(0, "apple")

print(fruits) # ["apple", "banana", "orange"]
```

## 1.7 ❌ Removing Items (remove)

```
colors = ["red", "green", "blue"]
colors.remove("green")

print(colors) # ["red", "blue"]
```

## 1.8 ✂ List Slicing

```
list[start:end]
```

- Start index → **included**

- End index → **excluded**

```
data = [10, 20, 30, 40, 50]
subset = data[1:4]

print(subset) # [20, 30, 40]
```

---

## 2. 🧊 Tuples in Nisr

A tuple is:

- ordered

- immutable (unchangeable)

Tuples use **parentheses**: `()`.

## 2.1 🛠 Creating Tuples

```
coordinates = (10, 20)
months = ("Jan", "Feb", "Mar")
```

One-item tuple:

```
single_item = (100,)     # tuple
not_a_tuple = (100)      # integer!

print(typeof(single_item)) # tuple
print(typeof(not_a_tuple)) # int
```
## 2.2 📚 Nested Tuples

```
nested_tuple = (
    (1, 2),
    (3, 4, 5),
    ("a", "b")
)

print(nested_tuple[1])      # (3, 4, 5)
print(nested_tuple[2][0])   # "a"

combo = (1, [10, 20], "X")
print(combo[1][0]) # 10
```

## 2.3 🎯 Accessing Tuple Items

```
colors = ("red", "green", "blue")

print(colors[0]) # red
```

## 2.4 🔗 Tuple Concatenation

Tuples can be combined using `+`:

```
t1 = (1, 2)
t2 = (3, 4)

print(t1 + t2) # (1, 2, 3, 4)
```

## 2.5 🧮 Tuple Methods

Tuples support limited methods:

- `count(value)`

- `len(tuple)`

```
t = (1, 2, 2, 3)
print(t.count(2)) # 2

t2 = (10, 20, 30)
print(len(t2)) # 3
```

## 2.6 📤 Returning a Tuple From a Function

```
fun get_range() {
    return (1, 10)
}

print(get_range()) # (1, 10)
```

---

## 🗃 Dictionary Manipulation in NISR

**Dictionaries** store data in **key-value** pairs and use `{}`.

## 1. ⚙ Dictionary Fundamentals
## 1.1 What Is a Dictionary?

- Uses { key: value }

- **Keys must be immutable** (hashable)

✔ Valid keys:

- int

- float

- string

- tuple

❌ Invalid keys:

- lists

- other dictionaries

```
dict1 = {
    "name": "Abe",
    "age": 30,
    10: "nisr5.0"
}

print(dict1)
# Output may vary
```

## 1.2 Accessing Values

```
print(dict1["name"])    # Abe
```

## 1.3 Dictionary Size – len()

```
print(len(dict1)) # 3
```

## 2. 📝 Modification and Creation

## 2.1 Updating Values

```
dict1["name"] = "Kidan"

print(dict1)
# { "name": "Kidan", "age": 30, 10: "nisr5.0" }
```


## 2.2 Adding New Key-Value Pair
```
dict1["members"] = 7
```

## 3. 🧩 Built-in Dictionary Methods

##3.1 get() – Safe Access
```
print(dict1.get("name"))       # Kidan
print(dict1.get("kkk"))        # null
print(dict1.get("kkk", 100))   # 100
```
## 3.2 set() – Add New Entry
```
a = dict1.set("version", 2)

print(dict1, a)
```
## 3.3 delete() – Remove a Key
```
dict1 = { "name": "Abe", "age": 30, 10: "nisr5.0" }
s = dict1.delete(10)

print(dict1, s)    # { "name": "Abe", "age": 30 } true
```
## 3.4 update() – Merge Dictionaries

Merge two dictionaries:
```
dict1 = { "name":"Abe", "age":30 }
dict2 = { 20:30, "grade": 10 }

w = dict1.update(dict2)
print(dict1, w)
```
Merge a single key-value pair:
```
w = dict1.update("city": "Addis")
print(dict1, w)
```

## 3.5 size() – Alternative to len()
```
dict1 = { "name":"Abe", "age":30 }

print(dict1.size()) # 2
```

## 3.6 clear() – Remove All Items
```
print(dict1.clear()) # {}
```
## 4. 🔑 Retrieval Methods
keys()
```
dict1 = { "name": "Abe", "age": 30, 10: "nisr5.0" }

print(dict1.keys())
# ["name", "age", 10]
```
values()
```
print(dict1.values())
# ["Abe", 30, "nisr5.0"]
```
items()
```
print(dict1.items())
# ["name":"Abe", "age":30, 10:"nisr5.0"]
```
## 4.1 has() – Check If Key Exists
```
if has(555) {
    print(true)
} else {
    print(false)
}

# false
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
