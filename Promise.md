# Promise Object Properties
The Promise object supports two properties: **state** and **result**.

While a Promise object is "pending" (working), the result is undefined.

When a Promise object is "fulfilled", the result is a value.

When a Promise object is "rejected", the result is an error object.

| myPromise.state | myPromise.result | 
| :--: | :--: |
| "pending" | undefined |
| "fulfilled" | a result value |
| "rejected" | an error object |
> [!note]
> You cannot access the Promise properties **state** and **result**.
> You must use a Promise method to handle promises.

Promise.then() takes two arguments, a callback for success and another for failure.

Both are optional, so you can add a callback for success or failure only.
```js
function myDisplayer(some) {  
  console.log(some);
}  
  
let myPromise = new Promise(function(myResolve, myReject) {  
  let x = 0;  
  
// The producing code (this may take some time)  
  
  if (x == 0) {  
    myResolve("OK");  
  } else {  
    myReject("Error");  
  }  
});  
  
myPromise.then(  
  function(value) {myDisplayer(value);},  
  function(error) {myDisplayer(error);}  
);
```
# Example 1
## Callback
```js
setTimeout(function() { myFunction("Hi"); }, 3000);  
  
function myFunction(value) {  
  console.log(value);
}
```
## Promise
```js
let myPromise = new Promise(function(myResolve, myReject) {  
  setTimeout(function() { myResolve("Hi"); }, 3000);  
});  
  
myPromise.then(function(value) {  
  console.log(value);
});
```

# Example 2
## Callback
```js
function getData(name, callback){
    setTimeout(()=>{
        callback({name: name, age: Math.floor(Math.random()*10), major: "CS"});
    }, 2000);
}

function getMovies(age, callback){
    if(age<12){
        setTimeout(()=>{
            callback("cartoon");
        }, 1500);
    }
    else if(age<18){
        setTimeout(()=>{
            callback("Teen");
        },1500);
    }
    else{
        setTimeout(()=>{
            callback("Adult");
        },1500);
    }
}

getData("JYu",(obj)=>{
    console.log(obj);
    getMovies(obj.age, (str)=>{
        console.log(str);
    });
});
```
## Promise
Catch 會抓到哪一個會視先後順序而定
```js
function getData(name){
   if(name == "JYu"){
    return new Promise((resolve, reject)=>{
        setTimeout(()=>{
            resolve({name:"JYu Chan", age: 23})
        },2000);
    });
   } else{
    return new Promise((resolve, reject)=>{
        setTimeout(()=>{
            reject(new Error("Not allowed"));
        }, 2000);
    });
   }
}

function getMovies(age, callback){
    if(age<12){
       return new Promise((resolve, reject)=>{
            setTimeout(()=>{
                resolve({text: "Cartoon"});
            },1500);
       });
    }
    else if(age<18){
        return new Promise((resolve, reject)=>{
            setTimeout(()=>{
                resolve({text: "Teen"});
            },1500);
       });
    }
    else{
        return new Promise((resolve, reject)=>{
            setTimeout(()=>{
                reject(new Error("You are too old."));
            },1500);
       });
    }
}

getData("JYu").then((obj) => {
    console.log(obj);
    return getMovies(obj.age)
}).then(msg=>{
    console.log(msg.text);
}).catch((e)=>{
    console.log(e);
});
```