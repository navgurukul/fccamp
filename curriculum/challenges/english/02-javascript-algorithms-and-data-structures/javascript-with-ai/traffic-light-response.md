---
id: 67543203521165763c06d85a
title: Traffic Light Response
challengeType: 1
dashedName: traffic-light-response
---

# --description--

**Introduction:**
Using a switch statement allows you to handle multiple conditions based on different inputs. This program demonstrates how to respond to traffic light colors and a numerical value with specific messages.
<br>

**Challenge:**
Write a switch statement that evaluates a variable trafficLightColor and a number, and outputs a message based on the conditions: "Stop" for "Red" with specific numeric constraints, "Get ready to go" for "Yellow", "Go" for "Green", and "invalid input" for other cases. This will help you practice using switch statements and handling multiple conditions.

**Explanation :**

* Stop for Red (when num is less than 15 and greater than or equal to zero)
* Get ready to go for Yellow (when num is greater than 15 and less than 20)
* Go for "Green" (when num is more than 20 and less than 30)
* Use the default statement as invalid input.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`trafficSignal(10,"Red")` should return `Stop`

```js
assert(trafficSignal(10,"Red")==="Stop")
```

`trafficSignal(5,"Green")` should return `invalid input`

```js
assert(trafficSignal(5,"Green")==="invalid input")
```

`trafficSignal(25,"Green")` should return `Go`

```js
assert(trafficSignal(25,"Green")==="Go")
```

`trafficSignal(5,"Blue")` should return `invalid input`

```js
assert(trafficSignal(5,"Blue")==="invalid input")
```

`trafficSignal(17,"Yellow")` should return `Get ready to go`

```js
assert(trafficSignal(17,"Yellow")==="Get ready to go")
```

`trafficSignal(30,"Green")` should return `invalid input`

```js
assert(trafficSignal(30,"Green")==="invalid input")
```

# --seed--
## --seed-contents--

```js
function trafficSignal(num,trafficLightColor) {
    //  Only change code below this line
	return
}
```

# --solutions--

```js
function trafficSignal(num, trafficLightColor) {
  switch (trafficLightColor) {
    case "Red":
      if (num < 15 && num >= 0) {
        return "Stop";
      }
      break;
    case "Yellow":
      if (num > 15 && num < 20) {
        return "Get ready to go";
      }
      break;
    case "Green":
      if (num > 20 && num < 30) {
        return "Go";
      }
      break;
    default:
      return "invalid input";
  }
  return "invalid input";
}
trafficSignal(num,trafficLightColor)
```
