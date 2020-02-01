### Asynchronous JavaScript Execution with `setTimeout()`
```js
function washClothes() {
    console.log('washing clothes')
    setTimeout(() => console.log('washing clothes - DONE'), 3000)
}

function cleanDishes() {
    console.log('cleaning dishes')
    setTimeout(() => console.log('cleaning dishes - DONE'), 4000)
}

function cleanHome() {
    console.log('home cleaning')
    setTimeout(() => console.log('home cleaning - DONE'), 5000)
}

washClothes()
cleanDishes()
cleanHome()
```