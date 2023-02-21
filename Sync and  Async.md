# Sync code
```js
function sayHello(){
    console.log("hello");
    console.log("How are you?");
}

console.log("start");

sayHello();

console.log("end");
```

# Async
JS是single-thread Programming langruage，沒有能力處理Async。網頁瀏覽器會提供 web API，JS會請瀏覽器幫我們處理。等瀏覽器處理完再傳回來。
```js
console.log("start");

setTimeout(()=>{
    console.log("Here is the code.");
}, 2000);

console.log("end");

```
- addEventListener() 也是 async
# [[Callback function]]
![[Callback function#^6533fb]]
```js
setTimeout(myFunction, 3000);

function myFunction() {
 console.log("Hello");
}
```
## Callback Hell
以前跟資料庫做連接的時候會遇到的問題
猜猜看會出現什麼？
```js
function getData(name){
  setTimeout(()=>{
      return {name: name, age:Math.floor(Math.random() * 20), major:"CS"};
  }, 2000);
}

console.log("start");

let data = getData("JYu");

console.log(data);

console.log("end");

```
要處理這個狀況，就可以用callback function
```js
function getData(name, callback){
  setTimeout(()=>{
    callback({name: name, age:Math.floor(Math.random() * 20), major:"CS"});
  }, 2000);
}

console.log("start");

data = getData("JYu", (obj)=>{
  console.log(obj);
});


console.log("end");
```

![[Screen Shot 2023-01-18 at 4.27.07 PM.png]]
假設又有一個 getMovieDetail需要繼續串下去...-> callback hell

# [[Promise]]


# [[async and await]]

mongoDB -> mongoose