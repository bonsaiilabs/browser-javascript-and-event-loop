### Synchronous JavaScript Execution with Delay - Blocking
```js
function washClothes(start) {
    console.log('washing clothes')
    while (new Date().getTime() < start + 3000) ;
    console.log('washing clothes - DONE')
}

function cleanDishes(start) {
    console.log('cleaning dishes')
    while (new Date().getTime() < start + 4000) ;
    console.log('cleaning dishes - DONE')
}

function cleanHome(start) {
    console.log('cleaning home')  	
    while (new Date().getTime() < start + 5000) ;
    console.log('home cleaning - DONE')
}

washClothes(new Date().getTime())
cleanDishes(new Date().getTime())
cleanHome(new Date().getTime())
```