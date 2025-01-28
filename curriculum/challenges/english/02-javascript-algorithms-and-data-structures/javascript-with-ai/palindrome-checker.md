---
id: 675435227cdba57af28d69ed
title: Palindrome Checker
challengeType: 1
dashedName: palindrome-checker
---

# --description--

**Introduction:**
Determining if a string is a palindrome is a common problem in text processing. This task involves creating a function that ignores spaces, special characters, and case to accurately check for palindromes.
<br>

**Challenge:**
Create a function isPalindrome(str) that checks if the input string is a palindrome, disregarding spaces, special characters, and case, and returns true if it is a palindrome and false otherwise.

*Note:* 
Use `toLowercase()` in your code to change the alphabet to Lowercase (in small).

**Example:**
<br>
Test Case:
<br>
Input
<br>
"A man a plan a canal, PAnama"
<br>
Output
<br>
True

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `toLowerCase()`  in your code.

```js
assert(code.match(/toLowerCase()/g));
```

`isPalindrome("A man a plan a canal, PAnama")` should return `true`

```js
assert(isPalindrome("A man a plan a canal, PAnama")===true)
```

`isPalindrome("Do geese see god")` should return `true`

```js
assert(isPalindrome("Do geese see god")===true)
```

`isPalindrome("Too hot to hoots")` should return `false`

```js
assert(isPalindrome("Too hot to hoots")===false)
```

`isPalindrome("No, it is0open4on one position")` should return `true`

```js
assert(isPalindrome("No, it is0open4on one position")===true)
```

`isPalindrome("Was it a car or a cat I saw? 2")` should return `true`

```js
assert(isPalindrome("Was it a car or a cat I saw? 2")===true)
```

`isPalindrome("Mr. Owl ate my metal worm")` should return `true`

```js
assert(isPalindrome("Mr. Owl ate my metal worm")===true)
```

# --seed--
## --seed-contents--

```js
function isPalindrome(str) {
  // Only change code below this line
	return
}
```

# --solutions--

```js
function isPalindrome(str) {
    let cleanedStr = ""; // Initialize an empty string for the cleaned version
    // Step 1: Clean the string
    for (let i = 0; i < str.length; i++) {
        let char = str[i].toLowerCase();
        if (char >= 'a' && char <= 'z') {
            cleanedStr += char; // Add only alphanumeric characters in lowercase
        }
    }
    // Step 2: Check if the cleaned string is a palindrome
    let start = 0;
    let end = cleanedStr.length - 1;
    while (start < end) {
        if (cleanedStr[start] !== cleanedStr[end]) {
            return false; // If characters don't match, it's not a palindrome
        }
        start++;
        end--;
    }
    return true; // If all characters match, it's a palindrome
}
isPalindrome()
```
