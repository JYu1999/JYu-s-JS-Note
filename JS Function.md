# Global Execution Context
---
## Creation Phase
- [[Window Object]] gets instantiated
- [[Scope Chain]] gets created, follow the principle of [[closure]]
- this keyword gets generate (points to the window object)
- memories get allocated to all the ==functions declaration variable and var variables==, except for the **let and const and function expression**. ([[Function Hoisting]])

---
## Execution Phase
- Run the code line by line followed the principle of [[callstack]]

---
# Function Execution Context
## Creation Phase
- [[Scope Chain]] gets created, follow the principle of [[closure]]
- this keyword gets generate, if the function is not an [[arrow function]]
- [[Function Hoisting]]
---
## Execution Phase
Run the code line by line followed the principle of [[callstack]]

---
# Constructor Function
- 用於製作大量相似的objects
- Starts With Uppercase Letter
- Used with "new" keyword
```js
function Car(brand, year, capacity){
  this.brand = brand,
    this.year = year,
    this.capacity = capacity,
    this.move = function(){
    	console.log("Moving...");
  }
}

let car1 = new Car("Toyota", 1999, 5);

let car2 = new Car("Tesla", 2021, 7);

car1.move();
```
---
# Prototype
- How about there are 100 cars?
```Javascript
	  console.log(car1.move === car2.move);
```
- They can use function together.
- ==Prototype is a simple reference to another object; this object contains common properties and methods across all instances.== ->  所有的物件都有 reference到 prototype
## Prototype Inheritance
```js
function Car(brand, year, capacity){
	    this.brand = brand,
	      this.year = year,
	      this.capacity = capacity
}
	  
Car.prototype.move = function(){
    console.log("Moving...");
}
	  
let car1 = new Car("Toyota", 1999, 5);
	  
let car2 = new Car("Tesla", 2021, 7);
	  
//Prototype Inheritance
car1.move();
	  
console.log(car1.move === car2.move);
```
```js
let num = [15,22,9];
	  
	  num.push(15);
	  console.log(num);
```
### [[Coercion]]
``let myName = "JYu`` vs ``let myName = new String("JYu")``

# 3 Important Functions(Methods)
## bind(): 綁定
```js
let JYu={
  name: "JYu Chan",
  age: 23
}
function getAge(){
  console.log(this);
  console.log(this.age);
}
```
在上面這個例子中，this是undefine。
下面這個例子中，我們綁定 getAge 這個 function 的 this 是 JYu
```js
let JYu={
  name: "JYu Chan",
  age: 23
}
function getAge(){
  console.log(this);
  console.log(this.age);
}

let getJYuAge = getAge.bind(JYu);
getJYuAge();
```
---
## call(): 執行
直接執行，但this 變成call他的
```js
let JYu={
  name: "JYu Chan",
  age: 23
}
function getAge(){
  //console.log(this);
  console.log(this.age);
}

getAge.call(JYu);
```

```js
let JYu={
  name: "JYu Chan",
  age: 23
}
function getAge(country, height){
  //console.log(this);
  console.log(this.age);
  console.log("I am from "+country+". I am "+height+" cm.");
}

getAge.call(JYu, "Taiwan", 174);
```
---
## apply()
```js
let JYu={
  name : "JYu Chan",
  age : 23
}
function getAge(country, height){
  //console.log(this);
  console.log(this.age);
  console.log("I am from "+country+". I am "+height+" cm.");
}

getAge.apply(JYu, ["Taiwan", 174]);
```
