---
id: 6754343d48db477949135b57
title: Enhanced Shopping List
challengeType: 1
dashedName: enhanced-shopping-list
---

# --description--

**Introduction:**
Adding functionality to check item existence and sort the list improves list management. This task involves extending a shopping list manager with these capabilities.
<br>

**Challenge:**
Extend the createShoppingList function to include checkItem and sortList methods. checkItem should accept an item name and return true if the item exists, while sortList should sort the shoppingList alphabetically by item name.

*Note*
Use `.length()` in your code to push elements at the end of the array.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.length`  in your code to push elements at the end of array.

```js
assert(code.match(/.length/g));
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.checkItem("Apples"),shoppingList.sortList()` should update the shopping list `true,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Oranges", quantity: 1 }]`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.checkItem("Apples"),shoppingList.sortList(),[true,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Oranges", quantity: 1 }]])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.addItem("Cherries",3),shoppingList.checkItem("Mangoes"),shoppingList.sortList()` should update the shopping list `false,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 15 },{ name: "Cherries", quantity: 3}, { name: "Oranges", quantity: 1 }]`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",15),shoppingList.addItem("Cherries",3),shoppingList.checkItem("Mangoes"),shoppingList.sortList(),[false,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 15 },{ name: "Cherries", quantity: 3},{ name: "Oranges", quantity: 1 }]])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.addItem("Cherries",3),shoppingList.checkItem("Mangoes"),shoppingList.sortList()` should update the shopping list `true,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Cherries", quantity: 3}, { name: "Oranges", quantity: 1 }]`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",3),shoppingList.addItem("Cherries",3),shoppingList.checkItem("Mangoes"),shoppingList.sortList(),[true,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 3 },{ name: "Cherries", quantity: 3},{ name: "Oranges", quantity: 1 }]])
```

`shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",15),shoppingList.checkItem("Cherries"),shoppingList.sortList()` should update the shopping list `false,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 15 },{ name: "Oranges", quantity: 1 }]`

```js
assert.deepEqual(shoppingList.addItem("Oranges",1),shoppingList.addItem("Apples",15),shoppingList.addItem("Bananas",15),shoppingList.checkItem("Cherries"),shoppingList.sortList(),[false,[{ name: "Apples", quantity: 15 },{ name: "Bananas", quantity: 15 },{ name: "Oranges", quantity: 1 }]])
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
shoppingList.addItem("Oranges",1); // Change this line
shoppingList.checkItem("Apples"); // Change this line
console.log(shoppingList.sortList());
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
    checkItem(name) {
      for (let i = 0; i < shoppingList.length; i++) {
        if (shoppingList[i].name === name) {
          return true; // Item found
        }
      }
      return false; // Item not found
    },
    sortList() {
      for (let i = 0; i < shoppingList.length - 1; i++) {
        for (let j = 0; j < shoppingList.length - i - 1; j++) {
          if (shoppingList[j].name > shoppingList[j + 1].name) {
            // Swap items
            const temp = shoppingList[j];
            shoppingList[j] = shoppingList[j + 1];
            shoppingList[j + 1] = temp;
          }
        }
      }
      return shoppingList; // Return sorted list
    }
  };
}
const shoppingList = createShoppingList();
shoppingList.addItem(name,quantity);
shoppingList.checkItem(item);
shoppingList.sortList(); // [{ name: "Apples", quantity: 2 }, { name: "Bananas", quantity: 3 }, { name: "Oranges", quantity: 1 }]
```
