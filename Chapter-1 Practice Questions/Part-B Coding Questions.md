# Part-B Coding Questions

### Q.1. What will be the output?
```js
var x = 5;
var x = 10;
console.log(x);
```
***Output:***
```js
10
```

### Q.2. What will be the output?
```js
let y = 15;
//let y = 20;
y = 25;
console.log(y);
```
***Outout:***
```js
25
```
### Q.3. What will happen?
```js
const z = 30;
z = 40;
console.log(z);
```
***Output:***
```js
// Uncaught TypeError: Assignment to constant variable.
```

### Q.4. Predict the output:
```js
if (true) {
  var a = "Hello";
  let b = "World";
}
console.log(a); // This can print but
console.log(b); // This will gives an error "ReferenceError: b is not defined"
```

### Q.5. Predict the output:
```js
function test() {
   var msg = "Inside function";
   console.log(msg);
}
test();
console.log(msg);
```
***Output:***
```js
// Uncaught ReferenceError: msg is not defined
```

### Q.6. Predict the output:
```js
console.log(num);
var num = 100;
```
***Output:***
```js
undefined
```

### Q.7. Predict the output
```js
console.log(age);
let age = 25;
```
***Output:***
```js
ReferenceError: Cannot access 'age' before initialization
```

### Q.8. Predict the output
```js
const PI = 3.14;
console.log(PI);
```
***Output:***
```js
3.14
```

### Q.9. Fix the error
```js
const city;
city = "Mumbai";
console.log(city);
```
***Correct Input:***
```js
const city = "Mumbai";
console.log(city);
```
***Output:***
```js
Mumbai
```

### Q.10. Write a small script:
- Create a variable for your name using let.
- Create a variable for your birth year using const.
- Create a variable for your current age using var.
- Print all three in the console.

```js
let name = "Sudhir";
const BirthYear = 1993;
var age = 31;
// print all variables
console.log(name);
console.log(BirthYear);
console.log(age);
```
***Output:***
```js
Sudhir
1993
31
```
