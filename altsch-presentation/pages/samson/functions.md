# Functions 

Functions are blocks of code designed to perform specific tasks. They help keep code reusable, and organized. 
We write functions to avoid repeating code, allowing us to call them whenever needed. The concept of using a function after it has been declared is called `'calling a function'.`

# Ways of defining functions in JavaScript.

* Function Declaration

```ts {monaco-run} {autorun:false}
function getUserId() {
  let userId = "Dauda Samson";
  let course = "Software engineering";
  let school = "Altschool Africa";
  let team = "Circle 11";

  console.log(`Hello, my name is ${userId}, a ${course} student, of ${school}. I belong to the unique ${team}.`);
}getUserId();
```

* Function Expression, and
* Arrow Function. 
---

