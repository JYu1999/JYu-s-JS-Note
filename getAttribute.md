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
    <a href="youtube.com" title="youtube">Go to youtube</a>
</body>
<script src="./app.js"></script>
</html>
```

```js
let a = document.querySelector("a");

console.log(a.getAttribute("href"));
console.log(a.getAttribute("title"));
```