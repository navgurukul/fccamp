---
id: 6606ce1bcbc39c15b0b5d550
title: Comparison with the Inequality Operator
challengeType: 1
dashedName: com-ineq-op
---

# --description--

The inequality operator (`!=`) is the opposite of the equality operator. It means not equal and returns `false` where equality would return `true` and *vice versa*. Like the equality operator, the inequality operator will convert data types of values while comparing.
<h2>Hinglish</h2>
Inequality operator (`!=`) equality operator ka opposite hota hai. Ye not equal ka matlab rakhta hai aur wahi jagah `false` return karta hai jahan equality `true` return karega aur ulta. Equality operator ki tarah, inequality operator bhi values ko compare karte waqt data types ko convert kar dega.

**Examples**

```js
1 !=  2    // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
```

# --instructions--

Add the inequality operator `!=` in the `if` statement so that the function will return the string `Not Equal` when `val` is not equivalent to `99`.

`if` statement mein inequality operator `!=` ko add karein taki function `Not Equal` string return kare jab `val` `99` ke barabar na ho.


# --hints--

`testNotEqual(99)` should return the string `Equal`

```js
assert(testNotEqual(99) === 'Equal');
```

`testNotEqual("99")` should return the string `Equal`

```js
assert(testNotEqual('99') === 'Equal');
```

`testNotEqual(12)` should return the string `Not Equal`

```js
assert(testNotEqual(12) === 'Not Equal');
```

`testNotEqual("12")` should return the string `Not Equal`

```js
assert(testNotEqual('12') === 'Not Equal');
```

`testNotEqual("bob")` should return the string `Not Equal`

```js
assert(testNotEqual('bob') === 'Not Equal');
```

You should use the `!=` operator

```js
assert(__helpers.removeJSComments(code).match(/(?!!==)!=/));
```

# --seed--

## --seed-contents--

```js
// Setup
function testNotEqual(val) {
  if (val) { // Change this line
    return "Not Equal";
  }
  return "Equal";
}

testNotEqual(10);
```

# --solutions--

```js
function testNotEqual(val) {
  if (val != 99) {
    return "Not Equal";
  }
  return "Equal";
}
```
