
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


