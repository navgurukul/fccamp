---
id: 675433f3c26c087905e22ced
title: Shopping List Manager
challengeType: 1
dashedName: shopping-list-manager
---

# --description--

**Introduction:**
Managing a shopping list involves adding and tracking items efficiently. This task focuses on creating a function to handle item addition to a list.
<br>

**Challenge:**
Write a function createShoppingList that initializes an empty shoppingList array. Implement an addItem function to accept an item object (with name and quantity properties) and add it to the shoppingList.

*Note:* 
Use `.push()` to add items at end of the shopping list.

**Example:**
<br>
Input:
<br>
const shoppingList = createShoppingList();
<br>
addItem(shoppingList, { name: "Apples", quantity: 2 });
<br>
addItem(shoppingList, { name: "Bananas", quantity: 3 });
<br>
Output:
<br>
console.log(shoppingList); // [{ name: "Apples", quantity: 2 }, { name: "Bananas",
quantity: 3 }]

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `.push()`  in your code.

```js
assert(code.match(/.push()/g));
```

`addItem([],{ name: "Apples", quantity: 2 }),addItem([{ name: "Apples", quantity: 2 }],{name: "Bananas", quantity: 3 })` should add the item to the shopping list `[{ name: "Apples", quantity: 2 },{ name: "Bananas", quantity: 3 }]`

```js
assert.deepEqual(addItem([],{ name: "Apples", quantity: 2 }),addItem([{ name: "Apples", quantity: 2 }],{name: "Bananas", quantity: 3 }),[{ name: "Apples", quantity: 2 },{ name: "Bananas", quantity: 3 }])
```

`addItem([],{ name: "Apples", quantity: 5 }),addItem([{ name: "Apples", quantity: 5 }],{name: "Bananas", quantity: 3 }),addItem([{ name: "Apples", quantity: 5 },{name: "Bananas", quantity: 3 }],{name: "Cherries", quantity: 3})` should add the item to the shopping list `[{ name: "Apples", quantity: 5 },{ name: "Bananas", quantity: 3 },{name: "Cherries", quantity: 3}]`

```js
assert.deepEqual(addItem([],{ name: "Apples", quantity: 5 }),addItem([{ name: "Apples", quantity: 5 }],{name: "Bananas", quantity: 3 }),addItem([{ name: "Apples", quantity: 5 },{name: "Bananas", quantity: 3 }],{name: "Cherries", quantity: 3}),[{ name: "Apples", quantity: 5 },{ name: "Bananas", quantity: 3 },{name: "Cherries", quantity: 3}])
```

# --seed--
## --seed-contents--

```js
function createShoppingList(){
    return [];
}
function addItem(shoppingList,item){
	//  Only change code below this line
	return
}
const shoppingList = createShoppingList();
addItem(shoppingList, { name: "Oranges", quantity: 3}); // Change this line
```

# --solutions--

```js
function createShoppingList() {
    return [];
}
// Function to add an item to the shopping list
function addItem(shoppingList, item) {
    if (item === null || item === undefined) {
        console.error("Item cannot be null or undefined.");
        return;
    }
    if (typeof item !== "object") {
        console.error("Item must be an object.");
        return;
    }
    if (typeof item.name !== "string") {
        console.error("Item must have a 'name' property of type string.");
        return;
    }
    if (typeof item.quantity !== "number") {
        console.error("Item must have a 'quantity' property of type number.");
        return;
    }
    // If all validations pass, add the item to the shopping list
    shoppingList.push(item);
}
const shoppingList = createShoppingList();
addItem(shoppingList, { name: "Oranges", quantity: 3});
```
