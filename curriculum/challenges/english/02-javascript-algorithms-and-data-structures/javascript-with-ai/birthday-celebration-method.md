---
id: 6754339ea79377788eeeeb02
title: Birthday Celebration Method
challengeType: 1
dashedName: birthday-celebration-method
---

# --description--

**Introduction:**
Enhancing object methods to manipulate properties dynamically is essential for interactive applications. This task involves adding a method to update an object's property in response to an event.
<br>

**Challenge:**
Extend the createPersonObject function to include a celebrateBirthday method. This method should increment the person’s age by 1 using this keyword to refer to the object's properties.

*Note:* 
Use `this.` in your code to refer the value of object.

**Example:**
<br>
Input:
<br>
person : Object created by createPersonObject from Problem 1
<br>
age: 29
<br>
Output:
<br>
*Updated person object with incremented age.
<br>
person.celebrateBirthday();
<br>
console.log(person.introduce()); // "Hi, I'm John Doe, 30 years old, living at 987 Maple Street, New City."


# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

You should use `this.`  in your code.

```js
assert(code.match(/this./g));
```

`createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"},{street: "987 ZXX Street", city: "New City"}).introduce()` should return `"Hi, I'm Bablu, 33 years old, living at 987 ZXX Street, New City"`

```js
assert.deepEqual(createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"},{street: "987 ZXX Street", city: "New City"}).introduce(),"Hi, I'm Bablu, 33 years old, living at 987 ZXX Street, New City")
```

`createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"},{street: "987 Maple Street", city: "New City"}).introduce()` should return `"Hi, I'm Chutki, 13 years old, living at 987 Maple Street, New City"`

```js
assert.deepEqual(createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"},{street: "987 Maple Street", city: "New City"}).introduce(),"Hi, I'm Chutki, 13 years old, living at 987 Maple Street, New City")
```

`createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"},{street: "91 Asd Lane", city: "New City"}).introduce()` should return `"Hi, I'm Nobita, 21 years old, living at 98 Road, New City"`

```js
assert.deepEqual(createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"},{street: "98 Road", city: "New City"}).introduce(),"Hi, I'm Nobita, 21 years old, living at 98 Road, New City")
```

`createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"},{street: "7 ZYX Street", city: "Old City"}).introduce()` should return `"Hi, I'm Chintu, 11 years old, living at 7 ZYX Street, Old City"`

```js
assert.deepEqual(createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"},{street: "7 ZYX Street", city: "Old City"}).introduce(),"Hi, I'm Chintu, 11 years old, living at 7 ZYX Street, Old City")
```

`createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"},{street: "9 Asd Lane", city: "Old City"}).introduce()` should return `"Hi, I'm Minki, 56 years old, living at 9 Asd Lane, Old City"`

```js
assert.deepEqual(createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"},{street: "9 Asd Lane", city: "Old City"}).introduce(),"Hi, I'm Minki, 56 years old, living at 9 Asd Lane, Old City")
```

# --seed--
## --seed-contents--

```js
function createPersonObject(name,age,address){
	//  Only change code below this line
	return
}
const person = createPersonObject("babli", 23, { street: "1234", city: "delhi" }, { street: "987 Maple Street", city: "New City" }); // Change this line
console.log(person.introduce());
```

# --solutions--

```js
function createPersonObject(name, age, oldAddress, newAddress) { 
    // Automatically assign the new address if provided
    const updatedAddress = newAddress || oldAddress; 
    return { 
        name: name, 
        age: age, 
        address: updatedAddress, 
        introduce: function () { 
            this.celebrateBirthday();
            return `Hi, I'm ${this.name}, ${this.age} years old, living at ${this.address.street}, ${this.address.city}`; 
        },
        celebrateBirthday: function () {
            this.age += 1;
        }
    }; 
}
const person = createPersonObject(name, age, {oldAddress}, {newAddress});
console.log(person.introduce());
```
