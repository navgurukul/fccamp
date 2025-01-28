---
id: 67543315a0f4197822b69ef0
title: Flatten Nested Array
challengeType: 1
dashedName: flatten-nested-array
---

# --description--

**Introduction:**
Flattening a multi-dimensional array involves combining all nested elements into a single array. This task helps in practicing recursion and handling arrays of varying depths.
<br>

**Challenge:**
Write a recursive function flattenArray(arr) that takes a multi-dimensional array and returns a single flattened array with all elements combined. Ensure it handles arrays nested to any depth.
<br>

*Note:* 
Use `result[result.length]=value` to push elements at the end of array.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `result[result.length]`  in your code to push elements at the end of array.

```js
assert(code.match(/result[result.length]/g));
```

`flattenArray([1,2,3,[2],4,5,6])` should return `[1,2,3,2,4,5,6]`

```js
assert.deepEqual(flattenArray([1,2,3,[2],4,5,6]), [1,2,3,2,4,5,6])
```

`flattenArray([1,2,3,[]])` should return `[1,2,3]`

```js
assert.deepEqual(flattenArray([1,2,3,[]]), [1,2,3])
```

`flattenArray([1,2,3,[2],4,5,6,7,8])` should return `[1,2,3,2,4,5,6,7,8]`

```js
assert.deepEqual(flattenArray([1,2,3,[2],4,5,6,7,8]), [1,2,3,2,4,5,6,7,8])
```

`flattenArray([1,2,3])` should return `[1,2,3]`

```js
assert.deepEqual(flattenArray([1,2,3]), [1,2,3])
```

`flattenArray([1,2,3,[[],2]])` should return `[1,2,3,2]`

```js
assert.deepEqual(flattenArray([1,2,3,[[],2]]), [1,2,3,2])
```

# --seed--
## --seed-contents--

```js
const flattenArray = (arr) => {
    const result = [];
    //  Only change code below this line
    return result;
}
```

# --solutions--

```js
const flattenArray = (arr) => {
  const result = []; // Step 1
  for (let element of arr) { // Step 2
    if (typeof element === "object") { // Step 3a
      if (element !== null) { // Step 3b
          if (typeof element.length === "number") { // Step 3c
            const flattened = flattenArray(element); // Step 4
            for (let item of flattened) { // Step 5
              result[result.length] = item; // Step 6
            }
          }
      }
    } else { // Step 7
      result[result.length] = element; // Step 8
    }
  }
  return result; // Step 9
}
flattenArray(arr)
```
