---
id: 675432e55ba97f76b33e2d3a
title: Simple Calculator Function
challengeType: 1
dashedName: simple-calculator-function
---

# --description--

**Introduction:**
Creating a basic calculator involves handling different operations based on user input. This task focuses on implementing a function that performs arithmetic calculations using operators.
<br>
**Challenge:**
Write an arrow function named calculate that takes two numbers and an operator (+, -, *, /) as arguments. Use a switch statement to perform the calculation and return the result. This exercise will help you practice using arrow functions and switch statements for conditional logic.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

**Example:**

**Input:**
<br>
let num1 = 10;
<br>
let num2 = 5
<br>
let Oper = "+"
<br>
**Output:**
<br>
15

# --hints--

`calculate(20,40,"*")` should return `800`

```js
assert(calculate(20,40,"*")===800)
```

`calculate(25,25,"-")` should return `0`

```js
assert(calculate(25,25,"-")===0)
```

`calculate(20,33,"+")` should return `53`

```js
assert(calculate(20,33,"+")===53)
```

`calculate(10,20,"/")` should return `0.5`

```js
assert(calculate(10,20,"/")===0.5)
```

`calculate(2,3,"-")` should return `-1`

```js
assert(calculate(2,3,"-")===-1)
```

`calculate(83,20,"/")` should return `4.15`

```js
assert(calculate(83,20,"/")===4.15)
```

`calculate(0,20,"/")` should return `0`

```js
assert(calculate(0,20,"/")===0)
```

`calculate(20,83,"&&")` should return `Error: Invalid operator`

```js
assert(calculate(20,83,"&&")==="Error: Invalid operator")
```

`calculate(20,0,"/")` should return `Error: Cannot divide by zero`

```js
assert(calculate(20,0,"/")==="Error: Cannot divide by zero")
```

# --seed--
## --seed-contents--

```js
const calculate = (num1,num2, operator) => {
    //  Only change code below this line
	return
}
```

# --solutions--

```js
const calculate = (num1, num2, operator) => {
  switch (operator) {
    case '+':
      return num1 + num2;
    case '-':
      return num1 - num2;
    case '*':
      return num1 * num2;
    case '/':
        if (num2!==0){
            return (num1/num2);
        }else{
            return "Error: Cannot divide by zero";
        }
    default:
      return "Error: Invalid operator";
  }
}
calculate(num1, num2, operator)
```
