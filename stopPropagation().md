停止擴散
```html
　<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
   <div class="a">
    <div class="b"></div>
   </div> 
</body>
<script src="./app.js"></script>
</html>
```

```css
.a {
    width: 300px;
    height: 300px;
    background-color: blue;
}

.b {
    width: 500px;
    height: 500px;
    background-color: red;
}
```

```js
let a = document.querySelector("div.a");
let b = document.querySelector("div.b");

a.addEventListener("click", ()=>{
    alert("AAAAA");
});

b.addEventListener("click",(e)=>{
    e.stopPropagation();
    alert("BBBB");
});
```
