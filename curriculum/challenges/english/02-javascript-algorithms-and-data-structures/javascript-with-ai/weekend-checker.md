---
id: 675435ad51513d7b82408d5a
title: Weekend Checker
challengeType: 1
dashedName: weekend-checker
---

# --description--

**Introduction:**
Determining if a given date falls on a weekend is useful for scheduling and time management. This task involves creating a function to identify weekend dates.
<br>

**Challenge:**
Implement the function isWeekend(date) that takes a Date object as input and returns true if the date is a Saturday or Sunday; otherwise, return false.

*Note*
Use `new Date()` to create a new date object with current date. <br>

**Example:**
<br>
Input
<br>
const today = new Date('2023-10-07'); // Saturday
<br>
Output
<br>
true

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `new Date()` in your code.

```js
assert(code.match(/new Date()/g));
```

`isWeekend("2023-10-05")` should return `false`

```js
assert(isWeekend("2023-10-05")===false)
```

`isWeekend("2023-11-06")` should return `false`

```js
assert(isWeekend("2023-11-06")===false)
```

`isWeekend("2020-10-07")` should return `false`

```js
assert(isWeekend("2020-10-07")===false)
```

`isWeekend("2003-10-11")` should return `true`

```js
assert(isWeekend("2003-10-11")===true)
```

`isWeekend("2023-12-31")` should return `true`

```js
assert(isWeekend("2023-12-31")===true)
```

# --seed--
## --seed-contents--

```js
function isWeekend(date) {
  // Only change code below this line
	return
}
```

# --solutions--

```js
function isWeekend(date) {
    let day = new Date(date);
    // Get the day of the week: 0 (Sunday) to 6 (Saturday)
    const dayOfWeek = day.getDay();
    // Return true if the day is Saturday (6) or Sunday (0)
    return dayOfWeek === 0 || dayOfWeek === 6;
}
isWeekend(date)
```
