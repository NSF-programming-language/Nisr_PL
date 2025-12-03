---

## 📝**Functions in NISR**

**Functions** are fundamental building blocks in **NISR**, enabling you to **encapsulate logic**, organize your code, and promote **reuse**.

## **1. ⚙ Function Declaration & Syntax**

**Functions** are reusable blocks of code that perform specific tasks.

In **NISR**:

• **Functions** are declared using the keyword `fun` .

• **Parameters** are written inside parentheses `\(\)` .

• **Function** bodies use braces `\{\}` .

• The **return** keyword sends a value back to the caller `\(optional\)`.

**General Syntax**

```
fun function_name(parameters) {
    # Function logic
    return expression ; Optional
}
```

## **1.1 📣 Function with No Parameter and No Return Value**

Used when a function only performs an action \(like printing to the console\).

**Example**

```
fun display() {
    Print("hello world")
}

display() ; function calling

; Output: hello world
```

## **1.2 📥 Function with Parameter but No Return Value**

Used when the function requires input to perform its task but does not produce an output value for the caller.

**Example**

```
fun greet(name) {
    Print("hello", name)
}

greet("Natan")

; Output: hello Natan
```

## **1.3 📤  Function with Return Value but No Parameters**

Returns a calculated or stored value to the caller but takes no input to operate.

**Example**

```
fun get_value() {
    return 1000
}

Print(get_value())

; Output: 1000
```

## **1.4 🔄 Function with Parameter and Return Value**

The most common function type: it takes specific **input parameters** and returns a **resultant value** after execution.

**Example**

```
fun add(a, b) {
    return a + b
}

Print(add(600, 80))

; Output: 680
```

## **2.🔑 Arguments in NISR Functions**

**Arguments** are the actual values passed to the function when it is called.

**2.1 **🥇** Positional Arguments**

The order of **arguments** matters. The **first value** passed corresponds to the **first parameter**, and so on.

**Example: **

```
fun multiply(a, b) {
    return a * b
}

result = multiply(100, 300) ; 100 goes to 'a', 300 goes to 'b'
Print(result)

; Output: 30000
```

**2.2 🎁 Default Arguments**

You can assign default values to **parameters**. If the caller does not provide a value for that parameter, **NISR** uses the **default**.

**Default parameters** make functions adaptable without overloading.

**Caution:** Default values are evaluated once at function definition.

**Example**

```
fun power(x, y = 2) {
    return x ** y

}

Print(power(10)) ; y uses default value 2. Output: 100

Print(power(10, 3)) ; y uses value 3. Output: 1000
```

## **2.3 🏷 Keyword Arguments**

The **caller** specifies which parameter receives which value by using the parameter name. The order of arguments does **NOT** matter.

• **Keyword arguments** make function calls self-documenting.

• Useful when functions have many optional parameters.

**Example**

```
fun div(x, y) {
    return x / y
}

Print(div(y = 2, x = 10)) ; Order is reversed, but the result is correc

; Output: 5
```

## **3. 🧩 Advanced Function Concepts**

## **3.1 **⬆** Higher-Order Functions**

You can pass **one function** into another as a **parameter**.

**Example**

```
fun add(x, y) {
    return x + y
}

fun operate(fun_name, x, y) {
    return fun_name(x, y)
}

result = operate(add, 10, 20)

Print(result)

; Output: 30
```

This is useful for **writing calculators**, **creating callbacks**, or **reusing logic** with different functions.

## **3.2 🏰 Nested Functions**

A **nested function** is defined inside another function. It is used to **encapsulate logic** or **create closures**.

**Example**

```
fun outer() {
    fun inner() {
        Print("Inner function called")
      }
      inner()
}

outer() ; Output: Inner function called

# inner() would not be accessible here
```

## **3.3 🔁 Recursion**

A **recursive function** calls itself. It must have a termination condition to avoid an **infinite loop**.

**Example: Factorial Calculation: **

```
fun factorial(n) {
    if n <= 1 {
       return 1
    }
    return n * factorial(n - 1)
}

print(factorial(5)) ; Output: 120

```

---

