---
id: 675433bf0e3e1478af660590
title: List Person Details
challengeType: 1
dashedName: list-person-details
---

# --description--

**Introduction:**
Iterating over object properties to display their values is a useful skill for data representation and debugging. This task involves creating a function to list all details of a person object.
<br>
**Challenge:**
Write a function listPersonDetails that takes a person object (created by createPersonObject) and returns a string listing all properties and their values. Use a for-in loop to iterate over the object's properties.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `typeof()`  in your code to check Data Type.

```js
assert(code.match(/typeof/g));
```

`listPersonDetails(createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"}))` should return `"name: Bablu, age: 32, address: [object]"`

```js
assert.deepEqual(listPersonDetails(createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"})),"name: Bablu, age: 32, address: [object]")
```

`listPersonDetails(createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"}))` should return `"name: Chutki, age: 12, address: [object]"`

```js
assert.deepEqual(listPersonDetails(createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"})),"name: Chutki, age: 12, address: [object]")
```

`listPersonDetails(createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"}))` should return `"name: Nobita, age: 20, address: [object]"`

```js
assert.deepEqual(listPersonDetails(createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"})),"name: Nobita, age: 20, address: [object]")
```

`listPersonDetails(createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"}))` should return `"name: Chintu, age: 10, address: [object]"`

```js
assert.deepEqual(listPersonDetails(createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"})),"name: Chintu, age: 10, address: [object]")
```

`listPersonDetails(createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"}))` should return `"name: Minki, age: 55, address: [object]"`

```js
assert.deepEqual(listPersonDetails(createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"})),"name: Minki, age: 55, address: [object]")
```

# --seed--
## --seed-contents--

```js
function createPersonObject(name,age,address){
	//  Only change code below this line
	return
}
const person = createPersonObject("Babli", 33, { street: "23 Abc Street", city: "XYZ" }); // Change this line
console.log(listPersonDetails(person));
```

# --solutions--

```js
function createPersonObject(name, age, address) {
  return {
    name: name,
    age: age,
    address: address,
  };
}
function listPersonDetails(person) {
    let details = "";
    for (let key in person) {
        if (typeof person[key] === "object" && person[key] !== null) {
            // Show nested objects as [object Object]
            // details += `${key}: [object Object]\n`;
            details += `${key}: [object]`;
        } else if (typeof person[key] !== "function") {
            // Add non-function properties directly
            // details += `${key}: "${person[key]}"\n`;
            details += `${key}: ${person[key]}, `;
        }
    }
    return details;
}
const person = createPersonObject("Babli", 33, { street: "23 Abc Street", city: "XYZ" });
console.log(listPersonDetails(person));
```
