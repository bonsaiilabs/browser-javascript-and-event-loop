### Synchronous JavaScript Execution
```js
console.log('wash clothes!')
console.log('clean dishes!')
console.log('clean home!')
```

### Synchronous JavaScript Execution without delay
```js
function washClothes() {
    console.log('washing clothes - DONE')
}

function cleanDishes() {
    console.log('cleaning dishes - DONE')
}

function cleanHome() {
    console.log('home cleaning - DONE')
}

washClothes()
cleanDishes()
cleanHome()
```