### Eventual Results
```js
let add = (a, b) => {
    let sum = a + b;
    console.log("The calculated sum is ", sum)
    return sum
}

add(2, 3)
setTimeout(() => add(3, 3), 5000)
```

### Create and return a resolved Promise
```js
let p = new Promise((resolve, reject) => {
	// Perform async computation
	resolve("Here is resulting data")
})
```

### Create and return a rejected Promise
```js
let p = new Promise((resolve, reject) => {
	// Perform async computation
	reject('The operation failed due to timeout')
}
```

### Creating promise using `Promise.resolve`
```js
let p = Promise.resolve('Creates a new Promise with resulting value')
p.then(data => {
	console.log(data)
})
```

### Creating promise using `Promise.reject`
```js
let p = Promise.reject('Creates new Promise containing error')
p.catch(err => {
	console.log(err)
})
```