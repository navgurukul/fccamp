---
id: 67467bca43e34103c27b32c2
title: Compare and Clarify Data Types
challengeType: 1
dashedName: compare-and-clarify-data-types
---

# --description--

**Introduction:**
In this challenge, we’ll compare variables of different types in JavaScript to understand how type coercion affects results. We’ll also explore the difference between null and undefined to clarify their roles in JavaScript.
<br>
**Challenge:**
Compare variables of different types and explain the results. Additionally, understand the distinction between null and undefined.

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

```

# --solutions--

```js
function checkDataType(a) {
    let ans=typeof(a);
    return ans;
}
checkDataType(age)
```
