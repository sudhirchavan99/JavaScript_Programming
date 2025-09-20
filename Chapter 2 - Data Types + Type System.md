# 🎯 Chapter 2: Data Types + Type System
## 📖 Theory
### 📌 What are Data Types ❓
In JavaScript every value has a type.
These types define what kind of data is being stored a number, text, boolean, object etc.
There are two categories:
- **Primitive types:** Stored directly
- **Reference types:** Stored as memory references.
  
### 1.Primitive Types (immutable, stored by value)
- String → text ("Hello", 'JS')
- Number → all numbers (integers, decimals, NaN)
- Boolean → true or false
- Null → intentional absence of value (null)
- Undefined → declared but not assigned
- Symbol → unique identifier (Symbol ("id") )
- BigInt → very large integers (123n)
 
👉 Primitive values are compared by value, not reference.
<hr>

### 2.Reference Types (mutable, stored by reference)
- **Objects** → { name: "John", age: 25 }
- **Arrays** → [1, 2, 3] (special kind of object)
- **Functions** → function sayHi() {} (functions are objects too!)
  
👉 Reference values are compared by memory location, not value.
<hr>

### 3. Dynamic Typing
JavaScript is **dynamically typed** → variable type can change at runtime.
```js
let x = 10;  // number
x = "hello";  // now string
```
<hr>

### 4. typeof quirks
- typeof null → "object" ❌ (this is a historical bug in JS)
- typeof NaN → "number"
- typeof [] → "object" (arrays are objects)
- typeof function(){} → "function"
<hr>

### 5. Type Coercion
- == → loose equality → converts types before comparing.
- === → strict equality → compares type + value.
```js
"5" == 5   // true
"5" === 5  // false
```
<hr>

### 6. Truthy & Falsy values
- **Falsy values:** false, 0, "", null, undefined, NaN
- Everything else is **truthy** (e.g., "hello", 42, [ ], { } ).
<hr>

## 📝 Practical Example
```js

// Primitive
let str = "Hello"; // string
let num = 42;      // number
let isJS = true;   // boolean
let empty = null;  // null
let notAssigned;   // undefined
let sym = Symbol("id"); // symbol
let big = 9007199254740991n; // bigint

// Reference
let arr = [1, 2, 3];
let obj = { name: "Alice", age: 25 };
function greet() { return "Hi!"; }

console.log(typeof str);  // string
console.log(typeof arr);  // object
console.log(typeof greet);// function

// Dynamic typing
let x = 100;
console.log(typeof x); // number
x = "now I am string";
console.log(typeof x); // string

// typeof quirks
console.log(typeof null); // object (bug)
console.log(typeof NaN);  // number

// Type coercion
console.log("5" == 5);   // true (loose)
console.log("5" === 5);  // false (strict)

// Truthy / Falsy
if ("") console.log("truthy"); else console.log("falsy"); // falsy
if ([]) console.log("truthy"); else console.log("falsy"); // truthy

```
<hr>


## 📋 Summary

🔹 **Categories**
- Primitive Types (immutable, stored by value) → string, number, boolean, null, undefined, symbol, bigint
- Reference Types (mutable, stored by reference) → object, array, function
<hr>

🔹 **Key Concepts**
- Dynamic Typing → Variable type can change at runtime.
- typeof quirks:
  - typeof null → "object" (bug)
  - typeof NaN → "number"
  - typeof [] → "object"
  - typeof function(){} → "function"
<hr>

🔹 **Equality**
- == (loose) → does type coercion before compare.
- === (strict) → compares both type and value.
<hr>

🔹 **Truthy & Falsy**
- Falsy values: false, 0, "", null, undefined, NaN, 0n
- Truthy values: everything else ("hello", 42, [], {}, etc.)
<hr>
