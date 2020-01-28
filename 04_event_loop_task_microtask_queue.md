### Event Loop's Task Queue and Micro Task Queue
```js
console.log("Hello script")
setTimeout(() => console.log("Work done!"), 5000)

fetch('https://api.myjson.com/bins/c8j82')
.then((response) => response.json())
.then(jsonData => console.log(jsonData))
.then(() => console.log('Data fetched.. exiting now!'))

console.log("Bye! Script")
```