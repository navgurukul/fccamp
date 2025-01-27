---
id: 6754304d21779d7445490b1a
title: Collatz Sequence Generator
challengeType: 1
dashedName: collatz-sequence-generator
---

# --description--

**Introduction:**
The Collatz sequence is a mathematical sequence that demonstrates how a simple set of rules can lead to intriguing patterns. By applying different operations based on whether a number is odd or even, the sequence eventually converges to 1, no matter the starting number.
<br>

**Challenge:**
Write a program that generates the Collatz sequence for a given positive integer. Begin with the input number and apply the rules: divide by 2 if even, or multiply by 3 and add 1 if odd, continuing until the sequence reaches 1. Print each number in the sequence (Use positive integers only).
<br>

*Note:* 
Use `arr[arr.length]=value` to push elements at the end of array.

**Explanation:**
<br>

```js
// 7 is odd, so multiply by 3 and add 1 to get 22.

// 22 is even, so divide by 2 to get 11.

// 11 is odd, so multiply by 3 and add 1 to get 34.

// 34 is even, so divide by 2 to get 17.

// 17 is odd, so multiply by 3 and add 1 to get 52.

// 52 is even, so divide by 2 to get 26.

// 26 is even, so divide by 2 to get 13.

// 13 is odd, so multiply by 3 and add 1 to get 40.

// 40 is even, so divide by 2 to get 20.

// 20 is even, so divide by 2 to get 10.

// 10 is even, so divide by 2 to get 5.

// 5 is odd, so multiply by 3 and add 1 to get 16.

// 16 is even, so divide by 2 to get 8.

// 8 is even, so divide by 2 to get 4.

// 4 is even, so divide by 2 to get 2.

// 2 is even, so divide by 2 to get 1.

// The sequence ends as it reaches 1.

```

# --instructions--

Click on this <a target="_blank" href="https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `arr[arr.length]`  in your code to push elements at the end of array.

```js
assert(code.match(/arr[arr.length]/g));
```

`collatzSequenceGenerator(7)` should return `[7, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1]`

```js
assert(collatzSequenceGenerator(7), [7, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1])
```

`collatzSequenceGenerator(8)` should return `[8, 4, 2, 1]`

```js
assert(collatzSequenceGenerator(8), [8, 4, 2, 1])
```

`collatzSequenceGenerator(13)` should return `[13, 40, 20, 10, 5, 16, 8, 4, 2, 1]`

```js
assert(collatzSequenceGenerator(13), [13, 40, 20, 10, 5, 16, 8, 4, 2, 1])
```

`collatzSequenceGenerator(4)` should return `[4, 2, 1]`

```js
assert(collatzSequenceGenerator(4), [4, 2, 1])
```

`collatzSequenceGenerator(10)` should return `[10, 5, 16, 8, 4, 2, 1]`

```js
assert(collatzSequenceGenerator(10), [10, 5, 16, 8, 4, 2, 1])
```

`collatzSequenceGenerator(1)` should return `[1]`

```js
assert(collatzSequenceGenerator(1), [1])
```

`collatzSequenceGenerator(-1)` should return `"Please enter a positive integer`

```js
assert(collatzSequenceGenerator(-1), "Please enter a positive integer")
```

# --seed--
## --seed-contents--

```js
function collatzSequenceGenerator(num) {
  const arr=[];
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function collatzSequenceGenerator(num) {
  const arr=[]
  if (num <= 0) {
    return ("Please enter a positive integer");
  }
  arr[arr.length]=num
  while (num !== 1) {
    if (num % 2 === 0) {
      num = num / 2;
    } else {
      num = 3 * num + 1;
    }
    arr[arr.length]=num
  }
  return arr;
}
collatzSequenceGenerator(num)
```
