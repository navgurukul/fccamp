---
id: 67543588baf80a7b6069c132
title: Date Adder
challengeType: 1
dashedName: date-adder
---

# --description--

**Introduction:**
Manipulating dates by adding days can be crucial for scheduling and time calculations. This task involves creating a function that adjusts a date by a given number of days.
<br>

**Challenge:**
Implement the function addDaysToDate(date, days) that takes a Date object and a number of days as input, and returns a new Date object (in string format) representing the date after adding the specified number of days.

*Note*
Use only positive values to add. <br>
Use `new Date()` to create a new date object with current date. <br>
Use `.setDate()` to set date values. <br>
Use `.getDate()` to et date as a number. <br>
Use `.getFullYear()` to get year as a number. <br>
Use `.getMonth()` to get month as a number. <br>

**Example:**
<br>
Input
<br>
const date = new Date(); // Assuming today's date is 2023-10-05<br>
const daysToAdd = 11;<br>
<br>
Output
<br>
2023-10-16

# --instructions--

Click on this <a href="https://cs50.ai/chat" target="_blank" style="color:blue;" >Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `new Date()` in your code.

```js
assert(code.match(/new Date()/g));
```

You should use `.setDate()`  in your code.

```js
assert(code.match(/.setDate()/g));
```

You should use `.getDate()`  in your code.

```js
assert(code.match(/.getDate()/g));
```

You should use `.getFullYear()`  in your code.

```js
assert(code.match(/.getFullYear()/g));
```

You should use `.getMonth()`  in your code.

```js
assert(code.match(/.getMonth()/g));
```

`addDaysToDate("2023-10-05",10)` should return `"2023-10-15"`

```js
assert(addDaysToDate("2023-10-05",10)==="2023-10-15")
```

`addDaysToDate("2023-11-06",0)` should return `"2023-11-06"`

```js
assert(addDaysToDate("2023-11-06",0)==="2023-11-06")
```

`addDaysToDate("2020-10-07",12)` should return `"2020-10-19"`

```js
assert(addDaysToDate("2020-10-07",12)==="2020-10-19")
```

`addDaysToDate("2003-10-08",5)` should return `"2003-10-13"`

```js
assert(addDaysToDate("2003-10-08",5)==="2003-10-13")
```

`addDaysToDate("2023-12-31",1)` should return `"2024-01-01"`

```js
assert(addDaysToDate("2023-12-31",1)==="2024-01-01")
```


# --seed--
## --seed-contents--

```js
function addDaysToDate(date, days) {
  // Only change code below this line
	return
}
```

# --solutions--

```js
function addDaysToDate(date, days) {
    // Create a new Date object to avoid mutating the original date
    const newDate = new Date(date);
    // Add the specified number of days
    newDate.setDate(newDate.getDate() + days);
    // Format the date as YYYY MM DD without using padStart
    const year = newDate.getFullYear();
    const month = (newDate.getMonth() + 1) < 10 ? "0" + (newDate.getMonth() + 1) : (newDate.getMonth() + 1);
    const day = newDate.getDate() < 10 ? "0" + newDate.getDate() : newDate.getDate();
    let str = year+"-"+month+"-"+day
    return str; // Return the formatted date
}
```
