---
id: 677bbe94287556b6d3eedfda
title: Triangle Type Checker
challengeType: 1
dashedName: triangle-type-checker
---

# --description--

**Introduction:**
Determining the type of a triangle based on its side lengths helps in understanding geometric properties. This program will validate the triangle and classify it as Scalene, Isosceles, or Equilateral.
<br>

**Challenge:**
Write a program that takes the lengths of the sides of a triangle, checks if it forms a valid triangle, and then classifies it as Scalene, Isosceles, or Equilateral. If the triangle is not valid, print "Not a valid triangle." This will help you practice triangle properties and conditional logic.

**Example :**
<br>
Input:
<br>
let a = 5;
<br>
let b = 5;
<br>
let c = 5;
<br>
Output:
<br>
Equilateral Triangle

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`classifyTriangle(15,15,15)` should return `Equilateral Triangle`

```js
assert(classifyTriangle(15,15,15)==="Equilateral Triangle")
```

`classifyTriangle(7,5,3)` should return `Scalene Triangle`

```js
assert(classifyTriangle(7,5,3)==="Scalene Triangle")
```

`classifyTriangle(5,5,7)` should return `Isosceles Triangle`

```js
assert(classifyTriangle(5,5,7)==="Isosceles Triangle")
```

`classifyTriangle(9,2,4)` should return `Not a valid triangle`

```js
assert(classifyTriangle(9,2,4)==="Not a valid triangle")
```

`classifyTriangle(5,5,9)` should return `Isosceles Triangle`

```js
assert(classifyTriangle(5,5,9)==="Isosceles Triangle")
```

# --seed--
## --seed-contents--

```js
function classifyTriangle(a, b, c) {
  //  Only change code below this line
	return
}
```

# --solutions--

```js
function classifyTriangle(a, b, c) {
  // Step 1: Validate the triangle with combined condition
  // Check if any side is less than or equal to 0
  if (a <= 0 || b <= 0 || c <= 0) {
    return "Not a valid triangle";
  }
  // Check if the sum of any two sides is less than or equal to the third side
  if (a + b <= c || a + c <= b || b + c <= a) {
    return "Not a valid triangle";
  }
  // Step 2: Classify the triangle
  if (a === b && b === c) {
    return "Equilateral Triangle";
  } else if (a === b || b === c || a === c) {
    return "Isosceles Triangle";
  } else {
    return "Scalene Triangle";
  }
}
classifyTriangle(a, b, c)
```
