---
id: 67543537a33d657b1b9aa55f
title: String Compressor
challengeType: 1
dashedName: string-compressor
---

# --description--

**Introduction:**
Compressing a string by counting repeated characters can optimize storage and processing. This task involves creating a function to efficiently compress strings.
<br>

**Challenge:**
Implement the function compressString(str) that compresses the input string by replacing sequences of repeated characters with the character followed by its count, and returns the compressed string.

**Example:**
<br>
Test Case:
<br>
Input
<br>
"aabcccccaaa"
<br>
Output
<br>
"a2b1c5a3"

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`compressString("abcdef")` should return `a1b1c1d1e1f1`

```js
assert(compressString("abcdef")==="a1b1c1d1e1f1")
```

`compressString("aaaddddzacq")` should return `a3d4z1a1c1q1`

```js
assert(compressString("aaaddddzacq")==="a3d4z1a1c1q1")
```

`compressString("aaabccd")` should return `a3b1c2d1`

```js
assert(compressString("aaabccd")==="a3b1c2d1")
```

`compressString("zzzwxxxs")` should return `z3w1x3s1`

```js
assert(compressString("zzzwxxxs")==="z3w1x3s1")
```

`compressString("sssssss")` should return `s7`

```js
assert(compressString("sssssss")==="s7")
```

`compressString("aabcccccaaa")` should return `a2b1c5a3`

```js
assert(compressString("aabcccccaaa")==="a2b1c5a3")
```

# --seed--
## --seed-contents--

```js
function compressString(str) {
  // Only change code below this line
	return
}
```

# --solutions--

```js
function compressString(str) {
    // Step 1: Initialize an empty string for the result
    let compressedStr = "";
    let count = 1; // Variable to keep track of character repetition count
    // Step 2: Iterate through the string
    for (let i = 0; i < str.length; i++) {
        // If the next character is the same, increment the count
        if (str[i] === str[i + 1]) {
            count++;
        } else {
            // If the next character is different or it's the end of the string, append current char and count to the result
            compressedStr += str[i] + count;
            count = 1; // Reset count for the next character
        }
    }
    return compressedStr; // Return the compressed string
}
compressString()
```
