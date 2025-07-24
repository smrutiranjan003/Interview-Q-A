# JavaScript Interview: 100 Questions & Answers with Code Examples

## 📚 Q1–Q25

### 1. What is JavaScript?
JavaScript is a high-level, interpreted programming language used to create interactive effects within web browsers.

```js
console.log("Hello, JavaScript!");
```

---

### 2. Difference between `var`, `let`, and `const`?

* `var`: function-scoped, hoisted
* `let`: block-scoped, not hoisted
* `const`: block-scoped, cannot be reassigned

```js
var a = 10;
let b = 20;
const c = 30;
```

---

### 3. What are arrow functions?

Short syntax for functions; they don’t have their own `this`.

```js
const add = (x, y) => x + y;
```

---

### 4. What is a closure?

A function that retains access to variables from its outer lexical scope.

```js
function outer() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}
const counter = outer();
```

---

### 5. Difference between `==` and `===`?

* `==`: compares values with type coercion
* `===`: compares both value and type

```js
5 == "5"   // true
5 === "5"  // false
```

---

### 6. What is the DOM?

Document Object Model represents the page structure, allowing scripts to update content, style, and structure.

```js
document.getElementById("app").innerText = "Updated";
```

---

### 7. What is hoisting?

JavaScript moves variable and function declarations to the top of their scope before execution.

```js
console.log(a); // undefined
var a = 10;
```

---

### 8. What are template literals?

Strings enclosed in backticks allowing embedded expressions.

```js
let name = "Alice";
console.log(`Hello, ${name}`);
```

---

### 9. Difference between `undefined` and `null`?

* `undefined`: variable declared but not assigned
* `null`: intentional absence of value

```js
let a;
let b = null;
```

---

### 10. How does `setTimeout` work?

Schedules a function to execute after a specified delay.

```js
setTimeout(() => console.log("Hello"), 1000);
```

---

### 11. What are higher-order functions?

Functions that accept other functions as arguments or return them.

```js
function greet(fn) {
  return fn("John");
}
```

---

### 12. What is the use of `bind()`, `call()`, and `apply()`?

They set the value of `this` in functions.

```js
const obj = { name: "John" };
function sayHello() {
  console.log("Hello, " + this.name);
}
sayHello.call(obj);
```

---

### 13. What is event bubbling and capturing?

* Bubbling: event flows from child to parent
* Capturing: event flows from parent to child

```js
element.addEventListener("click", handler, true); // capturing
element.addEventListener("click", handler, false); // bubbling
```

---

### 14. What is the spread operator?

Expands arrays or objects into individual elements.

```js
let arr = [1, 2];
let newArr = [...arr, 3];
```

---

### 15. What is the rest operator?

Condenses multiple arguments into an array.

```js
function sum(...args) {
  return args.reduce((a, b) => a + b);
}
```

---

### 16. What are callback functions?

Functions passed as arguments and executed later.

```js
setTimeout(() => console.log("Done"), 1000);
```

---

### 17. Difference between synchronous and asynchronous?

* Synchronous: runs code sequentially
* Asynchronous: runs code in background without blocking

```js
console.log("Start");
setTimeout(() => console.log("Async"), 0);
console.log("End");
```

---

### 18. What is a Promise?

An object representing eventual completion or failure of an asynchronous operation.

```js
const promise = new Promise((resolve, reject) => {
  resolve("Success");
});
promise.then(console.log);
```

---

### 19. What is async/await?

Syntax to handle promises more elegantly with synchronous style code.

```js
async function fetchData() {
  const data = await fetch("url");
  return data;
}
```

---

### 20. Difference between `map()`, `forEach()`, and `filter()`?

* `map()`: transforms array and returns a new one
* `forEach()`: iterates but doesn’t return
* `filter()`: returns array of items meeting condition

```js
arr.map(x => x * 2);
arr.filter(x => x > 5);
```

---

### 21. What is an IIFE?

Immediately Invoked Function Expression; runs as soon as defined.

```js
(function() {
  console.log("IIFE");
})();
```

---

### 22. What is lexical scoping?

Scope determined by where variables/functions are defined, not where they are called.

```js
function outer() {
  let x = 10;
  function inner() {
    console.log(x);
  }
  inner();
}
```

---

### 23. What does the `this` keyword refer to?

The object from which the function was called.

```js
const obj = {
  name: "John",
  greet() {
    console.log(this.name);
  }
};
```

---

### 24. Difference between stack and heap?

* Stack: stores primitives and function calls (static memory)
* Heap: stores objects and closures (dynamic memory)

---

### 25. How to clone an object?

Use spread syntax or `Object.assign()`.

```js
const original = { a: 1 };
const copy = { ...original };
// or
const copy2 = Object.assign({}, original);
```

