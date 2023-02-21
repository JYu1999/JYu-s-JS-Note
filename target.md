回傳 event  的目標是什麼
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
   <h1>This is my H1</h1> 
</body>
<script src="./app.js"></script>
</html>
```

```js
let h1 = document.querySelector("h1");

h1.addEventListener("click", e=>{
    console.log(e.target.innterText);
});
```