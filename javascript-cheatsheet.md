Here’s a clean, practical **JavaScript cheat sheet in Markdown** you can copy and use:

---

# 🟨 JavaScript Cheat Sheet

## 📌 Basics

```js
// Variables
let name = "John";
const age = 25;
var oldWay = true;

// Data Types
let str = "Hello";
let num = 42;
let bool = true;
let arr = [1, 2, 3];
let obj = { key: "value" };
let und;
let nul = null;
```

---

## 🔁 Control Flow

```js
// If / Else
if (age > 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

// Ternary
let result = age > 18 ? "Adult" : "Minor";

// Switch
switch (day) {
  case "Mon":
    break;
  default:
    break;
}
```

---

## 🔄 Loops

```js
for (let i = 0; i < 5; i++) {}

while (condition) {}

do {} while (condition);

// For...of (arrays)
for (let item of arr) {}

// For...in (objects)
for (let key in obj) {}
```

---

## 🧩 Functions

```js
// Function declaration
function greet(name) {
  return "Hello " + name;
}

// Arrow function
const greet2 = (name) => `Hello ${name}`;

// Default params
const sum = (a = 0, b = 0) => a + b;
```

---

## 📦 Arrays

```js
let arr = [1, 2, 3];

// Common methods
arr.push(4);
arr.pop();
arr.shift();
arr.unshift(0);

arr.map(x => x * 2);
arr.filter(x => x > 1);
arr.reduce((a, b) => a + b, 0);
```

---

## 🧱 Objects

```js
let user = {
  name: "John",
  age: 25,
  greet() {
    console.log("Hi!");
  }
};

// Access
user.name;
user["age"];
```

---

## 🧬 ES6+ Features

```js
// Destructuring
const { name, age } = user;
const [a, b] = arr;

// Spread
const newArr = [...arr];
const newObj = { ...user };

// Template literals
let msg = `Hello ${name}`;

// Optional chaining
user?.address?.city;
```

---

## ⏳ Async JavaScript

```js
// Promise
const fetchData = () =>
  new Promise((resolve, reject) => {
    resolve("Done");
  });

// Async/Await
async function getData() {
  try {
    let res = await fetchData();
  } catch (err) {}
}
```

---

## 🌐 Fetch API

```js
fetch("https://api.example.com")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));
```

---

## 🛠️ DOM Manipulation

```js
// Select
document.querySelector(".class");
document.getElementById("id");

// Modify
element.textContent = "Hello";
element.innerHTML = "<b>Hi</b>";

// Events
element.addEventListener("click", () => {
  console.log("Clicked");
});
```

---

## ⚠️ Error Handling

```js
try {
  throw new Error("Oops");
} catch (e) {
  console.error(e.message);
} finally {
  console.log("Done");
}
```

---

## 📚 Useful Shortcuts

```js
// Convert to number
Number("123");

// Convert to string
String(123);

// Check array
Array.isArray(arr);

// JSON
JSON.stringify(obj);
JSON.parse(str);
```

---

## 🧠 Tips

* `===` checks value **and** type
* Prefer `const` over `let` when possible
* Avoid `var`
* Use arrow functions for cleaner syntax
* Keep functions small and reusable

---
