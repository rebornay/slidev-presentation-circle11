<!-- ---
monaco: true
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Objects in Javascript
info: |
  ## Circle 11 Assignment
  Presentation slides on Javascript Objects.

# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: true
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev

 -->

# Javascript Objects

A presentation on what we've learnt so far on JS Objects


<!-- <div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div> -->

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Presentation Outline


- Introduction to Objects, and its syntax
- Assessing objects property
- Property value shorthand
- Reassigning values
- Objects.assign()
- Objects.entries()
- for-in loop
-conclusion
<br>
<br>

Read more about [Why Slidev?](https://sli.dev/guide/why)

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<!--<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>-->

<!--
Here is another comment.
-->

<!-- ---
transition: slide-up
level: 2 -->
---

# Introduction to Objects, and syntax

- A non-primitive datatype used to store keyed collections of various data and more complex entities. They are arranged in key-value pairs inside curly braces. 

This syntax is called object constuctor
```js {monaco}
let user = {
  firstName: "Jane",
  lastName: "Doe",
  age: 12,
  stack: "Frontend eng"
}
```
This syntax is called object literal
```js {monaco}
const user = new Object();
user.firstName = "Jane"
user.lastName = "Doe",
user.age = 12
user.stack = "Frontend eng"
```
Usually, the object constructor method is usually employed.
---

## Accessing properties in an object
Properties in a curly brace  can be accessed either using: 
1. The dot notation
```js
objectName.propertyName;
```

2. using sqaure brackets
```js
objectName["propertyName"]
```

### Property value shorthand
Sometimes, we use existing values for property name. Instead of repeating this we can implement the shorthand property.

```js
const getUser = (name, age) => {
  return {
    name: name,
    age: age,
  };
}
let user = getUser("Jane", 40);
alert(user.name);
```
this can be shortened to: 
```js
const getUser = (name, age) => {
  return {
    name,
    age,
  };
}
let user = getUser("Setemi", 40);
alert(user.age);
```
---

# Reassigning values
Indeed, like we've learnt that variables cannot be re-declared using const. However, there's a slight difference with objects. 
```js

const user = {
  name: "Jane Doe"
}

user.name = "John Doe";
alert(user.name); //John Doe
``` 
---

# Objects.assign()
Object.assign() is a built-in JavaScript method used to copy the values of all enumerable own properties from one or more source objects to a target object. It returns the modified target object.

Syntax: 
```js
Object.assign(target, ...sources)
```
- target: The object that will receive the properties.

- ...sources: One or more objects whose properties you want to copy to the target.

```js
const target = { a: 1 };
const source = { b: 2, c: 3 };

const result = Object.assign(target, source);

console.log(result); // { a: 1, b: 2, c: 3 }
console.log(target); // { a: 1, b: 2, c: 3 } — target is also changed
```

---

# Object.entries()
Object.entries() is a JavaScript method that returns an array of a given object's own enumerable string-keyed property [key, value] pairs.

Syntax
```js
Object.entries(obj)
```
It can be used to loop through an object: 
```js
const user = { name: 'Jane', age: 10 };

for (const [key, value] of Object.entries(user)) {
  console.log(`${key}: ${value}`);
}
// Output:
// name: Jane
// age: 10
```
---

# The for in loop
The for in loop can be sued to iterate over enumerabble string properties in an object. Example: 
```js
let user = {
  club: "Arsenal",
  alias: "Gunners",
  winningtheUCL: false
}

for (let key in user) {
  alert( key ); // club, alias, winningtheUCL
  console.log( user[key] ); // Arsenal, Gunners, false
}

---

# Conclusion

- JavaScript objects are a foundational part of the language; powerful, flexible, and essential for organizing and working with data. 
- While we’ve only scratched the surface, it’s clear that objects play a major role in everything from simple data structures to more advanced programming patterns.
- Apparently, I can’t cover everything we’ve explored this semester on JavaScript objects in just a few slides but, I’ve touched on some of the key concepts.
- From object creation to built-in methods like Object.assign() and Object.entries().
-  There’s still so much more to learn, but understanding the basics has given us a solid foundation to build on as we grow in our journey as world-class developers.

Thank you. 


