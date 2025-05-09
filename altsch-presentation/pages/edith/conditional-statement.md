---
layout: center
theme: default
class: my-theme

---

# Conditional Statement

---

# Conditional Statements
Ever heard of **conditionals**?

### What are Conditional Statements ?
Conditional Statements are a fundamental concept in programming that allows one to execute different blocks of code based on specific conditions, agreements or decisions.
these helps programs to adapt to different situations, make decisions, and respond accordingly.

##### Types of Conditional Statements
conditional statements exists in several types, they include;

1. **If**
2. **If-else**
3. **If-else if-else**
4. **Switch**
5. **Nested if**

---

# if Conditional Statement
This statement exutes a block of code if a certain condition is true but skips or ignores the block of code if the condition is false.
Different if statements includes;
 a **simple** if statement.
 an if statement with a **false condition**.
 an if statement with **variable condition**.
the if statement follows a syntax thus;

```js
if (condition) {
    // block of code(s) to be executed
}
```

# code sample

```js
let edith = 'female';
if (edith === 'female') {
    console.log('Edith is a lady.');
}
```

---

# if-else Conditional 
The **if-else statement** is a fundamental control structure in programming which executes different blocks of codes based on conditions, i.e one block of code is executed if condition is true, and another block if its false.
It follows this syntax;

```js
if (condition) {
    // code to be excuted if condition is true
} else {
    //code to execute if condition is true
}
```

#  Code example

```js
let edith = 'lady';
if (edith === 'lady') {
    console.log('Edith will join the ladys team.');
} else {
    console.log('Edith will not join the ladys team.');
}
```

---

# How it works
#

1. **edith** was declared as a variable and the value **lady** was assigned to it.
2. The if statement checks whether **edith** is equal to **lady**.
3. Since **edith** is equal to **lady**, the condition is true and the code inside the if block is executed and thereby logs **Edith will join the ladys team** to the console.
4. If the condition is false, the code inside the else block will be executed.

---

# if-else if-else
 This statement checks **multiple conditions** and executes different blocks of code accordingly.
  syntax;

  ```js
 if (condition1) {
    // code to be executed if condition1 is true
 } else if (condition2) {
    //code to be executed if condition1 is false and condition2 is true
 } else {
    // code to execute if all conditions are false
 }
 ```

# code sample

```js
 let edith = 'lady';
 if (edith === 'lady') {
    console.log('edith joined the ladys team.');
 } else if (edith === 'man') {
    console.log('edith joined the mens team.');
 } else {
    console.log('edith has no team.');
 }
 ```

---

# code explanation
The **if-else if-else** statement was used to check the value of edith. 
Since the first condition was true, the block of code associated with it was executed, which logs edith joined the ladys team to the console.
Therefore, the code blocks associated with the else if and else clauses doesnt execute .

---

 ### Nested if conditional statement
##### The **nested if** statement evaluates conditions hierarchically. It consists of an **outer if** statement and one or more inner if statements, its syntax is as follows;
 
 # 
```js
if (condition1) {
    if (condition2) {
        // code to execute if both condition1 and condition2 are true
    } else {
        // code to execute if condition1 is true but condition 2 is false
    } else {
        // code to execute if condition1 is false
    }
 }
 ```


#### sample code

```js
 let edith = 'lady';
 let age = 20;
 if (edith ==='lady') {
    if ( age >= 18) {
        console.log('edith is a lady and also an adult.');
    }
    else {
        console.log('edith is a lady but is not an adult.');
    } else {
        console.log('edith is not a lady.');
    }
 }
 ```

---

# Code explanation
##### Here, two variables **edith** and **age** were assigned values **lady** and **20** respectively.  while the nested if statement was used to evaluate the conditions **hierarchically**, the **outer if** statement checked whether edith was **equal** to lady. since  the condition was true, we moved on to the **inner if** statement.the inner if statement checked whether **age** is **greater than or equal** to **18**, since the condition is also true, the code block associated with it was executed which logged **edith is a lady and also an adult to the console**. The code blocks associated with the else clauses were not executed because the outer and inner if statements were **true**

 #

### Switch Statements
##### The javascript **switch statement** is a control structure that allows the execution of different blocks of code based on the **case value of a variable or expression** .It is a more concise and readable alternative to using **multiple if-else statements**, it follows the syntax below;
  
   ```js
   switch (expression) {
    case value1:
    // code to execute if expression equals value1
     break;
     case value2:
    // code to execute if expression equals value2
     break;
     default:
     // code to execute if expression does not equal any of the values
   }
```


---

## Code Example 
```js
    let setemi = 'instructor';
    switch (setemi) {
        case 'instructor':
        console.log('setemi is an instructor.');
        break;
        case 'student':
        console.log('setemi is a student.');
        break;
        default:
        console.log('setemi is neither an instructor nor a student.');
    }
   ```

---



# How the code example works
*  we declare a variable setemi and assign it the value instructor.
* we use the switch statement to evaluate the value of setemi.
* the swith statement checks whether setemi equals instructor.
since this condition is true, we execute the block of code associated with it which logs setemi is an instructor to the console.
* the break statement is used to exit the switch block and prevent the code from falling or sliding through to the next case.
* if setemi did not equal any of the values specified in the case statements, the code block associated with the default statement would be executed.

---


# SUMMARY
Conditional statements helps in decision-making, error-handling, logic and lots more.
## Characteristics
1. conditional execution
 2. alternative execution
 3. flexibility, etc.
    while working with conditional statements, it necessary to;
- keep it simple
- test thoroughly
- use wisely.

