# Part-A Theory Questions
### Q.1. What is the difference between var, let, and const in JAvaScript?

**Difference between var, let, and const**

**Answer:**
- var → old way, function-scoped, allows redeclare + reassign.
- let → modern way, block-scoped, no redeclare, but reassign is allowed.
- const → block-scoped, no redeclare, no reassign (fixed value).

### Q.2. Which of the following is block-scoped?
- a) var
- b) let
- c) const
  
**Answer:** b) let and c) const are block-scoped.

### Q.3. Can a variable declared with const be reassigned? Why or why not?

**Answer:**

No, Once a const is assigned a value, it cannot be changed.

### Q.4. What happens if you redeclare a variable using let inside the same scope?
**Answer:**

It will throw an error because let does not allow redeclaration in the same scope.

### Q.5. Define function scope and give an example with var.
**Answer:**
Function scope means variables declared inside a function can only be used in that function.
```js
function test() {
   var msg = "Hello";
   console.log(msg); // It works
}
console.log(msg); // It gives an error
```

### Q.6. Define block scope and give an example with let or const.
**Answer:**
Block scope means variables declared inside { } can only be used inside that block.
```js
if (true) {
   let a = 10;
   const b = 20;
}
console.log(a); // error
```

### Q.7. Explain the Temporal Dead Zone (TDZ) in your own words.
**Answer:**
TDZ is the time between entering a scopeand declaring a variable with let or const. In that time, we can't use the variable → it gives an error.

### Q.8. What value is printed when you try to console.log(varVariable) before it is declared with var?
**Answer:**
It prints undefined because var is hoisted.

### Q.9. What will happen if you try to console.log(letVariable) before it is declared with let?
**Answer:**
It gives an error (ReferenceError) because let is in the Temporal Dead Zone.

### Q.10. Which one of the following declarations is correct?
- a) let 123name = "John";
- b) var myName = "John";
- c) const value;

**Answer:** b) var myName = "John"; - Correct ✅

a) is wrong because variable name can't start with a number.
c) is wrong because const must be initialized immediately.