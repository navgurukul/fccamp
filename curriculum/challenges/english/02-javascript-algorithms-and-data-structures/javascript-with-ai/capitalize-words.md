---
id: 675434ef1448267ad6ff9457
title: Capitalize Words
challengeType: 1
dashedName: capitalize-words
---

# --description--

**Introduction:**
Capitalizing the first letter of each word in a string enhances readability and presentation. This task involves creating a function to format strings into title case.
<br>

**Challenge:**
Create a function capitalizeWords(str) that capitalizes the first letter of each word in the input string and returns the updated string.

*Note:* 
Use `toUppercase()` in your code to change the alphabet to uppercase (in capital).

**Example:**
<br>
Input:
<br>
let str = "This is my first code"
<br>
Output:
<br>
"This Is My First Code"

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `toUppercase()`  in your code.

```js
assert(code.match(/toUpperCase()/g));
```

`capitalizeWords("this is my first code")` should return `This Is My First Code`

```js
assert(capitalizeWords("this is my first code")==="This Is My First Code")
```

`capitalizeWords("India")` should return `India`

```js
assert(capitalizeWords("India")==="India")
```

`capitalizeWords("welcome to the world of Computers")` should return `Welcome To The World Of Computers`

```js
assert(capitalizeWords("welcome to the world of Computers")==="Welcome To The World Of Computers")
```

`capitalizeWords("WELL DONE")` should return `WELL DONE`

```js
assert(capitalizeWords("WELL DONE")==="WELL DONE")
```

# --seed--
## --seed-contents--

```js
const capitalizeWords = (str) => {
    //  Only change code below this line
    return
}
```

# --solutions--

```js
const capitalizeWords = (str) => {
  let result = "";
  let capitalizeNext = true;
  for (let i = 0; i < str.length; i++) {
    let char = str[i];
    // Check if the current character is a space
    if (char === " ") {
      result += char; // Add the space to the result
      capitalizeNext = true; // Mark the next character for capitalization
    } else if (capitalizeNext && char >= "a" && char <= "z") {
      // Capitalize the first letter of the word
      result += char.toUpperCase() // ? char.toUpperCase() : char - ('a' - 'A');
      capitalizeNext = false; // Reset capitalization marker
    } else if (capitalizeNext && char >= "A" && char <= "Z"){
      result += char;
      capitalizeNext = false;
    }else {
      // Add the rest of the word as-is
      result += char;
    }
  }
return result;
}
capitalizeWords(str)
```
