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
if (age > 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

let result = age > 18 ? "Adult" : "Minor";

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

// Arrays
for (let item of arr) {}

// Objects
for (let key in obj) {}
```

---

## 🧩 Functions

```js
function greet(name) {
  return "Hello " + name;
}

const greet2 = (name) => `Hello ${name}`;

const sum = (a = 0, b = 0) => a + b;
```

---

## 📦 Arrays

```js
let arr = [1, 2, 3];

arr.push(4);
arr.pop();
arr.shift();
arr.unshift(0);

arr.map(x => x * 2);
arr.filter(x => x > 1);
arr.reduce((a, b) => a + b, 0);

// Useful patterns
const unique = [...new Set(arr)];
const flat = arr.flat(2);
arr.sort((a, b) => a - b);
```

---

## 🔤 Strings

```js
const str = "hello";

str.length;
str.toUpperCase();
str.includes("he");

// Reverse
const reversed = str.split("").reverse().join("");

// Palindrome
const isPalindrome = s => s === s.split("").reverse().join("");
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

user.name;
user["age"];
```

---

## 🧬 ES6+ Features

```js
const { name, age } = user;
const [a, b] = arr;

const newArr = [...arr];
const newObj = { ...user };

let msg = `Hello ${name}`;

user?.address?.city;
```

---

## 🪟 Map & Set

```js
const map = new Map();
map.set("a", 1);
map.get("a");

const set = new Set([1, 2, 2, 3]);

const wm = new WeakMap();
```

---

## 🔒 Closures

```js
function counter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

const inc = counter();
```

---

## 🧭 this / call / apply / bind

```js
const person = {
  name: "John",
  greet() {
    console.log(this.name);
  }
};

const newPerson = { name: "Jane" };

person.greet.call(newPerson);
person.greet.apply(newPerson);

const bound = person.greet.bind(newPerson);
bound();
```

---

## 🧱 Classes

```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(this.name + " makes a noise");
  }
}

class Dog extends Animal {
  speak() {
    console.log(this.name + " barks");
  }
}
```

---

## ⏳ Async JavaScript

```js
const fetchData = () =>
  new Promise((resolve) => resolve("Done"));

async function getData() {
  try {
    let res = await fetchData();
  } catch (err) {}
}
```

---

## 🔁 Event Loop

```js
console.log("Start");

setTimeout(() => console.log("Timeout"), 0);

Promise.resolve().then(() => console.log("Promise"));

console.log("End");

// Output:
// Start → End → Promise → Timeout
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
document.querySelector(".class");
document.getElementById("id");

element.textContent = "Hello";
element.innerHTML = "<b>Hi</b>";

element.addEventListener("click", () => {
  console.log("Clicked");
});
```

---

## ⚡ Debounce & Throttle

```js
function debounce(fn, delay) {
  let timeout;
  return (...args) => {
    clearTimeout(timeout);
    timeout = setTimeout(() => fn(...args), delay);
  };
}

function throttle(fn, limit) {
  let inThrottle;
  return (...args) => {
    if (!inThrottle) {
      fn(...args);
      inThrottle = true;
      setTimeout(() => (inThrottle = false), limit);
    }
  };
}
```

---

## 📦 Modules

```js
export const name = "John";

import { name } from "./file.js";

export default function () {}
```

---

## 🧪 Utilities

```js
Number("123");
String(123);

Array.isArray(arr);

JSON.stringify(obj);
JSON.parse(str);

const deepCopy = structuredClone(obj);
```

---

## 💾 Storage

```js
localStorage.setItem("key", "value");
localStorage.getItem("key");
```

---

## 📅 Date

```js
const now = new Date();
now.toISOString();
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

## ❗ Common Gotchas

```js
[] == false        // true
[] === false       // false

typeof null        // "object"

NaN === NaN        // false
isNaN(NaN)         // true
```

---

## 🧠 Tips

* Use `===` instead of `==`
* Prefer `const` over `let`
* Avoid `var`
* Keep functions small
* Use meaningful variable names
* Learn async patterns deeply

---
