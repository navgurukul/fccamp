---
id: 674670da1cdfe3e7e9922e73
title: Classify Variable Data Types
challengeType: 1
dashedName: classify-variable-data-types
---

# --description--

**Introduction:**
In this challenge, we’ll practice identifying data types in JavaScript. Understanding the data type of a variable is crucial for writing efficient and error-free code. By analyzing the provided code snippet, you’ll determine the data type for each variable.
<br>
**Challenge:**
Identify the data type of each variable in the given code snippet. This exercise will help you sharpen your skills in recognizing and working with different data types in JavaScript.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`checkDataType(67)` should return `number`

```js
assert(checkDataType(67)==="number")

```

# --seed--
## --seed-contents--

```js
function checkDataType(a) {
    //  Only change code below this line
}
let age=67; //  Change this line
checkDataType(age)

```

# --solutions--

```js
function checkDataType(a) {
    let ans=typeof(a);
    return ans;
}
checkDataType(age)
```
