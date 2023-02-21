- Works perfectly fine just like function declaration
- doesn't create this keyword.(this keyword refers to window object)
    - 
```js
     
let JYu = {
    name: "JYu Chan",
    sayHi(){
        console.log("Hi, my name is "+this.name+".");
    },
    walk: ()=>{
        console.log(this.name+" is walking on the street.");
    }
}

JYu.sayHi();
JYu.walk(); 
``` 
      

![[Function Hoisting]]

It is okay to do things like the following:
```js
sayHi();

function sayHi(){
    console.log("Hi");
}
```
but you will get error if you code the following:
```js
sayHi();

let sayHi=()=>{
    console.log("Hi");
};

```