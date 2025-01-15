---
id: 675434d476f9b77ab6afecee
title: String Transformer
challengeType: 1
dashedName: string-transformer
---

# --description--

**Introduction:**
Transforming strings by removing spaces and replacing characters enhances data processing. This task focuses on updating a string by trimming and character substitution.
<br>

**Challenge:**
Create a function updatedString(str, originalChar, replacedChar) that removes leading and trailing spaces from the input string, replaces all occurrences of originalChar with replacedChar, and returns the updated string.

*Note*
Use `.trim()` to delete leading and trailing spaces.

**Example:**
<br>
Input:
<br>
let str = " 	This#is#my#first##code	"	
<br>
let originalChar = “#”
<br>
let replacedChar = " "
<br>
Output: 
<br>
"This is my first code"

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.trim()`  in your code to remove trailing and starting whitespaces.

```js
assert(code.match(/.trim()/g));
```

`updatedString("    This#is#my#first#code    ","#"," ")` should return `This is my first code`

```js
assert(updatedString("    This#is#my#first#code    ","#"," ")==="This is my first code")
```

`updatedString(" I am a student","s","S")` should return `I am a Student`

```js
assert(updatedString(" I am a student","s","S")==="I am a Student")
```

`updatedString("    Password    ","s","$")` should return `Pa$$word`

```js
assert(updatedString("    Password    ","s","$")==="Pa$$word")
```

`updatedString("    i love coding    ","i","I")` should return `I love codIng`

```js
assert(updatedString("    i love coding    ","i","I")==="I love codIng")
```

# --seed--
## --seed-contents--

```js
function updatedString(str, originalChar, replacedChar) {
  // Only change code below this line
	return
}
```

# --solutions--

```js
// Function to update the string
function updatedString(str, originalChar, replacedChar) {
    // Step 1: Trim leading and trailing spaces
    let result = "";
	const trimmedString = str.trim();
    for (let i = 0; i < (trimmedString.length); i++) {
        if (trimmedString[i] === originalChar) {
            result += replacedChar; // Replace originalChar with replacedChar
        } else {
            result += trimmedString[i]; // Append the character as-is
        }
    }
    return result;
}
updatedString(str, originalChar,replacedChar);
```
