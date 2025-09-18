# 🎯 Chapter 1: Variables & Declarations
## 📖 Theory
### 1. var, let, const
- Var
   - Old way (before ES6)
   - Function-scoped (not block-scoped).
   - Allows **redeclaration** and **reassignment**.
   - Hoisted (moved to top) but initialized with undefined.

- let
   - Modern way (introduced in ES6).
   - Block-scoped ({ } matters).
   - Allows reassignment but not redeclaration.
   - Hoisted but inside Temporal Dead Zone (TDZ) → can’t access before declaration.

- const
   - Constant variable.
   - Block-scoped.
   - No redeclaration, no reassignment.
   - Hoisted but inside TDZ.
<hr>

### 2. Scope
- **Global Scope** → accessible anywhere.
- **Function Scope** → accessible only inside the function (var is function-scoped).
- **Block Scope** → accessible only inside { } (applies to let and const).
<hr>

### 3. Reassignment vs Redeclaration
- **Reassignment** → changing value.
- **Redeclaration** → declaring the same variable name again.
<hr>

### 4. Temporal Dead Zone (TDZ)
- Time between entering scope and declaring variable.
- Variables declared with let & const are hoisted but not usable until the declaration line.
<hr>

### 5. Hoisting
- var → hoisted and initialized as undefined.
- let / const → hoisted but not initialized (TDZ).
<hr>

## 💻 Practical Examples
```js
// var example
var x = 10;
var x = 20;  // redeclaration is allowed
console.log(x);   // Output: 20

// let example
let y = 15;
// let y = 25; //❌ Error: can't redeclare
y = 25; // ✅ reassignment allowed
console.log(y); // 25

// const example
const z = 30;
// z = 40; // ❌ Error: can't reassign
// const z = 50; // ❌ Error: can't redeclare
console.log(z);

// Scope
if (true) {
    var a = "var inside block";
    let b = "let inside block";
    const c = "const inside block";
}
console.log(a); // ✅ works, var is not block-scoped
// console.log(b); // ❌ Error
// console.log(c); // ❌ Error

// Hoisting
console.log(hoistVar); // undefined (var is hoisted)
var hoistVar = "I am var";

// console.log(hoistLet); // ❌ Error (TDZ)
let hoistLet = "I am let";

// console.log(hoistConst); // ❌ Error (TDZ)
const hoistConst = "I am const";

```
## 📝 Practice Tasks for You
### 1. Try declaring the same variable name with:
- var twice → what happens?
- let twice → what happens?
- const twice → what happens?
  
```js
// using var (redeclaration is allowed)
var a = 10;
var a = 20;
console.log("var redeclaration:",a);

// using let (redeclaration not allowed)
let b = 30;
let b = 40; // ❌ Error: Identifier 'b' has already been declared
b = 40; // reassignment allowed
console.log("let reassignment:", b);

// Using const (no redeclaration, no reassignment)
const c = 50;
// const c = 60; // ❌ Error: Identifier 'c' has already been declared
// c = 60;       // ❌ Error: Assignment to constant variable
console.log("const value:", c); // 50

```
***Output:***
```
var redeclaration: 20

let reassignment: 40

const value: 50

```

### 2. Write a function with a var inside it. Try to access it outside the function.

```js
function testFunction() {
    var message = "Hello from inside the function!";
    console.log(message); // work inside function
}
testFunction();
console.log(message); // ❌ Error: message is not defined (var is function-scoped)

```
***Output:***
```
Hello from inside the function!
```
### 3. Inside a block ({ }), declare variables with var, let, const.
- Check which ones you can access outside the block.

```js
if (true) {
    var x = "I am var inside block";
    let y = "I am let inside block";
    const z = "I am const inside block";

    console.log(x); // ✅ works
    console.log(y); // ✅ works inside block
    console.log(z); // ✅ works inside block
}

console.log(x); // ✅ works, var ignores block scope
console.log(y); // ❌ Error: y is not defined
console.log(z); // ❌ Error: z is not defined

```

### 4. Write a code to prove TDZ:
- Use console.log() before declaration for let and const.

```js
// TDZ Example with let
// console.log(myLet); // ❌ Error: Cannot access 'myLet' before initialization
let myLet = "I am let";

// TDZ Example with const
// console.log(myConst); // ❌ Error: Cannot access 'myConst' before initialization
const myConst = "I am const";

// Hoisting with var (works but gives undefined)
console.log(myVar); // ✅ undefined
var myVar = "I am var";
console.log(myVar); // "I am var"
```

## 📋 Summary
- var → Redeclare & reassign, function-scoped. hoisted as undefined.
- let → No redeclare, reassignment allowed, block-scoped, TDZ applies.
- const → No redeclare, no reassign, block-scoped, TDZ applies.
