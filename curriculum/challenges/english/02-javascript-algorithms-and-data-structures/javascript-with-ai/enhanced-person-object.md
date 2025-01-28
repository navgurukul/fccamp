---
id: 67543370f9bb22786d6f0692
title: Enhanced Person Object
challengeType: 1
dashedName: enhanced-person-object
---

# --description--

**Introduction:**
Adding methods to update properties in objects enhances their flexibility and functionality. This task involves extending an existing function to include a method for updating an address.
<br>

**Challenge:**
Extend the createPersonObject function to include an updateAddress method. This method should accept a new address object and update the person’s address accordingly. Ensure the returned object includes this new method.

*Note:* 
Use `this.` in your code to refer the value of object.

**Example:**
<br>
Input:
<br>
person : Object created by createPersonObject from Problem 1<br>
newAddress : {street: "987 Maple Street", city: "New City"}
<br>
Output:
<br>
*Updated person object with the new address.
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

`createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"},{street: "987 ZXX Street", city: "New City"}).introduce()` should return `"Hi, I'm Bablu, 32 years old, living at 987 ZXX Street, New City"`

```js
assert.deepEqual(createPersonObject("Bablu",32,{street: "23 Abc Street", city : "XYZ"},{street: "987 ZXX Street", city: "New City"}).introduce(),"Hi, I'm Bablu, 32 years old, living at 987 ZXX Street, New City")
```

`createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"},{street: "987 Maple Street", city: "New City"}).introduce()` should return `"Hi, I'm Chutki, 12 years old, living at 987 Maple Street, New City"`

```js
assert.deepEqual(createPersonObject("Chutki",12,{street: "45 Abc Street", city: "XYZ"},{street: "987 Maple Street", city: "New City"}).introduce(),"Hi, I'm Chutki, 12 years old, living at 987 Maple Street, New City")
```

`createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"},{street: "91 Asd Lane", city: "New City"}).introduce()` should return `"Hi, I'm Nobita, 20 years old, living at 98 Road, New City"`

```js
assert.deepEqual(createPersonObject("Nobita",20,{street: "44 ghi Street", city: "PQR"},{street: "98 Road", city: "New City"}).introduce(),"Hi, I'm Nobita, 20 years old, living at 98 Road, New City")
```

`createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"},{street: "7 ZYX Street", city: "Old City"}).introduce()` should return `"Hi, I'm Chintu, 10 years old, living at 7 ZYX Street, Old City"`

```js
assert.deepEqual(createPersonObject("Chintu",10,{street: "23 Abc Street", city: "WXYZ"},{street: "7 ZYX Street", city: "Old City"}).introduce(),"Hi, I'm Chintu, 10 years old, living at 7 ZYX Street, Old City")
```

`createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"},{street: "9 Asd Lane", city: "Old City"}).introduce()` should return `"Hi, I'm Minki, 55 years old, living at 9 Asd Lane, Old City"`

```js
assert.deepEqual(createPersonObject("Minki",55,{street: "11 Abc Lane", city: "XYZ"},{street: "9 Asd Lane", city: "Old City"}).introduce(),"Hi, I'm Minki, 55 years old, living at 9 Asd Lane, Old City")
```

# --seed--
## --seed-contents--

```js
function createPersonObject(name,age,address){
	//  Only change code below this line
	return
}
const person = createPersonObject("babli",23,{street:"1234",city:"delhi"},{ street: "987 Maple Street", city: "New City" }); // Change this line
console.log(person.introduce());
```

# --solutions--

```js
function createPersonObject(name, age, oldAddress, newAddress) { // Automatically assign the new address if provided
    const updatedAddress = newAddress || oldAddress; 
        return { 
            name: name, 
            age: age, 
            address: updatedAddress, 
            introduce: function () { 
                return `Hi, I'm ${this.name}, ${this.age} years old, living at ${this.address.street}, ${this.address.city}`; 
                } 
        }; 
    }
const person = createPersonObject("babli",23,{street:"1234",city:"delhi"},{ street: "987 Maple Street", city: "New City" });
console.log(person.introduce());
```
