---
layout: center
theme: default
class: my-theme
---

# Arrays in JavaScript

---

# What is an Array?

An **array** is an ordered collection of values, which can be of any data type, stored under a single variable name.  
Each value has a **numbered index**, starting from **0**.

```js
const fruits = ["apple", "pawpaw", "orange", "mango", "pineapple"];
fruits[0]; // "apple"
fruits[4]; // "pineapple"
```

---

# Common Array Methods & Properties

<v-clicks>

- **Array Property**: `length` – Returns the number of elements in an array.
</v-clicks>

```js {1|2}
const fruitList = ["apple", "banana", "mango"];
console.log(fruitList.length); // 3
```

<v-clicks>

- **Array Method**: `push` – Adds one or more elements to the end.
</v-clicks>

```js {1|2|3}
const nums1 = [1, 2];
nums1.push(3);
console.log(nums1); // [1, 2, 3]
```

<v-clicks>

- **Array Method**: `pop` – Removes the last element.
</v-clicks>

```js {1|2|3}
const nums2 = [1, 2, 3];
nums2.pop();
console.log(nums2); // [1, 2]
```

---

# More Array Methods

<v-clicks>

- `shift` – Removes the first element from an array.
</v-clicks>

```js
const nums3 = [1, 2, 3];
nums3.shift();
console.log(nums3); // [2, 3]
```

<v-clicks>

- `unshift` – Adds elements to the beginning of an array.
</v-clicks>

```js
const nums4 = [2, 3];
nums4.unshift(1);
console.log(nums4); // [1, 2, 3]
```

<v-clicks>

- `map` – Transforms elements and returns a new array.
</v-clicks>

```js
const nums5 = [1, 2, 3];
const doubled = nums5.map(n => n * 2);
console.log(doubled); // [2, 4, 6]
```

---

# Even More Array Methods

<v-clicks>

- `filter` – Filters elements that meet a condition.
</v-clicks>

```js
const nums6 = [1, 2, 3, 4];
const evens = nums6.filter(n => n % 2 === 0);
console.log(evens); // [2, 4]
```

<v-clicks>

- `find` – Returns the first matching element.
</v-clicks>

```js
const users = [{id: 1}, {id: 2}];
const user = users.find(u => u.id === 2);
console.log(user); // {id: 2}
```

<v-clicks>

- `forEach` – Executes a function for each element.
</v-clicks>

```js
const nums7 = [1, 2, 3];
nums7.forEach(n => console.log(n)); // 1 2 3
```

<v-clicks>

- `reduce` – Reduces array to a single value.
</v-clicks>

```js
const nums8 = [1, 2, 3];
const total = nums8.reduce((sum, n) => sum + n, 0);
console.log(total); // 6
```

---

# Array Utility Methods

<v-clicks>

- `includes` – Checks for value existence.
</v-clicks>

```js
const fruitList = ["apple", "banana"];
console.log(fruitList.includes("banana")); // true
```

<v-clicks>

- `indexOf` – Returns index or -1 if not found.
</v-clicks>

```js
const nums9 = [10, 20, 30];
console.log(nums9.indexOf(20)); // 1
```

<v-clicks>

- `sort` – Sorts elements; use a compare function for numbers.
</v-clicks>

```js
const nums10 = [10, 5, 2];
nums10.sort((a, b) => a - b);
console.log(nums10); // [2, 5, 10]
```

---

# Spread Operator with Arrays

The spread operator `...` lets you unpack or copy elements.

```js
const fruits = ["apple", "orange"];
const allFruits = [...fruits, "banana", "mango"];
console.log(allFruits); // ["apple", "orange", "banana", "mango"]
```

---

# JavaScript Bundle

A **bundler** combines your JavaScript (and assets) into fewer files—usually just one.

It improves performance by reducing file requests and optimizing code.

Used tools: **Webpack**, **Vite**, **Parcel**, **Rollup**

```js
// Traditional way:
// <script src="script1.js"></script>
// <script src="script2.js"></script>

// With a bundler:
// <script src="bundle.js"></script>
```

---

# 🧩 Why Use JavaScript Bundles?

Bundlers solve limitations of native ES Modules in browsers.

<v-clicks>

- Native ESM requires full file paths and only supports `.js`
- Can’t load npm packages or non-JS files (like CSS/images)
</v-clicks>

```js
// ✅ Works
import { add } from './utils/math.js';

// ❌ Doesn't work in browser without a bundler
import _ from 'lodash';
import image from './logo.png';
```

---

# 🚀 Benefits of Bundlers

<v-clicks>

- 🔗 **Modularity** – Organize your code better
- 📦 **Dependency Management** – Handles third-party packages
- ⚙️ **Code Optimization** – Minify, tree-shake, compress
- 🖼️ **Asset Handling** – Import CSS, images, fonts
- ⏳ **Lazy Loading** – Load only what's needed
</v-clicks>