---
id: 67543473508572797156f17f
title: Detailed Shopping List
challengeType: 1
dashedName: detailed-shopping-list
---

# --description--

**Introduction:**
Displaying a shopping list with item details helps in better tracking and management. This task involves adding functionality to format and show a detailed list of items.
<br>

**Challenge:**
Extend the createShoppingList function to include a displayDetailedList method. This method should return a formatted string listing all items in the shoppingList along with their quantities.

*Note*
Use `.length`  in your code to push elements at the end of array. <br>
Use `.trim`  in your code to push elements at the end of array.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.length`  in your code to push elements at the end of array.

```js
assert(code.match(/.length/g));
```

You should use `.trim`  in your code to push elements at the end of array.

```js
assert(code.match(/.trim/g));
```

`shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",3),shoppingList.displayDetailedList()` should return the string `"Oranges : 1 Apples : 15 Bananas : 3"`

```js
assert.deepEqual(shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",3),shoppingList.displayDetailedList(), ["Oranges : 1 Apples : 15 Bananas : 3"])
```

`shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",3),shoppingList.addItemQuantity("Cherries",3),shoppingList.displayDetailedList()` should return the string `"Oranges : 1 Apples : 15 Bananas : 3 Cherries : 3 "`

```js
assert.deepEqual(shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",3),shoppingList.addItemQuantity("Cherries",3),shoppingList.displayDetailedList(), ["Oranges : 1 Apples : 15 Bananas : 3 Cherries : 3 "])
```

`shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",30),shoppingList.displayDetailedList()` should return the string `"Oranges : 1 Apples : 15 Bananas : 30 "`

```js
assert.deepEqual(shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Bananas",30),shoppingList.displayDetailedList(), ["Oranges : 1 Apples : 15 Bananas : 30 "])
```

`shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Cherries",3),shoppingList.displayDetailedList()` should return the string `"Oranges : 1 Apples : 15 Cherries : 3 "`

```js
assert.deepEqual(shoppingList.addItemQuantity("Oranges",1),shoppingList.addItemQuantity("Apples",15),shoppingList.addItemQuantity("Cherries",3),shoppingList.displayDetailedList(), ["Oranges : 1 Apples : 15 Cherries : 3 "])
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
shoppingList.addItemQuantity("Apples",5);  // Change this line
console.log(shoppingList.displayDetailedList());
```

# --solutions--

```js
function createShoppingList() {
  const shoppingList = [];
  return {
    addItemQuantity(name, quantity) {
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
    displayDetailedList() {
      if (shoppingList.length === 0) {
        return "Shopping List is empty."; // Handle empty list
      }
      // Format the list for display
      let detailedList = "";
      for (let i = 0; i < shoppingList.length; i++) {
        detailedList += `${shoppingList[i].name} : ${shoppingList[i].quantity} `;
      }
    return detailedList.trim(); // Remove the trailing newline
    }
  };
}
const shoppingList = createShoppingList();
shoppingList.addItemQuantity(name,quantity);
shoppingList.displayDetailedList();
```
