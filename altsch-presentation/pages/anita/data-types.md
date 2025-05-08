## What are Data Types?

**Data types** specify what kind of data a variable holds.
- **Numbers**: represent *numeric values* for calculations.
They can be integers or floating-point numbers.
They are used in calculations like addition, subtraction, etc.

```js  
let age = 25;             // Integer  
let price = 19.99;        // Floating-point number  

console.log(age);         // 25  
console.log(price);       // 19.99  

```

Numeric operations
```js
let a = 10;  
let b = 3;  

console.log(a + b);   // 13 (addition) 
console.log(a - b);   // 7  (subtraction)
console.log(a * b);   // 30  (multiplication)
console.log(a / b);   // 3.333...  (division)
console.log(a % b);   // 1  (modulus - remainder)  
console.log(1 / 0);   // Infinity (result of dividing by zero) 
console.log("hello" - 5); // NaN (result of invalid operations)
```
---

## Data Types (Cont'd)




 - **Booleans**: The simplest data type for logic. They are represented by *true* or *false* values, often used for conditions.

 
```js
let isRaining = true;  
let hasHomework = false; 

//Boolean Expressions: Conditions
let age = 20;  
console.log(age >= 18);   // true  
//Logical operators
let isAdult = age >= 18;         // true  
let hasID = true;  

console.log(isAdult && hasID);   // true  
console.log(isAdult || false);   // true  
console.log(!isAdult);            // false  
//Numbers can be used in a Boolean context (truthy/falsy)
let count = 0;  
let score = 100;  
console.log(Boolean(score));   // true  

let temperature = 25;  

console.log(temperature <= 10);        // false  
```

