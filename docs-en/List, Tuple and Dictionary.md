
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

---

