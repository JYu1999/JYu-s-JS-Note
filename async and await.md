> [!note]
> _async and await make promises easier to write_
> **async** makes a function return a Promise
> **await** makes a function wait for a Promise
# Syntax
## Async
The keyword `async` before a function makes the function return a promise:
以下兩個寫法相同
```js
async function myFunction() {  
  return "Hello";  
}

function myFunction() {  
  return Promise.resolve("Hello");  
}
```
### Example
```js
async function myFunction() {  
  return "Hello";  
}  
myFunction().then(  
  function(value) {myDisplayer(value);}  
);
```

## Await
The `await` keyword can only be used inside an `async` function.

The `await` keyword makes the function pause the execution and wait for a resolved promise before it continues:

```js
let value = await promise;
```

[W3school: More Example](https://www.w3schools.com/js/js_async.asp)

# Example
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
 
async function showMovie(){
    const obj = await getData("JYu");
    const movie = await getMovies(obj.age);
    console.log(movie.text);
}

showMovie();
```

把可能出錯的程式碼放到 try 裡面
```js
async function showMovie(){
    try{
        const obj = await getData("JYu");
        const movie = await getMovies(obj.age);
        console.log(movie.text);
    } catch(e){
        console.log(e);
    }
   
}
```