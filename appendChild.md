對於 parent element 附加小孩
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    
    
</body>
<script src="./app.js"></script>
</html>
```

```js
let body =document.querySelector("body");

let myh1 = document.createElement("h1");

myh1.innerText = "Hello, world";

body.appendChild(myh1);
```