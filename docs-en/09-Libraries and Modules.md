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

# 📚 NISR Library System

Clean, reusable, and modular code with **NISR Libraries**.

---

## • 🔧 What is a NISR Library?

A NISR library is simply a `.ns` file that contains **functions**, **classes**, or **reusable logic** that you can import into other files.  
Libraries help you write cleaner, reusable, and more maintainable code.

---

## • 📁 Project Structure Example

```
/main/main.ns
/lib/test.ns
```

- `test.ns` → Your library  
- `main.ns` → Your main program

---

## • ✍️ Writing Code Inside the Library

### ◦ test.ns

```ns
fun display() {
    Print("function from library")
    return true
}

fun add(x, y) {
    return x + y
}

class A {

    fun A(name, age) {
        this.name = name
        this.age  = age
    }

    fun getName() {
        return this.name
    }

    fun getAge() {
        return this.age
    }
}

Print("library is running")   ; Executes when library loads
```
## 📝 Explanation

- **display()** → Prints a message + returns true

- **add(x,y)** → Returns the sum of x and y

- **class A** → Stores name & age with getter methods

- The final **Print()** runs automatically once the library is imported

## • ⚙️ Compiling the Library

Before importing, compile the library:
```
nsrc test.ns -o lib
```

The compiler produces:
```
lib.nb
```

This file is what NISR loads when importing.

## • 📥 Importing the Library

Inside main.ns:
```
import lib
```
When imported:

- `lib.nb` loads automatically

- Top-level code (like `Print(...)`) executes

- All functions & classes become available under the `lib` namespace

## • 🚀 Using Library Functions
◦ **main.ns**
```
import lib

Print(lib.display())
```
Output
```
library is running
function from library
true
```
## • ➕ Calling Add Function
```
import lib

Print(lib.add(1000, 300))
```

Output
```
library is running
1300
```
## • 🏗️ Creating Objects from Library Classes
```
import lib

obj = lib.A(name="Nisr", age=20)
Print(obj.getName(), obj.getAge())
```
Output
```
library is running
Nisr 20
```
## • ✅ Summary

- Libraries are .ns files

- Must be compiled into .nb files

- Imported using import lib

- Behave like built-in modules with namespace access


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
