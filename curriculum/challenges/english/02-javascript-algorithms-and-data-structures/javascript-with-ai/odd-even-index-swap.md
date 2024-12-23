---
id: 67543025063c7f741cac607e
title: Odd-Even Index Swap
challengeType: 1
dashedName: odd-even-index-swap
---

# --description--

**Introduction:**
Swapping elements in an array based on their indices is a common task in programming. Understanding how to manipulate array elements helps in solving various algorithmic problems efficiently.
<br>
**Challenge:**
Write a program that takes an array and swaps the elements at odd indices with the elements at the preceding even indices. This will strengthen your skills in array manipulation and indexing.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`oddEvenSwap([1,2,3,4,5,6,7])` should return `[2,1,4,3,6,5,7]`

```js
assert.deepEqual(oddEvenSwap([1,2,3,4,5,6,7]), [2,1,4,3,6,5,7])
```

`oddEvenSwap([1,2,3,4,50])` should return `[2,1,4,3,50]`

```js
assert.deepEqual(oddEvenSwap([1,2,3,4,50]), [2,1,4,3,50])
```

`oddEvenSwap([1,2,3,4,5,6])` should return `[2,1,4,3,6,5]`

```js
assert.deepEqual(oddEvenSwap([1,2,3,4,5,6]), [2,1,4,3,6,5])
```

`oddEvenSwap([1,2,3,4,5,5])` should return `[2,1,4,3,5,5]`

```js
assert.deepEqual(oddEvenSwap([1,2,3,4,5,5]), [2,1,4,3,5,5])
```

`oddEvenSwap([1,1,2,2,3,3,4,4])` should return `[1,1,2,2,3,3,4,4]`

```js
assert.deepEqual(oddEvenSwap([1,1,2,2,3,3,4,4]),[1,1,2,2,3,3,4,4])
```

`oddEvenSwap([1])` should return `[1]`

```js
assert.deepEqual(oddEvenSwap([1]), [1])
```

# --seed--
## --seed-contents--

```js
function oddEvenSwap(arr) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function oddEvenSwap(arr) {
  for (let i = 1; i < arr.length; i += 2) {
    [arr[i], arr[i - 1]] = [arr[i - 1], arr[i]];
  }
  return arr;
}
oddEvenSwap(arr)
```
