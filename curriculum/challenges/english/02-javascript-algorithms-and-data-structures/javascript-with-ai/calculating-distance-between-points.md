---
id: 67543664e6f1637c38f64936
title: Calculating Distance Between Points
challengeType: 1
dashedName: calculating-distance-between-points
---

# --description--

**Introduction:**
Imagine you’re trying to measure the straight-line distance between two locations on a 2D map, like finding out how far apart two cities are. To calculate this distance, we use the distance formula, which involves both squaring and taking the square root of the differences between the coordinates of the two points. In JavaScript, Math.sqrt() helps us find the square root, and Math.pow() allows us to raise numbers to a power.
<br>

**Challenge:**
Your challenge is to write a function getDistance that takes four numbers (x1, y1, x2, y2) as arguments representing two points on a 2D plane. The function should return the distance between these points using the distance formula.

*Note:* 
Use `Math.pow(number,power)` in your code to find the value of number raise to power. <br>
Use `Math.sqrt(number)` in your code to find the value of square root.

**Example:**
<br>
Input <br>
const x1 = 1; <br>
const y1 = 2; <br>
const x2 = 4; <br>
const y2 = 6; <br>
Output <br>
5

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `Math.pow`  in your code.

```js
assert(code.match(/Math.pow/g));
```

You should use `Math.sqrt`  in your code.

```js
assert(code.match(/Math.sqrt/g));
```

`getDistance(1,1,4,5)` should return `5`

```js
assert(getDistance(1,1,4,5)===5)
```

`getDistance(1,1,5,5)` should return `5.656854249492381`

```js
assert(getDistance(1,1,5,5)===5.656854249492381)
```

`getDistance(1,4,1,4)` should return `0`

```js
assert(getDistance(1,4,1,4)===0)
```

`getDistance(1,4,2,4)` should return `1`

```js
assert(getDistance(1,4,2,4)===1)
```

`getDistance(1,10,10,1)` should return `12.727922061357855`

```js
assert(getDistance(1,10,10,1)===12.727922061357855)
```

# --seed--
## --seed-contents--

```js
const getDistance = (x1, y1, x2, y2) => {
    //  Only change code below this line
    return
}
```

# --solutions--

```js
const getDistance = (x1, y1, x2, y2) => {
  const xDiff = x2 - x1;
  const yDiff = y2 - y1;
  const distance = Math.sqrt(Math.pow(xDiff, 2) + Math.pow(yDiff, 2));
  return distance;
}
getDistance(x1, y1, x2, y2)
```
