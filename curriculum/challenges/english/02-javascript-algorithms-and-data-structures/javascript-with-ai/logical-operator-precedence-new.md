---
id: 67870e1f40860e1c72b78821
title: Logical Operator Precedence
challengeType: 19
dashedName: logical-operator-precedence-new
---

# --description--

**Introduction:**
In JavaScript, logical operators (&&, ||, !) follow a specific order of precedence, which affects how expressions are evaluated. Understanding this order is essential for writing correct and predictable code.

# --questions--

## --text--

What will be the output of the code?

```js
let a = 10, b = 20, c = 11;
if (a++ > 0 || b-- > 0 && --c == 10) {
  console.log("Condition is true.");
} else {
  console.log("Condition is false.");
}
console.log(a, b, c);
```

## --answers--

Condition is true.  
11 20 10

---

Condition is false.  
11 19 10

---

Condition is true.  
11 20 11

---

Condition is false.  
10 20 11


## --video-solution--

3
