---
id: 675435e338706a7bc6911016
title: Custom Date Formatter
challengeType: 1
dashedName: custom-date-formatter
---

# --description--

**Introduction:**
The customDateFormatter function lets you format dates with specific placeholders, allowing for flexible and readable date representations. You can specify how you want the date and time components to appear in the output.
<br>

**Challenge:**
Implement the function customDateFormatter(date, formatString) to take a Date object and a format string with placeholders (YYYY, MM, DD, HH, mm, ss, A). Return a string where the date and time are formatted according to the given format.

*Note*
Use only positive values to add. <br>
Use `new Date()` to create a new date object with current date. <br>
Use `.getDate()` to et date as a number. <br>
Use `getFullYear()` to get year as a number. <br>
Use `getMonth()` to get month as a number. <br>
Use `.Hours()` to get hours as a number. <br>
Use `.getMinutes()` to get minutes as a number. <br>
Use `.getSeconds()` to get seconds as a number. <br>
Use `.replace()` to replace the values for getting the desired output.

**Example:**
<br>
Input <br>
const today = new Date(); <br>
(Assuming today's date is 2023-10-05 10:30 PM) <br>
const formatString1 = "DD/MM/YYYY"; <br>
const formatString2 = "HH:mm A"; <br>
<br>
Output
const formattedDate1 = customDateFormatter(today, formatString1); // "05/10/2023" <br>
const formattedDate2 = customDateFormatter(today, formatString2); // "10:30 PM"

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `new Date()` in your code.

```js
assert(code.match(/new Date()/g));
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

You should use `.getMinutes()`  in your code.

```js
assert(code.match(/.getMinutes()/g));
```

You should use `.getHours()`  in your code.

```js
assert(code.match(/.getHours()/g));
```

You should use `.getSeconds()`  in your code.

```js
assert(code.match(/.getSeconds()/g));
```

You should use `.replace()`  in your code.

```js
assert(code.match(/.replace()/g));
```

# --seed--
## --seed-contents--

```js
function customDateFormatter(date, formatString) {
  // Only change code below this line
	return
}
customDateFormatter("2023-10-05", "DD/MM/YYYY")
customDateFormatter("2023-10-05", "hh:mm A")
```

# --solutions--

```js
function customDateFormatter(date, formatString) {
  const day = date.getDate() < 10 ? '0' + date.getDate() : date.getDate(); // DD
  const month = (date.getMonth() + 1) < 10 ? '0' + (date.getMonth() + 1) : (date.getMonth() + 1); // MM
  const year = date.getFullYear(); // YYYY
  const hours = date.getHours(); // 24-hour format hours
  const minutes = date.getMinutes() < 10 ? '0' + date.getMinutes() : date.getMinutes(); // mm
  const seconds = date.getSeconds() < 10 ? '0' + date.getSeconds() : date.getSeconds(); // ss
  const period = hours < 12 ? 'AM' : 'PM'; // A
  // Convert to 12-hour format
  const hours12 = hours % 12 || 12;
  return formatString
    .replace('DD', day)
    .replace('MM', month)
    .replace('YYYY', year)
    .replace('HH', hours < 10 ? '0' + hours : hours) // Always show 2 digits for HH in 24-hour format
    .replace('hh', hours12 < 10 ? '0' + hours12 : hours12) // Always show 2 digits for hh in 12-hour format
    .replace('mm', minutes)
    .replace('ss', seconds)
    .replace('A', period);
}
```
