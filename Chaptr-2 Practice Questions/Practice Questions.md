### Q.1. Declare variables of all primitive types and log their types using typeof.

**Answer:**

```js
let str = "Hello";         // string
let num = 42;              // number
let isTrue = false;        // boolean
let empty = null;          // null
let notAssigned;           // undefined
let sym = Symbol("id");    // symbol
let big = 123456789n;      // bigint

console.log(typeof str);       // string
console.log(typeof num);       // number
console.log(typeof isTrue);    // boolean
console.log(typeof empty);     // object (quirk)
console.log(typeof notAssigned); // undefined
console.log(typeof sym);       // symbol
console.log(typeof big);       // bigint
```
<hr>

### Q.2. Create an object car with properties brand, model, and year. Print its type.

**Answer:**

```js
let car = { brand: "TATA", model: "Tata-Punch", year: 2024 };
console.log(typeof car);  // object
```
<hr>

### Q.3. Create an array of 5 fruits. Print its type and check if it's truthy.

**Answer:**

```js
let fruits = ["Apple", "Banana", "Mango", "Orange", "Grapes"];
console.log(typeof fruits); // object
if(fruits) console.log("Truthy");  // Truthy
```
<hr>

### Q.4. What will this log?
```js
console.log(typeof NaN);
```

**Answer:** Type of NaN is "number".
<hr>

### Q.5. Why does typeof null return "object"?

**Answer:**

Because of a historical bug in JavaScript. Null is not really an object, but typeof wrongly reports it as "object".
<hr>

### Q.6. Show an example where a variable changes its type (dynamic typing).

**Answer:**

```js
let x = 10 //number
x = "hello" // now string
```
<hr>

### Q.7. Compare "10" == 10 and "10" === 10. Explain results.

**Answer:**

- "10" == 10 → true (because == does type coercion).
- "10" === 10 → false (strict equality checks type also).

```js
console.log("10"==10); // true
console.log("10"===10); //false
```
<hr>

### Q.8. Which values are falsy in JavaScript? List them.

**Answer:**

- false
- 0
- ""
- null
- undefined
- NaN

<hr>

### Q.9. Predict output:
```js
if (0) console.log("yes");
else console.log("no");
```
**Answer:**

***Output:***
```js
no // because 0 is falsy
```
<hr>

### Q.10. Predict output:
```js
if (" ") console.log("truthy");
else console.log("falsy");
```
**Answer:**

**truthy** (non-empty string, even with space. is truthy).
<hr>

### Q.11. Create a function sayHello that returns "Hello JS". Print its type.

**Answer:**
```js
function sayHello() { return "Hello JS"; }
console.log(sayHello()); // Hello JS
console.log(typeof sayHello); // function
```
<hr>

### Q.12. Check if two different objects with the same values are equal using ==.

**Answer:**

```js
let obj1 = { car: "Hyundai" };
let obj2 = { car: "Hyundai" };
console.log(obj1 == obj2); // false (different memory reference)
```
<hr>

### Q.13. Predict output:
```js
console.log([] == false);
```

**Answer:** 
**true** (empty array converts to "", then 0, which equals false).
<hr>

### Q.14. Predict Output:
```js
console.log([1,2]=="1,2");
```
**Answer:**

**true** (array converts to string "1,2").
<hr>

### Q.15. Create a BigInt and try adding it with a normal number. What happens?

**Answer:**

```js
let big = 10n;
let num = 5;
// console.log(big + num); // ❌ TypeError: Cannot mix BigInt and number
```
<hr>

### Q.16. Use typeof on undefined.

**Answer:**
```js
console.log(typeof undefined);
```
The type of undefined is **undefined**
<hr>

### Q.17. Check if null == undefined and null === undefined.

**Answer:**
```js
console.log(null == undefined); // true
console.log(null === undefined); // false
```

- null == undefined → true (loose equality).
- null === undefined → false (different types).
<hr>

### Q.18. Wrire a condition that prints "Valid" if a variable is truthy.

**Answer:**
```js
let value = "Hello";
if (value) console.log("Valid"); // prints Valid
```
<hr>

### Q.19. Create an object student with name and age. Check its type with typeof.

**Answer:**
```js
let student = {name: "Sudhir", age: 31};
console.log(typeof student); // object
```
<hr>

### Q.20. Explain difference between primitive comparison and reference comparison with an example.

**Answer:**
```js
// Primitive
let a = 10, b = 10;
console.log(a == b); // true (values compared)

// Reference
let arr1 = [1,2];
let arr2 = [1,2];
console.log(arr1 == arr2); // false (different memory addresses)

```
<hr>
