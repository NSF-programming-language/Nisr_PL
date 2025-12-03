<p align="center">
  <img src="/assets/animated_header.svg" alt="NISR Logo" width="1000" />
</p>

---

# 🏛️ Object-Oriented Programming (OOP) in NISR

Object-Oriented Programming (OOP) in **NISR** improves code organization using **classes**, **objects**, **attributes**, and **methods**, promoting modularity and reusability.

---

## 1. 🧩 Classes and Objects

---

### • 1.1 Defining a Class and Creating an Object

A **class** is a blueprint for creating objects.  
Defined using the `class` keyword.

**Syntax**
```nisr
class ClassName(
    // attributes and methods
)
```
Object Creation
```
class Person()
    // Class definition

p = Person()     // Creating an object
print(p)         // Output: <object Person>
```

## 1.2 Constructor (fun ClassName())

A constructor initializes object attributes when an object is created.

```
class Person(
    fun Person(name, age) {
        this.name = name
        this.age = age
    }
)

p = Person("NISR5.0", 1)
print(p.name, p.age)      // Output: NISR5.0 1
```

⚠️ Incorrect usage produces an argument-size error.

## 1.3 Instance Methods

**Instance methods** operate on the **object's data**.
```
class Person(
    fun Person(name, age) {
        this.name = name
        this.age = age
    }

    fun greet() {
        return "Hello, #(this.name)"
    }
)

p = Person("NISR5.0", 1)
print(p.greet())       // Output: Hello, NISR5.0
```

## 1.4 Class (Static) Attributes

Shared by all **instances** of the class.
```
class Circle(
    PI = 3.14159

    fun Circle(radius) {
        this.radius = radius
    }
)

print(Circle.PI)     // Output: 3.14159
```
## 1.5 Class (Static) Methods

Defined using the **static** keyword.
```
class MathUtil(
    static fun sum(x, y) {
        return x + y
    }
)

print(MathUtil.sum(5, 10))   // Output: 15
```
## 1.6 Private Attributes

**Private attributes** start with` _ `and **cannot** be accessed outside the class.
```
class BankAccount(
    fun BankAccount(balance) {
        this._balance = balance
    }

    fun getBalance() {
        return this._balance
    }
)

acc = BankAccount(1000)
print(acc.getBalance())   // Output: 1000
```

---

## 2. 🌐 Inheritance and Polymorphism
## 2.1 Inheritance

Allows a **child class** to reuse **attributes** and **methods** of a **parent class**.
```
class Animal(
    fun speak() {
        return "Some sound"
    }
)

class Dog(Animal) { }

d = Dog()
print(d.speak())      // Output: Some sound
```

Method Overriding
```
class Dog(Animal) {
    fun speak() {
        return "woof!"
    }
}

print(Dog().speak())      // Output: woof!
```

## 2.2 Multiple Inheritance
```
class A { }
class B { }

class C(A, B) { }
```
## 2.3 Polymorphism

Different classes responding differently to the same method.
```
class A(
    fun speak() { return "A speaking" }
)

class B(
    fun speak() { return "B speaking" }
)

print(A().speak())    // A speaking
print(B().speak())    // B speaking
```
## 2.4 Super Function

Used to call **parent-class constructors/methods**.
```
class Person(
    fun Person(name) {
        this.name = name
    }
)

class Employee(Person) {
    fun Employee(name, id) {
        super(name)
        this.id = id
    }
}

e = Employee("Abebe", 101)
print(e.name, e.id)    // Abebe 101
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
