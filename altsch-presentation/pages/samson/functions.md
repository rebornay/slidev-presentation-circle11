---
layout: center
theme: default
class: my-theme
--- 

# Functions in JavaScript
---

# Functions 

##### Functions are blocks of code designed to perform specific tasks. They help keep code reusable, and organized. 
##### We write functions to avoid repeating code, allowing us to call them whenever needed. The concept of using a function after it has been declared is called `'calling a function'.`
#

### Ways of defining functions in JavaScript.
#

* ####  Function Declaration

#### A function declaration defines a named function using the function keyword.

```js {monaco-run} {autorun:false}
function getUserId() {
  let userId = "Dauda Samson";
  let course = "Software engineering";
  let school = "Altschool Africa";
  let team = "Circle 11";

  console.log(`Hello, my name is ${userId}, a ${course} student, a ${school}. I belong to the unique ${team}.`);
}
getUserId();
```
---

# Function Expression 
#

A function expression assigns a function to a variable.

* #### The function has no name (anonymous), and It’s stored in the variable greet.

```js {monaco-run} {autorun:false} 
const greet = function greetFunc(name) {
  return `Hello, ${name}`;
};
console.log(greet("World!")); 
```
<br>

```js {monaco-run} {autorun:false} 
const getUserId = function() {
  let userId = "Dauda Samson";
  let course = "Software engineering";
  let school = "Altschool Africa";
  let team = "Circle 11";

  console.log(`Hello, my name is ${userId}, a ${course} student, of ${school}. I belong to the unique ${team}.`);
}; 
getUserId();
```

---

# Arrow Function

Arrow functions are a shorter way to write function expressions. They use =>

```js {monaco-run} {autorun:false} 
const getUserId = () => {
  let userId = "Dauda Samson";
  let course = "Software engineering";
  let school = "Altschool Africa";
  let team = "Circle 11";

  console.log(`Hello, my name is ${userId}, a ${course} student, of ${school}. I belong to the unique ${team}.`);
};
getUserId();
```

Even shorter if there's only one parameter and one return line:
```js {monaco-run} {autorun:false} 
const greet = name => `Hello, ${name}`;
console.log(greet("Sam"));
```

---

# Function Types Summary

| Style               | Hoisted | Short Syntax | `this` Binding |
|--------------------|---------|--------------|----------------|
| Function Declaration | ✅ Yes  | ❌ No         | ✅ Yes         |
| Function Expression  | ❌ No   | ❌ No         | ✅ Yes         |
| Arrow Function       | ❌ No   | ✅ Yes        | ❌ No          |

#

#### In JavaScript, function declarations are hoisted, so you can use them before they’re defined, but function expressions and arrow functions aren’t. Arrow functions use a shorter syntax and don’t have their own this—they inherit it from the parent scope. 

#

#### This makes them cleaner for simple tasks but tricky when working with objects. For example, using this.userId in a regular function gives "Dauda Samson", but in an arrow function, it might return undefined.
---

# What Are Parameters?

##### Parameters are placeholders for values that you pass into a function.  
##### They allow your function to work with dynamic input instead of hardcoded values.
#

```js {monaco-run} {autorun:false}
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Dauda"); // Output: Hello, Dauda!
```
### Multiple Parameters

##### You can pass more than one parameter into a function.

```js {monaco-run} {autorun:false}
function introduce(name, course) {
  console.log("My name is " + name + " and I study " + course + ".");
} 
introduce("Dauda Samson", "Software Engineering");
```

---

# Why Use Parameters?

Parameters make your functions:

- #### Reusable — you don’t have to rewrite the function for each new value
- #### Cleaner — reduces hardcoded duplication
- #### Flexible — lets the same function handle different inputs

<br>

# Callback Functions

#### A **callback function** is a function passed **as an argument** to another function and is **called (executed)** later inside that function.

They are often used when:
- ##### You want to run something **after** another task (e.g., after loading data)
- ##### You want to allow custom behavior inside a generic function

---

#  Example: Callback in Action

```ts {monaco-run} {autorun:false}
function greet(name, callback) {
  console.log("Hello, " + name + "!");
  callback(); // call the passed-in function
}

function sayBye() {
  console.log("Goodbye!");
}

greet("Dauda", sayBye);
```
