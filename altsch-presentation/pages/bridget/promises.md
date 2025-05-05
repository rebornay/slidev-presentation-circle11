## Promises

```markdown

A Promise is an object that represents the result of an asynchronous operation. It may succeed or fail in the future.

# Three States of a Promise

1. Pending – The operation hasn’t completed yet  
2. Fulfilled – The operation completed successfully  
3. Rejected – The operation failed

## Promise Structure
A promise uses two functions:
- `resolve` - Success hnadler
- `reject` - Error hnadler

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






---

# Async and Await



<!--#### `slides.md`

```markdown
# 

Page 2 from main entry.

---

## src: ./subpage.md
```

<br>

#### `subpage.md`

```markdown
# Page 2

Page 2 from another file.
``` -->
