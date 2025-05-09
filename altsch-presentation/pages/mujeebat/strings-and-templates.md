---
layout: center
theme: default
class: my-theme

---

# String Concatenation and Template Literals 

---


### Understanding strings and concatenation

<div v-click>

Strings are a datatype and are any values written within quotes; double and single quotes.
</div>   

<div v-click>

### Code example 
```js
const a = 5;  // number
const b = '5'; // string
const c = true; // boolean
const d = "true"; // string
```
</div>  

---

# Console output
#

```
console.log (typeof a); // number
console.log (typeof b); // string
console.log (typeof c); // boolean
console.log (typeof d); // string
```

# Result (Click to reveal each one)

- <span v-click>typeof a: number</span>
- <span v-click>typeof b: string</span>
- <span v-click>typeof c: boolean</span>
- <span v-click>typeof d: string</span>

---

# Concatenation
<span v-click class="result-line">
Think concatenation, think <strong>Chains, Links, Hydrocarbons,</strong> join together. Like prepositions joining sentences.
The + operator is used for concatenation</span>


<span v-click class="result-line">

```js
const firstName = 'Mujeebah';
const nationality = "Nigerian";
console.log( 'my name is ' + firstName  + ", I’m " + nationality)
```
</span>

<span v-click>The + sign is also a mathematical operator and therefore has some weird quirks in some use case regarding numbers (5) and strings (‘5’)
</span>

---

# Concatenation cont’d
For example,

<div v-click>
```js
console.log (5+5) // would equal 10 however
console.log(5+’5’) //would equal 55 this is because of string concatenation 
```
</div>   

<div v-click>
```js
console.log (2+3+'5'+7) // would equal 557: 2+3=5, '5', + 7
// in cases like this, the values are converted to the number datatype
console.log (2+3+ Number('5')+7)
```
</div>

---

# Template literals


<ul>
<li v-click > For complex strings, template literals are used to write *complex strings in a more normal way. The variables are inserted straight into the strings instead of using the + operator </li>
<li v-click>
Back ticks(``) are used to write template literals </li>
<li v-click> To inserts variables in template literals, the dollar sign ($)along with curly braces {} is used.</li>

</ul>

<div v-click style="margin-top: 1rem;">
```js
Console.log (`My name is ${firstname}, I'm ${nationality}`)
```
</div>

---

# cont'd

## Code example

<div v-click style="margin-top: 1rem;">
```js
const country = 'Nigeria';
const continent = 'Africa';
const officialLanguage = 'English';
const population = 200; // in million
```
</div>

<div v-click style="margin-top: 1rem;">
String concatenation method 
```js
console.log (country + ' is in ' + continent + ' and its ' + population + ' million people speaks ' + language) ;
```
</div>
<div v-click style="margin-top: 1rem;">
Template literal method 
```js
console.log (`${country} is in ${continent} and its ${population} million people speak ${language}`); 
```
</div>


---
layout: center
theme: default
class: my-theme

---

# THANK YOU