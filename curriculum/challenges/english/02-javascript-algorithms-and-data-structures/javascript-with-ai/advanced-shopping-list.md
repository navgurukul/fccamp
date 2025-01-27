---
id: 675434137f447d7926cdaca5
title: Advanced Shoopping List
challengeType: 1
dashedName: advanced-shopping-list
---

# --description--

**Introduction:**
Enhancing a shopping list manager with methods to update and remove items adds greater functionality. This task involves expanding the basic shopping list with additional management capabilities.
<br>

**Challenge:**
Extend the createShoppingList function to include updateItemQuantity and removeItem methods. updateItemQuantity should accept an item name and update its quantity, while removeItem should accept an item name and remove it from the shoppingList.

*Note:* 
Use `shoppingList[shoppingList.length] = { name, quantity };` to push elements at the end of array.

# --instructions--

Click on this <a target="_blank" href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.length`  in your code to push elements at the end of array.

```js
assert(code.match(/.length/g));
```

`shoppingList.updateItemQuantity("Apples",5),shoppingList.updateItemQuantity("Apples",15),shoppingList.removeItem("Bananas"),shoppingList.getList()` should update the shopping list `[{ name: "Apples", quantity: 15 }]`

```js
assert.deepEqual(shoppingList.updateItemQuantity("Apples",5),shoppingList.updateItemQuantity("Apples",15),shoppingList.removeItem("Bananas"),shoppingList.getList(),[{ name: "Apples", quantity: 15 }])
```

`shoppingList.updateItemQuantity("Apples",5),shoppingList.updateItemQuantity("Cherries",3),shoppingList.removeItem("Bananas"),shoppingList.getList()` should update the shopping list `[{ name: "Apples", quantity: 5 },{name: "Cherries", quantity: 3}]`

```js
assert.deepEqual(shoppingList.updateItemQuantity("Apples",5),shoppingList.updateItemQuantity("Cherries",3),shoppingList.removeItem("Bananas"),shoppingList.getList(),[{ name: "Apples", quantity: 5 },{name: "Cherries", quantity: 3}])
```

`shoppingList.updateItemQuantity("Apples",5),shoppingList.removeItem("Bananas"),shoppingList.getList()` should update the shopping list `[{ name: "Apples", quantity: 5 }]`

```js
assert.deepEqual(shoppingList.updateItemQuantity("Apples",5),shoppingList.removeItem("Bananas"),shoppingList.getList(),[{ name: "Apples", quantity: 5 }])
```

`shoppingList.updateItemQuantity("Apples",5),shoppingList.removeItem("Apples"),shoppingList.getList()` should update the shopping list `[]`

```js
assert.deepEqual(shoppingList.updateItemQuantity("Apples",5),shoppingList.removeItem("Apples"),shoppingList.getList(),[])
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
shoppingList.updateItemQuantity("Apples",5);  // Change this line
shoppingList.removeItem("Bananas");  // Change this line
console.log(shoppingList.getList());
```

# --solutions--

```js
function createShoppingList() {
  const shoppingList = [];
  return {
    updateItemQuantity(name, quantity) {
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
    removeItem(name) {
      let newList = [];
      let found = false;
      for (let i = 0; i < shoppingList.length; i++) {
        if (shoppingList[i].name !== name) {
          newList[newList.length] = shoppingList[i]; // Copy items that don't match
        } else {
          found = true; // Mark as found
        }
      }
      if (found) {
        // Replace shoppingList contents with newList
        for (let i = 0; i < newList.length; i++) {
          shoppingList[i] = newList[i];
        }
        shoppingList.length = newList.length; // Adjust length
      }
      // If not found, do nothing and retain the original list
    },
    getList() {
      return shoppingList;
    },
  };
}
const shoppingList = createShoppingList();
shoppingList.updateItemQuantity(name,quantity);
shoppingList.removeItem(name);
console.log(shoppingList.getList());
```
