
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
    
    <h1 class="myH1"></h1>
    
</body>
<script src="./app.js"></script>
</html>
```

網頁可以針對使用者顯示不同的頁面
```js
let h1 = document.querySelector("h1.myH1");

h1.innerHTML = "Hello";
//h1.innerText = "Hello";
//h1.innerHTML = "<mark>Hi, I am JYu</mark>";
```