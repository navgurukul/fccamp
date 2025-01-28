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

You should use `typeof()`  in your code to check Data Type.

```js
assert(code.match(/typeof/g));
```

`checkDataType(67)` should return `number`

```js
assert(checkDataType(67)==="number")
```

`checkDataType("Hello")` should return `string`

```js
assert(checkDataType("Hello")==="string")
```

`checkDataType(true)` should return `boolean`

```js
assert(checkDataType(true)==="boolean")
```

`checkDataType([1,2,3])` should return `object`

```js
assert(checkDataType([1,2,3])==="object")
```

`checkDataType({name:"Rohan",age:23})` should return `object`

```js
assert(checkDataType({name:"Rohan",age:23})==="object")
```

`checkDataType()` should return `undefined`

```js
assert(checkDataType()==="undefined")
```

# --seed--
## --seed-contents--

```js
function checkDataType(a) {
    //  Only change code below this line
}
checkDataType();
```

# --solutions--

```js
function checkDataType(a) {
    let ans=typeof(a);
    return ans;
}
checkDataType(a)
```
