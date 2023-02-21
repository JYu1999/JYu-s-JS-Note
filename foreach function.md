# Syntax
```js

// Arrow function
forEach((element) => { /* … */ })
forEach((element, index) => { /* … */ })
forEach((element, index, array) => { /* … */ })

// Callback function
forEach(callbackFn)
forEach(callbackFn, thisArg)

// Inline callback function
forEach(function (element) { /* … */ })
forEach(function (element, index) { /* … */ })
forEach(function (element, index, array) { /* … */ })
forEach(function (element, index, array) { /* … */ }, thisArg)
```

## Parameters
- `callback`: A function to execute for each element in the array. Its return value is discarded. The function is called with the following arguments:
    - `elements`: The current element being processed in the array.
    - `index`: The index of the current element being processed in the array.
    - `array` : The array `forEach()` was called upon.
    - `thisArg`: A value to use as `this` when executing `callbackFn`. See [iterative methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#iterative_methods).

以下兩個寫法相同，但近代比較常用foreach (why?)
```js
let num=[1,20,3,600,3242,6,134];

num.forEach(function checkNum(n){
    if(n>100){
        console.log(n);
    }
})

for(let i = 0;i<num.length;i++){
    if(num[i]>100){
        console.log(num[i]);
    }
}
```
- Advantage(by JYu):
    1. 不用管陣列的大小
    2. 直接寫 callback function
        ```js
let num=[1,20,3,600,3242,6,134];

num.forEach(checkNum);

function checkNum(n){
    if(n>100){
        console.log(n);
    }
}

       ```
    3. 透過 parameter，所以幾乎可以取代 for
    4. function 可以不用命名(anonymous function)
       　```js
let num=[1,20,3,600,3242,6,134];

num.forEach(function(n){
    if(n>100){
        console.log(n);
    }
});
```
  