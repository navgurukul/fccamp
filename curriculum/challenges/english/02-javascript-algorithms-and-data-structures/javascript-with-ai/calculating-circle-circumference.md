---
id: 6754363dcd601a7c0c8bfbe7
title: Calculating Circle Circumference
challengeType: 1
dashedName: calculating-circle-circumference
---

# --description--

**Introduction:**
Imagine you have a perfectly round pizza, and you want to measure the distance around its edge to order the right amount of crust. In geometry, this distance is known as the circumference. To calculate it, we use the formula C=2πrC=2πr, where rr is the radius of the circle. In JavaScript, the Math object provides us with Math.PI, a constant that represents the value of π (Pi). By combining Math.PI with the radius, we can easily find the circumference of any circle.
<br>

**Challenge:**
Your challenge is to write a function getCircumference that takes the radius (in cm) of a circle as an argument and returns its circumference. Use Math.PI to calculate the result. Finally, print the circumference.

*Note:* 
Use `Math.PI(number,power)` in your code to get the constant value of Pi.

**Example:**
Input <br>
const radius = 5; <br>
Output <br>
31.415926535898

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `Math.PI`  in your code.

```js
assert(code.match(/Math.PI/g));
```

`getCircumference(5)` should return `31.41592653589793`

```js
assert(getCircumference(5)===31.41592653589793)
```

`getCircumference(1)` should return `6.283185307179586`

```js
assert(getCircumference(1)===6.283185307179586)
```

`getCircumference(2.5)` should return `15.707963267948966`

```js
assert(getCircumference(2.5)===15.707963267948966)
```

`getCircumference(3)` should return `18.84955592153876`

```js
assert(getCircumference(3)===18.84955592153876)
```

`getCircumference(3.5)` should return `21.991148575128552`

```js
assert(getCircumference(3.5)===21.991148575128552)
```

`getCircumference(10)` should return `62.83185307179586`

```js
assert(getCircumference(10)===62.83185307179586)
```

# --seed--
## --seed-contents--

```js
const getCircumference = (radius) => {
    //  Only change code below this line
    return
}
```

# --solutions--

```js
const getCircumference = (radius) => {
  const circumference = 2 * Math.PI * radius; // Formula for circumference: C = 2 * π * r
  return circumference;
}
getCircumference(radius)
```
