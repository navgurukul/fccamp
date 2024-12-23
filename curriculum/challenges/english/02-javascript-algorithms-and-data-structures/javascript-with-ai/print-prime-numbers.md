---
id: 675431b0013bfb76145d8bd5
title: Print Prime Numbers
challengeType: 1
dashedName: print-prime-numbers
---

# --description--

**Introduction:**
Prime numbers are fundamental in mathematics and programming, characterized by being divisible only by 1 and themselves. Identifying and printing prime numbers in a given range is a common task that helps in understanding algorithms and number theory.
<br>
**Challenge:**
Write a program that takes a number N and prints all prime numbers from 1 to N. This will help you practice detecting prime numbers and handling ranges effectively.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

**Example:**

const N = 18;
<br>
Output: 
<br>
2 3 5 7 11 13 17

**Explanation:**
<br>
Prints prime numbers between 1 and 18
<br>

*Note:* 
Use `primes[primes.length]=value` to push elements at the end of array.

# --hints--

You should use `primes[primes.length]`  in your code to push elements at the end of array.

```js
assert(code.match(/primes[primes.length]/g));
```

`printPrimes(25)` should return `[2, 3, 5, 7, 11, 13, 17, 19, 23]`

```js
assert.deepEqual(printPrimes(25), [2, 3, 5, 7, 11, 13, 17, 19, 23])
```

`printPrimes(2)` should return `[2]`

```js
assert.deepEqual(printPrimes(2), [2])
```

`printPrimes(19)` should return `[2, 3, 5, 7, 11, 13, 17, 19]`

```js
assert.deepEqual(printPrimes(19), [2, 3, 5, 7, 11, 13, 17, 19])
```

`printPrimes(9)` should return `[2, 3, 5, 7]`

```js
assert.deepEqual(printPrimes(9), [2, 3, 5, 7])
```

`printPrimes(1)` should return `[]`

```js
assert.deepEqual(printPrimes(1), [])
```

# --seed--
## --seed-contents--

```js
function printPrimes(N) {
    const primes = [];
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function printPrimes(N) {
    const primes = [];
    for (let i = 2; i <= N; i++) {
    let isPrime = true;
    for (let j = 2; j < i; j++) {
        if (i % j === 0) {
        isPrime = false;
        break;
        }
    }
    if (isPrime===true) {
        primes[primes.length] = i;
        }
    }
    return primes;
}
printPrimes(num)
```
