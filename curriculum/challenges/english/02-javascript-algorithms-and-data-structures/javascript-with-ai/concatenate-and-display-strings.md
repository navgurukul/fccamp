---
id: 67467befab007404086ee44e
title: Concatenate and Display Strings
challengeType: 1
dashedName: concatenate-and-display-strings
---

# --description--

**Introduction:**
In this challenge, you’ll write a simple program to concatenate two strings and print the result. String concatenation is a basic operation used to combine text in programming.
<br>
**Challenge:**
Create a program that concatenates two strings and displays the combined result.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `+` operator in your code to concatenate strings.

```js
assert(/\+/.test(__helpers.removeJSComments(code)));
```

`concatString("Hello"+"World")` should return `HelloWorld"

```js
assert(concatString("Hello","World")==="HelloWorld")
```

`concatString("Hello"+"  World")` should return `Hello  World"

```js
assert(concatString("Hello","  World")==="Hello  World")
```

`concatString("Hello"+"world")` should return `Helloworld"

```js
assert(concatString("Hello","world")==="Helloworld")
```

`concatString("Hello"+"123")` should return `Hello123"

```js
assert(concatString("Hello","123")==="Hello123")
```

# --seed--
## --seed-contents--

```js
function concatString(a,b) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function concatString(a,b) {
		let ans= a+b
		return ans;
}
concatString(a,b)
```
