---
id: 675430cce5ec2c746da638bc
title: Circular Array Rotation
challengeType: 1
dashedName: circular-array-rotation
---

# --description--

**Introduction:**
Rotating an array is a common operation in programming, especially in algorithms involving cyclic patterns. By rotating an array to the right, you shift its elements, but to maintain the array's structure, elements pushed off the end are reinserted at the beginning.
<br>

**Challenge:**
Write a program that rotates the elements of an array to the right by a given number of positions. The rotation should be circular, so elements moved off the end are placed back at the start. Implement this using a loop, without relying on built-in array rotation methods.

**Example:**
<br>
const inputArray1 = [1, 2, 3, 4, 5];
<br>
const rotationCount1 = 2;
<br>
const outputArray1 = rotateArray(inputArray1, rotationCount1);
<br>
console.log(outputArray1); // Output: [4, 5, 1, 2, 3]
<br>

**Explanation:**
<br>
Count = 1 // output [5,1,2,3,4]
<br>
Every number is shifted right and last element comes first
<br>
Count = 2 // output [4,5,1,2,3]
<br>
Every element is shifted right and last element comes at first position.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`circularRotation([1,2,3,4,5],1)` should return `[5,1,2,3,4]`

```js
assert.deepEqual(circularRotation([1,2,3,4,5],1), [5,1,2,3,4])
```

`circularRotation([1,2,3,4,5],2)` should return `[4,5,1,2,3]`

```js
assert.deepEqual(circularRotation([1,2,3,4,5],2), [4,5,1,2,3])
```

`circularRotation([1,2,3,4,5],5)` should return `[1,2,3,4,5]`

```js
assert.deepEqual(circularRotation([1,2,3,4,5],5), [1,2,3,4,5])
```

`circularRotation([1,2,3,4,5],10)` should return `[1,2,3,4,5]`

```js
assert.deepEqual(circularRotation([1,2,3,4,5],10), [1,2,3,4,5])
```

# --seed--
## --seed-contents--

```js
function circularRotation(arr,num) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function circularRotation(arr,num) {
  let n = arr.length;
  let rotationCount = num % n;
  let rotatedArr = new Array(n);
  for (let i = 0; i < n; i++) {
    rotatedArr[(i + rotationCount) % n] = arr[i];
  }
  return rotatedArr;
}
circularRotation(arr,num)
```
