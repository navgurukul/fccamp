---
id: 675435c970bc547ba287b9d4
title: Days Until Birthday
challengeType: 1
dashedName: days-until-birthday
---

# --description--

**Introduction:**
Calculating the number of days until the next birthday helps with planning and reminders. This function will compute how many days are left until the next occurrence of a birthday.
<br>

**Challenge:**
Implement the function daysUntilBirthday(birthdayDateString) that takes a birthday date string in "YYYY-MM-DD" format and returns the number of days from today until the user's next birthday.

*Note* <br>
if day = 1 print 1 day otherwise n days
Use `new Date()` to create a new date object with current date. <br>
Use `getFullYear()` to get year as a number. <br>
Use `setFullYear()` to set year. <br>
Use `Math.ceil()` to get number rounded up to it's nearest number, i.e (Math.ceil(4.4) will give 5). <br>

**Example:**
<br>
Input
<br>
const birthdayString = "2023-10-04";
<br>
Output
<br>
364 days (Assuming today is 2023-10-05)

# --instructions--

Click on this <a href = "https://cs50.ai/chat" target="_blank" style="color:blue;">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `new Date()` in your code.

```js
assert(code.match(/new Date()/g));
```

You should use `setFullYear())`  in your code.

```js
assert(code.match(/setFullYear()/g));
```

You should use `getFullYear()`  in your code.

```js
assert(code.match(/getFullYear()/g));
```

You should use `Math.ceil()`  in your code.

```js
assert(code.match(/Math.ceil()/g));
```

`daysUntilBirthday("2023-10-04")` should return `"271 days"`

```js
assert(daysUntilBirthday("2023-10-04")==="271 days")
```

# --seed--
## --seed-contents--

```js
function daysUntilBirthday(birthdayDateString) {
    const today = new Date();
  // Only change code below this line
	return
}
```

# --solutions--

```js
function daysUntilBirthday(birthdayDateString) {
  const today = new Date();
  const birthday = new Date(birthdayDateString);
  // Set the year of the birthday to the current year
  birthday.setFullYear(today.getFullYear());
  // If the birthday has already passed this year, set it for the next year
  if (birthday < today) {
    birthday.setFullYear(today.getFullYear() + 1);
  }
  // Calculate the difference in time (milliseconds)
  const timeDifference = birthday - today;
  // Convert time difference to days and round down to the nearest whole number
  const daysLeft = Math.ceil(timeDifference / (1000 * 3600 * 24));
  // Use if-else to decide between "day" and "days"
  let dayText;
  if (daysLeft === 1) {
    dayText = "day";
  } else {
    dayText = "days";
  }
  // Return the result
  return `${daysLeft} ${dayText}`;
}
daysUntilBirthday(birthdayDateString)
```
