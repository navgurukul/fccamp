---
id: 675432474711c6768f52d67e
title: Multiply array Elements
challengeType: 1
dashedName: multiply-array-elements
---

# --description--

**Introduction:**
Using arrow functions for array operations is a common practice in JavaScript. This task involves creating a function that scales each element in an array by a specified factor.
<br>
**Challenge:**
Create an arrow function named multiplyByTwo that takes an array of numbers and returns a new array with each element multiplied by 2. This exercise will help you practice using arrow functions and array manipulation.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

**Example:**
<br>
Input: <br>
const numbers = [1, 2, 3, 4, 5]; <br>
<br>
Output: 
<br>
[2, 4, 6, 8, 10]

*Note:* 
Use `result[result.length]=value` to push elements at the end of array.

# --hints--

You should use `result[result.length]`  in your code to push elements at the end of array.

```js
assert(code.match(/result[result.length]/g));
```

`multiplyByTwo([1,2,3,4,5])` should return `[2,4,6,8,10]`

```js
assert.deepEqual(multiplyByTwo([1,2,3,4,5]), [2,4,6,8,10])
```

`multiplyByTwo([1,1,1,1])` should return `[2,2,2,2]`

```js
assert.deepEqual(multiplyByTwo([1,1,1,1]), [2,2,2,2])
```

`multiplyByTwo([10,20,30,40,50])` should return `[20,40,60,80,100]`

```js
assert.deepEqual(multiplyByTwo([10,20,30,40,50]), [20,40,60,80,100])
```

`multiplyByTwo([5,6,5,6])` should return `[10,12,10,12]`

```js
assert.deepEqual(multiplyByTwo([5,6,5,6]), [10,12,10,12])
```

`multiplyByTwo([2,6,8])` should return `[4,12,16]`

```js
assert.deepEqual(multiplyByTwo([2,6,8]), [4,12,16])
```

`multiplyByTwo([100,200,300])` should return `[200,400,600]`

```js
assert.deepEqual(multiplyByTwo([100,200,300]), [200,400,600])
```

# --seed--
## --seed-contents--

```js
const multiplyByTwo = arr => {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
const multiplyByTwo = arr => {
const result = [];
for (let i = 0; i < arr.length; i++) {
  result[result.length]=(arr[i] * 2);
}
return result;
}
multiplyByTwo(arr)
```
