---
layout: center
---
# Arrays in JavaScript
<style>
  h1 {
    color: teal;
    font-size: 3rem;
  }
</style>

---

# What is an Array?
An **array** is an ordered collection of values, which can be of any data type, stored under a single variable name. 
Each value has a **numbered index**, starting from **0**.

```js
let fruits = ["apple", "pawpaw", "orange", "mango", "pineapple"];
fruits[0] // "apple"
fruits[4] // "pineapple"; 
```

<style>
    h1 {
        color: teal;
    }
</style>

---

# Common Array Methods & Properties
Some commonly used built-in array features include:
- **Array Property**: length - Returns the number of elements in an array.  
```js
  const fruits = ["apple", "banana", "mango"];
  console.log(fruits.length); // 3
```

- **Array Method**: push - Adds one or more elements to the end of an array.
```js
const nums = [1, 2];
nums.push(3);
console.log(nums); // [1, 2, 3]
```

- **Array Method**: pop - Removes the last element from an array. 
```js
const nums = [1, 2, 3];
nums.pop();
console.log(nums); // [1, 2]
```

<style>
 h1 {
    color: teal;
 }
</style>

---

# Contd.
- **Array Method**: shift - Removes the first element from an array.
```js
const nums = [1, 2, 3];
nums.shift();
console.log(nums); // [2, 3]
```

- **Array Method**: unshift - Adds one or more elements to the beginning of an array.  
```js
const nums = [2, 3];
nums.unshift(1);
console.log(nums); // [1, 2, 3]
```

- **Array Method**: map - Returns a new array by applying a function to each element. 
```js
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled); // [2, 4, 6]
```

<style>
    h1 {
        color: teal;
    }
</style>

---

# Contd. 
- **Array Method**: filter - Creates a new array with elements that match a condition.
```js
const nums = [1, 2, 3, 4];
const evens = nums.filter(n => n % 2 === 0);
console.log(evens); // [2, 4]
```

- **Array Method**: find - Returns the first element that matches a condition. 
```js
const users = [{id: 1}, {id: 2}];
const user = users.find(u => u.id === 2);
console.log(user); // {id: 2}
```

- **Array Method**: forEach - Executes a function for each array element (no return). 
```js
const nums = [1, 2, 3];
nums.forEach(n => console.log(n)); // 1 2 3
```

- **Array Method**: reduce - Reduces the array to a single value using a callback. 
```js
const nums = [1, 2, 3];
const total = nums.reduce((sum, n) => sum + n, 0);
console.log(total); // 6
```

<style>
    h1 {
        color: teal;
    }
</style>

---

# Contd.
- **Array Method**: includes - Checks if an array contains a specific value. 
```js
const fruits = ["apple", "banana"];
console.log(fruits.includes("banana")); // true
```

- **Array Method**: indexOf - Returns the first index of a value, or -1 if not found.
```js
const nums = [10, 20, 30];
console.log(nums.indexOf(20)); // 1
```

- **Array Method**: sort - Sorts the elements of an array in place as strings by default. Custom compare functions are needed for numeric sorting as seen in the example below;
```js
nums.sort((a, b) => a - b);
console.log(nums); // [2, 5, 10]
```

<style>
    h1 {
        color: teal;
    }
</style>

---

# Spread Operator with Arrays
The spread operator (...) lets you unpack or copy elements from arrays or objects.

```js
// Expanding an array
const fruits = ["apple", "orange"];
const allFruits = [...fruits, "banana", "mango"];
console.log(allFruits); // ["apple", "orange", "banana", "mango"]
```

<style>
    h1 {
        color: teal;
    }
</style>

---
layout: center
---

# JavaScript Bundle

<style>
    h1 {
        color: teal;
        font-size: 3rem;
    }
</>

---

## What is a JavaScript Bundle?


A **bundler** combines your JavaScript (and other assets) into fewer files—usually just one—so they load faster in the browser.

It improves performance by reducing file requests and optimizing the code for production.

It's created using tools like **Webpack**, **Vite**, or **Parcel** to make your code **smaller, faster, and easier to load** in the browser.

Webpack is the first genuine innovation in the bundler space. It enables performance optimization through advanced features like **lazy loading**, where non-essential resources are loaded only when required

```js
// Instead of loading many files...
// script1.js, script2.js, lib.js

// You load one bundle.js
```

<style>
    h2 {
        color: teal;
    }
</style>

---

## 🧩 Why Use JavaScript Bundles?

Bundlers are necessary because of the limitations of Native ES Modules in Browsers. 

Native ES Modules require full, direct file paths and only support JavaScript files.
They can’t resolve npm packages or import non-JS assets like images or styles.

```js
// Works only with full, direct file paths
import { add } from './utils/math.js'; // Named Import

// ❌ Doesn't work
import _ from 'lodash'; // Browser doesn't know how to resolve this

// ❌ Doesn't work
import image from './logo.png'; // Only works with a bundler
```
Bundlers make modern web development possible by bridging the gap between developer-friendly code and browser limitations.
They help manage assets like CSS, images, and fonts too.

<style>
    h2 {
        color: teal;
    }
</style>

---

# 🚀 Benefits of Bundlers

- 🔗 **Modularity** - Break your code into small, reusable pieces for better structure and maintainability.
- 📦 **Dependency Management** - Automatically resolves and bundles third-party packages and internal modules.
- ⚙️ **Code Optimization** - Minifies, tree-shakes, and compresses files to reduce bundle size and improve performance.
- 🖼️ **Asset Handling** - Import images, fonts, CSS, and more—just like JavaScript modules.
- ⏳ **Lazy Loading** - Loads only the code or assets needed at a given time to speed up initial load.

<style>
    h1 {
        color: teal;
    }
</style>

---