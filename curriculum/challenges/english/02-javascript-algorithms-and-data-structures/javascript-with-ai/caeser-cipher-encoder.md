---
id: 67543567604c727b38807d19
title: Caeser Cipher Encoder
challengeType: 1
dashedName: caeser-cipher-encoder
---

# --description--

**Introduction:**
The Caesar cipher is a classic encryption technique that shifts letters in the alphabet to encode messages. This task involves implementing a function to encrypt a string using this method.
<br>

**Challenge:**
Create the function caesarCipher(str, shift) that encrypts the input string by shifting each letter by the specified number of positions down the alphabet. The function should return the encrypted string.

**Example:**
<br>
Test Case:
<br>
Input:
<br>
"hello"
<br>
shift
<br>
1
<br>
Output
<br>
"ifmmp"

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`caesarCipher("I am a student",2)` should return `K co c uvwfgpv`

```js
assert(caesarCipher("I am a student",2)==="K co c uvwfgpv")
```

`caesarCipher("You got it right",3)` should return `Brx jrw lw uljkw`

```js
assert(caesarCipher("You got it right",3)==="Brx jrw lw uljkw")
```

`caesarCipher("Let's find out",4)` should return `Pix'w jmrh syx`

```js
assert(caesarCipher("Let's find out",4)==="Pix'w jmrh syx")
```

`caesarCipher("This is a random text",5)` should return `Ymnx nx f wfsitr yjcy`

```js
assert(caesarCipher("This is a random text",5)==="Ymnx nx f wfsitr yjcy")
```

`caesarCipher("stars",0)` should return `stars`

```js
assert(caesarCipher("stars",0)==="stars")
```

# --seed--
## --seed-contents--

```js
const caesarCipher = (str, shift) => {
    const lowerAlphabet = "abcdefghijklmnopqrstuvwxyz";
    const upperAlphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    //  Only change code below this line
    return
}
```

# --solutions--

```js
const caesarCipher = (str, shift) => {
  const lowerAlphabet = "abcdefghijklmnopqrstuvwxyz"; // Lowercase alphabet
  const upperAlphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"; // Uppercase alphabet
  let encrypted = ""; // To store the result
  for (let char of str) {
    let found = false; // Flag to check if character is found
    for (let i = 0; i < lowerAlphabet.length; i++) {
      if (char === lowerAlphabet[i]) {
        let newIndex = (i + shift) % 26; // Calculate the new index
        encrypted += lowerAlphabet[newIndex];
        found = true; // Set flag to true
        break; // Exit the loop
      }
    }
    if (found !== true) { // If character is not found in lowercase alphabet
      for (let i = 0; i < upperAlphabet.length; i++) {
        if (char === upperAlphabet[i]) {
          let newIndex = (i + shift) % 26; // Calculate the new index
          encrypted += upperAlphabet[newIndex];
          found = true; // Set flag to true
          break; // Exit the loop
        }
      }
    }
    if (found !== true) { // If character is not found in either alphabet
      encrypted += char; // Add the character as it is
    }
  }
  return encrypted;
}
caesarCipher(str, shift)
```
