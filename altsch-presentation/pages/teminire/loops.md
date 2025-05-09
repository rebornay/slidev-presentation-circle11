# 🔄 JavaScript Loops

Loops let you run the same block of code multiple times until a condition is met.

The **Four Main Loops** in JavaScript:

1. `while` loop
2. `for` loop
3. `for...in` loop
4. `for...of` loop

---

# 🔁 While Loop

Runs as long as the condition is true.

<span style="color:rgb(40, 141, 241); font-weight: bold">Example 1: Basic While Loop</span>

```js {monaco-run}
let i = 0;
while (i < 3) {
  console.log(i);
  i++;
}
```

This logs 0, 1, 2 to the console.
Once the condition `(i < 3)` becomes false, the loop ends.

---

<span style="color:rgb(241, 40, 60); font-weight: bold">Example 2: While Loop</span>

```js
const correctPassword = "temi123";
const attempts = ["wrong", "1234", "nire"];
let index = 0;
let input;

while (input !== correctPassword && index < attempts.length) {
  input = attempts[index];
  console.log(`Attempt ${index + 1}: ${input}`);
  index++;
}
```

This loop runs as long as the user hasn't entered the correct password `(input !== correctPassword)` there are still more attempts left in the array `(index < attempts.length)`. Inside the loop, The current input is taken from the array, the program logs which attempt it is and what the input was. The index increases so it can check the next attempt next time. However, once the correct password is input, the loop stops.

---

# 🔁 For Loop

This is used when the number of loops is known.

<span style="color:rgb(40, 141, 241); font-weight: bold">Example 1: Basic For Loop</span>

```js {monaco-run}
for (let i = 0; i < 3; i++) {
  console.log(i);
}
```

This logs `0, 1, 2` to the console.

---

<span style="color:rgb(241, 40, 60); font-weight: bold">Example 2</span>

```js {monaco-run}
const numbers = [12, 7, 22, 5, 9, 18];

for (let i = 0; i < numbers.length; i++) {
  const num = numbers[i];
  const type = num % 2 === 0 ? "even" : "odd";
  console.log(`${num} is ${type}`);
}
```

`for` loop is best when you know how many times you want to loop.
It has a built-in counter.

`while` loop is better when the number of iterations is unknown, and you loop based on a condition.

---

# 🔁 For...in Loop

This is used to loop through the properties of an object. It executes a block of code once for each property in the object.

<span style="color:rgb(40, 141, 241); font-weight: bold">Example 1: Basic For...in Loop</span>

```js {monaco-run}
const person = { name: "Oluwatiseteminire", age: 25 };

for (let key in person) {
  console.log(key, person[key]);
}
```

This will output name as "Oluwatiseteminire" and age as 25. Inside the loop, key will be "name" on the first loop, and "age" on the second.
`person[key]` will access the corresponding value: "Oluwatiseteminire" and 25.

---

<span style="color:rgb(241, 40, 60); font-weight: bold"> Example 2: Filtering only string-type values from an object</span>

```js {monaco-run}
const user = {
  name: "Oluwatiseteminire",
  age: 25,
  email: "teminire@gmail.com",
  verified: true,
};

for (let key in user) {
  if (typeof user[key] === "string") {
    console.log(`${key}: ${user[key]}`);
  }
}
```

The `for...in` loop goes through each property (key) in the user object. Inside the loop, it checks if the value of that property is a string. If it's a string like "Oluwatiseteminirere" or "teminire@gmail.com", it logs the key and value.

---

# 🔁 For...of Loop

This is used to loop through values in arrays, strings, and other iterables such as maps and sets.

<span style="color:rgb(40, 141, 241); font-weight: bold;">Example 1: Basic For...of Loop</span>

```js {monaco-run}
const states = ["Abuja", "Lagos", "Ogun"];

for (let state of states) {
  console.log(state);
}
```

This logs all states in the array to the console.

---

<span style="color:rgb(241, 40, 60); font-weight: bold"> Example 2: Looping through an array of objects</span>

```js {monaco-run}
const people = [
  { name: "Oluwatiseteminire", sign: "Gemini" },
  { name: "Ayomide", sign: "Taurus" },
  { name: "Victor", sign: "Scorpio" },
];

for (const person of people) {
  console.log(`${person.name} is a ${person.sign}`);
}
```

Each object in the `people` array has a name and sign. The loop prints each person’s name along with their zodiac sign.
