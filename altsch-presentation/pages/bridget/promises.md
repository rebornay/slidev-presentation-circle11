---
layout: center
theme: default
class: my-theme

---

# Promises, Async/Await & Api

---

### Promises in JavaScript
#

```markdown

A Promise is an object that represents the result of an asynchronous operation. It may succeed or fail in the future.
## Promises uses two functions which are `resolve` and `reject` 

# Three States of a Promise

1. Pending – The operation hasn’t completed yet  
2. Fulfilled – The operation completed successfully  
3. Rejected – The operation failed

#

```

```js  {monaco-run}

const myPromise = new Promise((resolve, reject) => {
  const success = true
  if (success) {
    resolve("Operation successful!")
  } else {
    reject("Something went wrong!")
  }
})
myPromise
  .then(response => console.log(response))  
  .catch(error => console.log(error)) 

```

<style>
h2 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---

### Examples with **fetch** and **Promises**

The fetch() function returns a Promise. We can use .then() to handle a successful response and .catch() for errors.




```js 

fetch("https://jsonplaceholder.typicode.com/users")
  .then(response => response.json())
  .then(data => console.log("Users:", data))
  .catch(error => console.log("Error:", error))
  

```
 

### Async & Await in JavaScript
#

##### `async` and `await` are modern ways to handle asynchronous operations, built on top of Promises  but easier to read and write.
#


```js
async function showMessage() {
  const message = await Promise.resolve("Hello from Team 11!");
  console.log(message);
}

showMessage();

```

---


<style>
h3 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>


### Async/Await with fetch

This is a cleaner way to use `fetch` with async/await instead of chaining `.then()`



```js {monaco-run}

async function loadUsers() {
  try {
    const res = await fetch("https://jsonplaceholder.typicode.com/users")
    const users = await res.json()
    console.log(users)
  } catch (error) {
    console.error("Failed to load users")
  }
}

loadUsers()


```
---

### APIs in web development
An **API** (Application Programming Interface) allows different software systems to talk to each other. We use APIs to **send or receive data**, like getting users from a server or posting form data.

It acts like a **messenger** that takes your request, tells another system what you want, then brings the response back.
#

### API Methods (Actions)

APIs usually use **HTTP methods** to perform actions:

- `GET`: Fetch or retrieve data  
- `POST`: Send or create data  
- `PUT`: Update data  
- `DELETE`: Remove data

--- 

```js {monaco-run}

async function createPost() {
  try {
    const res = await fetch("https://jsonplaceholder.typicode.com/posts", {
      method: "POST",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify({
        title: "Team 11 Project",
        body: "This is our presentation content",
        userId: 1
      })
    })

    const result = await res.json()
    console.log("Post created:", result)
  } catch (error) {
    console.error("Failed to create post:", error)
  }
}

createPost()

```

