Document Object Model

# Why?
It allows us to manipulate HTML elements. (If JS doesn;t have DOM, then it has no difference compared to other programming language.)

# Window Object
A global variable, window, representing the window in which the script is running, is exposed to JS code.
```js
console.log(window);
```
## Some common Methods
- alert()
    ```js
    window.alert("Hi");
    //window可省略
    ```
- prompt()
    ```js
    window.prompt("Hi");
    ```
- setInterval()
    - 每個多久執行一次
    ```js
    function hello(){
        console.log("Hi");
    }
    setInterval(hello, 1500);
    ```
- clearInterval()
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="./app.js"></script>
    <title>Document</title>
</head>
<body>
   <button onclick="stop()">Stop</button> 
</body>
</html>
```

```js
function hello(){
  console.log("Hi");
}
let myInterval = setInterval(hello, 1500);

function stop(){
  clearInterval(myInterval);
}
```
- addEventListener()
    to be continued...
## Some common Properties
[[JS OOP]]
> [!note]
> 以下四個都是 object
> 但不代表 window object 所有的 properties  都是 object
- Console
    - has properties but rarely use
    - method:
        - log()
        - error()
          ```js
          console.error("This is error.");
          ```
        - warn()
- [[Document]]
- [[LocalStorage and SessionStorage]]
