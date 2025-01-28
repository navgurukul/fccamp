---
id: 6754319594cb16756e638f62
title: Skip Perfect Squares
challengeType: 1
dashedName: skip-perfect-squares
---

# --description--

**Introduction:**
This program focuses on filtering numbers within a range, specifically excluding perfect squares. It also introduces a condition to limit the range if a threshold is exceeded.
<br>
**Challenge:**
Write a program that prints numbers from 1 to N, skipping perfect squares. If N exceeds 20, limit the output to numbers up to 20. This exercise will help you practice conditional logic and range manipulation.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

**Example:**
Input:
<br>
29
<br>
Output: 
<br>
2 3 5 6 7 8 10 11 12 13 14 15 17 18 19 20

**Explanation:**

Skips 1, 4, 9  and 16 as they are perfect squares, and stops at 20

*Note:* 
Use `result[result.length]=value` to push elements at the end of array.

# --hints--

You should use `result[result.length]`  in your code to push elements at the end of array.

```js
assert(code.match(/result[result.length]/g));
```

`skipPerfectSquares(25)` should return `[2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20]`

```js
assert.deepEqual(skipPerfectSquares(28), [2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20])
```

`skipPerfectSquares(25)` should return `[2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20]`

```js
assert.deepEqual(skipPerfectSquares(25), [2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20])
```

`skipPerfectSquares(19)` should return `[2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19]`

```js
assert.deepEqual(skipPerfectSquares(19), [2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19])
```

`skipPerfectSquares(9)` should return `[2, 3, 5, 6, 7, 8]`

```js
assert.deepEqual(skipPerfectSquares(9), [2, 3, 5, 6, 7, 8])
```

`skipPerfectSquares(100)` should return `[2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20]`

```js
assert.deepEqual(skipPerfectSquares(100), [2, 3, 5, 6, 7, 8, 10, 11, 12, 13, 14, 15, 17, 18, 19, 20])
```

# --seed--
## --seed-contents--

```js
function skipPerfectSquares(num) {
    const result = [];
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function skipPerfectSquares(num) {
  const result = [];
  let limit = 20;
  if (num <= 20) {
    limit = num;
  }
  let j=1;
  for (let i = 1; i <= limit; i++) {
      if (j * j === i) {
        j++;
        continue;
      }else{
        result[result.length] = i
    }
  }
  return result;
}
skipPerfectSquares(num)
```
