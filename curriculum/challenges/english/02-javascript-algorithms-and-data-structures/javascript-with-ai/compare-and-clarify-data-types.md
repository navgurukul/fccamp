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
Compare variables of different types and explain the results.

# --instructions--

Click on this <a target="_blank" href="https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `==`  in your code to check Data Type.

```js
assert(code.match(/==/g))
```

You should use `===`  in your code to check Data Type.

```js
assert(code.match(/===/g))
```

`isEqual(10,10)` should return `true` for `a==b`

```js
assert(isEqual(10,10)===true)
```

`isStrictEqual(10,10)` should return `true` for `a===b`

```js
assert(isStrictEqual(10,10)===true)
```

`isEqual(10,"10")` should return `true` for `a==b`

```js
assert(isEqual(10,"10")===true)
```

`isStrictEqual(10,"10")` should return `false` for `a===b`

```js
assert(isStrictEqual(10,"10")===false)
```

# --seed--
## --seed-contents--

```js
function isEqual(a,b) {
	//  Only change code below this line
	return
}
function isStrictEqual(a,b) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function isEqual(a,b) {
		let ans=(a==b);
		return ans;
}
function isStrictEqual(a,b) {
		let ans1=(a===b);
		return ans1;
}
isEqual(10,10)
isStrictEqual(10,10)
```
