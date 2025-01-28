---
id: 67467c2df49e0d048b379dff
title: Decide Umbrella Usage
challengeType: 1
dashedName: decide-umbrella-usage
---

# --description--

**Introduction:**
In this challenge, you'll use boolean variables to decide whether to bring an umbrella. The decision is based on whether it's raining or if it's not the weekend.
<br>
**Challenge:**
Determine if you should bring an umbrella based on the boolean variables isRaining and isWeekend. You should bring an umbrella if it is raining or it is not the weekend.

# --instructions--

Click on this <a href = "https://cs50.ai/chat">Link</a>  to Go to CS50 AI 
And use this prompt prompt __________
Prompt: What does it mean to 'identify the number's sign' in this context?

# --hints--

`umbrellaUsage(true,true)` should return `You don't need an umbrella`

```js
assert(umbrellaUsage(true,true)==="You don't need an umbrella")
```

`umbrellaUsage(true,false)` should return `You should bring an umbrella`

```js
assert(umbrellaUsage(true,false)==="You should bring an umbrella")
```

`umbrellaUsage(false,true)` should return `You don't need an umbrella`

```js
assert(umbrellaUsage(false,true)==="You don't need an umbrella")
```

`umbrellaUsage(false,false)` should return `You don't need an umbrella`

```js
assert(umbrellaUsage(false,false)==="You don't need an umbrella")
```

# --seed--
## --seed-contents--

```js
function umbrellaUsage(isRaining,isWeekend) {
	//  Only change code below this line
	return
}
```

# --solutions--

```js
function umbrellaUsage(isRaining,isWeekend) {
  let ans;
  if (isRaining===true){
    if (isWeekend!==true){
    ans = "You should bring an umbrella";
    }else{
    ans = "You don't need an umbrella";
    }
  }else{
    ans = "You don't need an umbrella";
  }
	return ans;
}
umbrellaUsage(isRaining,isWeekend)
```
