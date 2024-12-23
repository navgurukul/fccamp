---
id: 67542fb29f51f57367dc7cd2
title: Party Entry Check
challengeType: 1
dashedName: party-entry-check
---

# --description--

**Introduction:**
In JavaScript, logical operators allow us to combine multiple conditions to make decisions. For example, determining if someone meets all the requirements to enter a private party—like having a valid ID, being of the right age, and having an invitation.
<br>
**Challenge:**
Write a JavaScript code snippet that checks if a person can enter a private party based on their valid ID, age, and invitation status. This will help you practice combining multiple conditions using logical operators.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `&&`  in your code to check multiple conditions together.

```js
assert(code.match(/&&/g))
```

`partyEntry(true,true,true)` should return `true`

```js
assert(partyEntry(true,true,true)===true)
```

`partyEntry(true,true,false)` should return `false`

```js
assert(partyEntry(true,true,false)===false)
```

`partyEntry(true,false,false)` should return `false`

```js
assert(partyEntry(true,false,false)===false)
```

`partyEntry(false,false,false)` should return `false`

```js
assert(partyEntry(false,false,false)===false)
```

`partyEntry(false,true,true)` should return `false`

```js
assert(partyEntry(false,true,true)===false)
```

# --seed--
## --seed-contents--

```js
function partyEntry(hasValidID, isAbove21, isInvited) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function partyEntry(hasValidID, isAbove21, isInvited) {
  let canEnter;
  if (hasValidID && isAbove21 && isInvited) {
    canEnter = true;
  } else {
    canEnter = false;
  }
  return canEnter;
}
partyEntry(hasValidID, isAbove21, isInvited)
```
