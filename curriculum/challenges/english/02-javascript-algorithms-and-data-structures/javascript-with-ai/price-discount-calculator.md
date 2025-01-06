---
id: 677bc4d1dfed46c39bea6754
title: Price Discount Calculator
challengeType: 1
dashedName: price-discount-calculator
---

# --description--

**Introduction:**
Applying discounts based on price thresholds is a common task in programming. This exercise 
involves calculating a discounted price by applying different discount rates depending on the item's cost.
<br>

**Challenge:**
Write a program that takes a variable price, applies a 10% discount if the price is over 1000, a 5% discount if the price is over 500, and stores the final discounted price in a variable discountedPrice. This will help you practice conditional logic and arithmetic operations.

**Example :**
<br>
Input:
<br>
let price = 750;
<br>
Output
<br>
712.5

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`applyDiscount(500)` should return `500`

```js
assert(applyDiscount(500)===500)
```

`applyDiscount(1200)` should return `1080`

```js
assert(applyDiscount(1200)===1080)
```

`applyDiscount(700)` should return `665`

```js
assert(applyDiscount(700)===665)
```

`applyDiscount(200)` should return `200`

```js
assert(applyDiscount(200)===200)
```

`applyDiscount(1000)` should return `950`

```js
assert(applyDiscount(1000)===950)
```

# --seed--
## --seed-contents--

```js
function applyDiscount(price) {
  //  Only change code below this line
	return
}
```

# --solutions--

```js
function applyDiscount(price) {
  let discountedPrice;
  // Check if the price is greater than 1000 and apply a 10% discount
  if (price > 1000) {
    discountedPrice = price * 0.90;  // Apply 10% discount
  }
  // Check if the price is greater than 500 and apply a 5% discount
  else if (price > 500) {
    discountedPrice = price * 0.95;  // Apply 5% discount
  }
  // If price is 500 or below, no discount
  else {
    discountedPrice = price;  // No discount
  }
  return discountedPrice;
}
applyDiscount(price)
```
