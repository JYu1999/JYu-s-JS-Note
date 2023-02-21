Also called [[closure]]
# [[Scope]]
- In function execution context, if they find a variable that was not declared inside the function, Javascript will go to the global variables and find.
- Global means
	1. where the memory was allocated to the function
	2. a lower level function of the callstack where the memory was allocated to, and keep searching down.
	   ```js
let myName = "JYu";

function sayHI(){
let myName = "Apple";
console.log(myName + "says hi.");
  
function sayHI2(){
    console.log(myName+"says hi.");
}
    sayHI2();
}
sayHI();
	   ```
    - Global Execution Context
        - Creation Phase
    	- myname, function declaration 放進 memory
	- Execution Phase
		- myname = JYU
		- function 先不管，因為已經放進memory
		- 執行sayHI()
		- Function Execution Context
			- Creation Phaes
				- 把 sayHI2() 放進 memory
			- Execution Phase
				- myname = apple
				- apple says hi
				- sayHI2()
				- Function Execution Context
				- Creation Phase -> none
				- Execution Phase
				- console.log
```js
let myName = "JYu";
function sayHI(){
	let myName = "Apple";
	console.log(myName + "says hi.");


	sayHI2();
}
function sayHI2(){
  console.log(myName+"says hi.");
}

sayHI();
```
- 執行 sayHI2() 的時候，myName沒有被定義。會去 function 被定義的地方找。
```js
let myName = "JYu";
function sayHI(){
	let myName = "Apple";
	console.log(myName + "says hi.");
	
  function sayHI2(){
  	console.log(myName+"says hi.");
	}

	function sayHI3(){
      let myName = "banana";
      sayHI2();
    }
}


sayHI();

```

```js
let myName = "JYu";
function sayHI(){
	console.log(myName + "says hi.");
	
  function sayHI2(){
  	console.log(myName+"says hi.");
	}

	function sayHI3(){
      let myName = "banana";
      sayHI2();
    }
}


sayHI();
```


    - [[Global Execution Context]]
		- Creation Phase
			- myname, function declaration 放進 memory
		- Execution Phase
			- myname = JYU
			- function 先不管，因為已經放進memory
			- 執行sayHI()
		- Function Execution Context
			- Creation Phaes
				- 把 sayHI2() 放進 memory
			- Execution Phase
				- myname = apple
				- apple says hi
				- sayHI2()
		- Function Execution Context
			- Creation Phase -> none
			- Execution Phase
				- console.log
- ```Javascript
  let myName = "JYu";
  function sayHI(){
  	let myName = "Apple";
  	console.log(myName + "says hi.");
  
  
  	sayHI2();
  }
  function sayHI2(){
    console.log(myName+"says hi.");
  }
  
  sayHI();
  ```
	- 執行 sayHI2() 的時候，myName沒有被定義。會去 function 被定義的地方找。
- ```Javascript
  let myName = "JYu";
  function sayHI(){
  	let myName = "Apple";
  	console.log(myName + "says hi.");
  	
    function sayHI2(){
    	console.log(myName+"says hi.");
  	}
  
  	function sayHI3(){
        let myName = "banana";
        sayHI2();
      }
  }
  
  
  sayHI();
  ```
- ```Javascript
  let myName = "JYu";
  function sayHI(){
  	console.log(myName + "says hi.");
  	
    function sayHI2(){
    	console.log(myName+"says hi.");
  	}
  
  	function sayHI3(){
        let myName = "banana";
        sayHI2();
      }
  }
  
  
  sayHI();
  ```
-