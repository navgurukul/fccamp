---
id: 675434b92364017a9764d618
title: Shopping List Enhancements
challengeType: 1
dashedName: shopping-list-enhancements
---

# --description--

**Introduction:**
Improving a shopping list with filtering and quantity calculations adds valuable insights for better inventory management. This task involves extending the list manager to include these functionalities.
<br>

**Challenge:**
Extend the createShoppingList function to include filterByQuantity and calculateTotalQuantity methods. filterByQuantity should return items with quantities greater than a given threshold, while calculateTotalQuantity should return the total quantity of all items in the shoppingList.

*Note*
Use `.length`  in your code to push elements at the end of array.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.length`  in your code to push elements at the end of array.

```js
assert(code.match(/.length/g));
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(1),shoppingList.calculateTotalQuantity()` should return `[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Oranges", quantity: 1 }],19`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(1),shoppingList.calculateTotalQuantity(),[[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Oranges", quantity: 1 }],19])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(2),shoppingList.calculateTotalQuantity()` should return `[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 }],19`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(2),shoppingList.calculateTotalQuantity(),[[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 }],19])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(15),shoppingList.calculateTotalQuantity()` should return `[{ name: "Apples", quantity: 15 }],19`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(15),shoppingList.calculateTotalQuantity(),[[{ name: "Apples", quantity: 15 }],19])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(16),shoppingList.calculateTotalQuantity()` should return `[],19`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.filterByQuantity(16),shoppingList.calculateTotalQuantity(),[[],19])
```

# --seed--
## --seed-contents--

```js
function createShoppingList() {
  const shoppingList = [];
  //Only change code below this line
  return
}
const shoppingList = createShoppingList();
shoppingList.addItem("Apples",5); // Change this line
shoppingList.filterByQuantity(2); // Change this line
shoppingList.calculateTotalQuantity();
```

# --solutions--

```js
function createShoppingList() {
  const shoppingList = [];
  return {
    addItem(name, quantity) {
      let found = false;
      for (let i = 0; i < shoppingList.length; i++) {
        if (shoppingList[i].name === name) {
          shoppingList[i].quantity = quantity; // Update quantity
          found = true;
          break;
        }
      }
      if (!found) {
        shoppingList[shoppingList.length] = { name, quantity }; // Add new item
      }
    },
    filterByQuantity(threshold) {
      const filteredList = [];
      for (let i = 0; i < shoppingList.length; i++) {
        if (shoppingList[i].quantity >= threshold) {
          filteredList[filteredList.length] = shoppingList[i]; // Add items meeting threshold
        }
      }
      return filteredList; // Return filtered list
    },
    calculateTotalQuantity() {
      let totalQuantity = 0;
      for (let i = 0; i < shoppingList.length; i++) {
        totalQuantity += shoppingList[i].quantity; // Sum up all quantities
      }
      return totalQuantity; // Return total quantity
    },
    getList() {
      return shoppingList; // Return the full shopping list
    }
  };
}
const shoppingList = createShoppingList();
shoppingList.addItem(name, quantity);
shoppingList.filterByQuantity(threshold);
shoppingList.calculateTotalQuantity();
```
