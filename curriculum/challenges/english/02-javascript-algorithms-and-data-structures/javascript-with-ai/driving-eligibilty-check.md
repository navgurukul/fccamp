---
id: 67542f94ddb36571b423b87d
title: Driving Eligibility Check
challengeType: 1
dashedName: driving-eligibilty-check
---

# --description--

**Introduction:**
In JavaScript, logical conditions can be used to determine if someone meets certain criteria, such as being of legal age and possessing a driving license. This helps in making decisions based on multiple factors.
<br>
**Challenge:**
Write a JavaScript snippet that checks if a person is eligible to drive based on their age and whether they have a driving license. This will enhance your understanding of logical operators in decision-making.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`drivingEligibility(18,true)` should return `true`

```js
assert(drivingEligibility(18,true)===true)
```

`drivingEligibility(25,false)` should return `false`

```js
assert(drivingEligibility(25,false)===false)
```

`drivingEligibility(27,true)` should return `true`

```js
assert(drivingEligibility(27,true)===true)
```

`drivingEligibility(12,true)` should return `false`

```js
assert(drivingEligibility(12,true)===false)
```

`drivingEligibility(13,false)` should return `false`

```js
assert(drivingEligibility(13,false)===false)
```

# --seed--
## --seed-contents--

```js
function drivingEligibility(age,hasDL) {
  let isAdult = false;
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function drivingEligibility(age,hasDL) {
  let isAdult = false;
  let ans;
  if (age>17){
    isAdult = true;
  }
  if (isAdult===true){
    if (hasDL===true){
    ans = true;
    }else{
    ans = false;
    }
  }else{
    ans = false;
  }
	return ans;
}
drivingEligibility(age,hasDL)
```
