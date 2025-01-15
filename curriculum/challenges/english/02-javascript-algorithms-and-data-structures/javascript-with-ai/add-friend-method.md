---
id: 675433d8dc140478e1d73240
title: Add Friend Method
challengeType: 1
dashedName: add-friend-method
---

# --description--

**Introduction:**
Managing relationships between objects is crucial for creating interactive systems. This task involves enhancing an object with a method to maintain a list of friends.
<br>

**Challenge:**
Extend the createPersonObject function to include an addFriend method. This method should accept another person object and add it to a friends array property. If the friends array doesn’t exist, it should be created.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `this.`  in your code.

```js
assert(code.match(/this./g));
```

`createPersonObject("bablu", 23, { street: "1234", city: "delhi" }).addFriend("babli", 23, { street: "1234", city: "old delhi" })` should return `[{ name: "babli", age: 23, address: { street: "1234", city: "old delhi" }}]`

```js
assert.deepEqual(createPersonObject("bablu", 23, { street: "1234", city: "delhi" }).addFriend("babli", 23, { street: "1234", city: "old delhi" }),[{ name: "babli", age: 23, address: { street: "1234", city: "old delhi" }}])
```

# --seed--
## --seed-contents--

```js
function createPersonObject(name, age, address) {
  //Only change code below this line
  return
}
const person1 = createPersonObject("bablu", 23, { street: "1234", city: "delhi" }); // Change this line
const person2 = createPersonObject("babli", 23, { street: "1234", city: "old delhi" }) // Change this line
person1.addFriend(person2)
console.log(person1.friends);
```

# --solutions--

```js
function createPersonObject(name, age, address) {
  return {
    name: name,
    age: age,
    address: address,
    addFriend: function (friend) {
      if (typeof friend === "object" && friend.name && friend.age) {
        if (this.friend = this.friend ?? []) { // Check if friends is null or undefined and assign default value []
        // if (this.friends === undefined) { // Check if friends is undefined
          this.friends = []; // Initialize friends array
        }
        this.friends.push({ // Add the friend to the list
        name: friend.name,
        age: friend.age,
        address: friend.address,
      })
      } else {
        console.error("Invalid friend object");
      }
    },
  }
}
const person1 = createPersonObject("bablu", 23, { street: "1234", city: "delhi" }); // Change this line
const person2 = createPersonObject("babli", 23, { street: "1234", city: "old delhi" }) // Change this line
person1.addFriend(person2)
console.log(person1.friends);
```
