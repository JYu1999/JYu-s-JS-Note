一個 tag 可以有好多 class ，classList 會把全部的 class 回傳
先用以下範例看一下會回傳什麼：
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
    <p class="red bold">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis, fuga ipsa maxime quas sit accusantium earum voluptatem atque vero natus.
    </p>
</body>
<script src="./app.js"></script>
</html>
```


```js
let myP = document.querySelector("p");

console.log(myP.classList);
//console.log(typeof myP.classList);
```

## add()
接著我們把 p tag 裡面的 class 移除
```HTML
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
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis, fuga ipsa maxime quas sit accusantium earum voluptatem atque vero natus.
    </p>
</body>
<script src="./app.js"></script>
</html>
```
加一個 css  方面看效果
```css
.red{
    background-color: red;
}

.blue{
    background-color: blue;
}

.bold{
    font-weight: bolder;
}
```

```js
let myP = document.querySelector("p");

myP.classList.add("red");
myP.classList.add("bold");
```
## remove
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
    <p class="red">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis, fuga ipsa maxime quas sit accusantium earum voluptatem atque vero natus.
    </p>
</body>
<script src="./app.js"></script>
</html>
```

```js
let myP = document.querySelector("p");

myP.classList.remove("red");
```

## toggle
```js
let myP = document.querySelector("p");

myP.classList.toggle("red");
```
## contains
return whether an element contains a certain class
```js
let myP = document.querySelector("p");

console.log(myP.classList.contains("blue"));
```