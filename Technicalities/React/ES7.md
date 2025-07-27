# ⚡ ES6/ES7+ JavaScript Cheat Sheet

This cheat sheet covers essential and modern JavaScript features every dev should know, especially if you’re working with React, Node, or any serious frontend/backend JS stack.

---

<details>
<summary>📌 let / const (Block Scope)</summary>

```js
let count = 0;      // Mutable
const name = "Ali"; // Immutable (cannot reassign)

if (true) {
  let blockVar = "I exist only here";
}
```

</details>

---

<details>
<summary>🧲 Arrow Functions</summary>

```js
// Regular function
function sum(a, b) {
  return a + b;
}

// Arrow version
const sum = (a, b) => a + b;

// One-liner
const double = x => x * 2;
```

</details>

---

<details>
<summary>📦 Import / Export</summary>

```js
// Export
export const greet = () => console.log("Hey");

// Import
import { greet } from "./utils";
```

</details>

---

<details>
<summary>🔁 Spread / Rest Operator</summary>

```js
// Spread
const nums = [1, 2, 3];
const more = [...nums, 4];

// Rest
const add = (...args) => args.reduce((a, b) => a + b, 0);
```

</details>

---

<details>
<summary>🧱 Destructuring</summary>

```js
const person = { name: "Ali", age: 28 };
const { name, age } = person;

const arr = [1, 2, 3];
const [first, second] = arr;
```

</details>

---

<details>
<summary>🧪 Template Literals</summary>

```js
const name = "Ali";
const greet = `Hello, ${name}!`;
```

</details>

---

<details>
<summary>⚙️ Default + Named Parameters</summary>

```js
const greet = (name = "Stranger") => `Hi ${name}`;
```

</details>

---

<details>
<summary>🔐 Promises</summary>

```js
const fetchData = () =>
  new Promise((resolve, reject) => {
    setTimeout(() => resolve("Done!"), 1000);
  });

fetchData().then(console.log);
```

</details>

---

<details>
<summary>⏱ Async / Await</summary>

```js
const getData = async () => {
  const result = await fetchData();
  console.log(result);
};
```

</details>

---

<details>
<summary>🔁 for...of vs for...in</summary>

```js
const arr = [10, 20, 30];

// for...of (values)
for (let num of arr) console.log(num);

// for...in (indexes)
for (let i in arr) console.log(i);
```

</details>

---

<details>
<summary>🧰 Object Shorthand + Computed Props</summary>

```js
const age = 28;
const user = {
  name: "Ali",
  age, // shorthand
  ["user_" + age]: true, // computed
};
```

</details>

---

<details>
<summary>✅ Optional Chaining + Nullish Coalescing</summary>

```js
const user = { profile: null };

console.log(user?.profile?.name); // undefined, no crash
console.log(user.profile ?? "No profile"); // fallback if null/undefined
```

</details>

---

<details>
<summary>📚 Array Methods (map, filter, reduce)</summary>

```js
const nums = [1, 2, 3, 4];

nums.map(n => n * 2); // [2,4,6,8]
nums.filter(n => n % 2 === 0); // [2,4]
nums.reduce((a, b) => a + b, 0); // 10
```

</details>

---

<details>
<summary>🧩 Classes + Inheritance</summary>

```js
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks`);
  }
}
```

</details>

---

<details>
<summary>🧠 Useful One-Liners</summary>

```js
// Get unique items
const unique = [...new Set([1, 2, 2, 3])];

// Shuffle array
const shuffle = arr => arr.sort(() => Math.random() - 0.5);

// Clone object
const clone = obj => JSON.parse(JSON.stringify(obj));
```

</details>

---

> 🧙 Bonus Tip: Use Babel or TypeScript to ensure all modern syntax is supported across browsers.

---
> Written with 💻 and ☕ by [AKR]
