---
id: 6754334ab3c1b278468adc18
title: Person Object Creator
challengeType: 1
dashedName: person-object-creator
---

# --description--

**Introduction:**
Creating structured objects with methods enhances code organization and functionality. This task involves building a function to create a person object with specific properties and methods.
<br>

**Challenge:**
Write a function createPersonObject that takes name, age, and address (with street and city properties) as parameters. The function should return an object with these properties and an introduce method that returns a string introduction of the person.

*Note:* 
Use `this.` in your code to refer the value of object.

**Example:**
<br>
Input:
<br>
name : "John Doe" <br>
age : 30 <br>
address : {street: "123 Elm Street", city: "Somewhere"}
<br>
Output:
<br>
*Object with properties name , age , address , and method introduce console.log(person.introduce()); // "Hi, I'm John Doe, 30 years old, living at 123 Elm Street, Somewhere."


# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `this.`  in your code.

```js
assert(code.match(/this./g));
```

`createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"}).introdce()` should return `Hi, I'm Bablu, 32 years old, living at 23 Abc Street, XYZ`

```js
assert.deepEqual(createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"}).introduce(),"Hi, I'm Bablu, 32 years old, living at 23 Abc Street, XYZ")
```

`createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"}).introduce()` should return `"Hi, I'm Chutki, 12 years old, living at 45 Abc Street, XYZ"`

```js
assert.deepEqual(createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"}).introduce(),"Hi, I'm Chutki, 12 years old, living at 45 Abc Street, XYZ")
```

`createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"}).introduce()` should return `"Hi, I'm Nobita, 20 years old, living at 44 ghi Street, PQR"`

```js
assert.deepEqual(createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"}).introduce(),"Hi, I'm Nobita, 20 years old, living at 44 ghi Street, PQR")
```

`createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"}).introduce()` should return `"Hi, I'm Chintu, 10 years old, living at 23 Abc Street, WXYZ"`

```js
assert.deepEqual(createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"}).introduce(),"Hi, I'm Chintu, 10 years old, living at 23 Abc Street, WXYZ")
```

`createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"}).introduce()` should return `"Hi, I'm Minki, 55 years old, living at 11 Abc Lane, XYZ"`

```js
assert.deepEqual(createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"}).introduce(),"Hi, I'm Minki, 55 years old, living at 11 Abc Lane, XYZ")
```

# --seed--
## --seed-contents--

```js
function createPersonObject(name,age,address){
	//  Only change code below this line
	return
}
const person = createPersonObject("babli",23,{street:"1234",city:"delhi"}) // Change this line
console.log(person.introduce());
```

# --solutions--

```js
function createPersonObject(name, age, address) {
  return {
    name: name,
    age: age,
    address: address,
    introduce: function () {
      return `Hi, I'm ${this.name}, ${this.age} years old, living at ${this.address.street}, ${this.address.city}`;
    },
  };
}
const person = createPersonObject("babli",23,{street:"1234",city:"delhi"}) // Change this line
console.log(person.introduce());
```
