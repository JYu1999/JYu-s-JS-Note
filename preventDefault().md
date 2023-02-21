防止某些預設的事情發生

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
    <form>
        <input type="text"/>
        <button type="submit">Submit the form.</button>
    </form>
</body>
<script src="./app.js"></script>
</html>
```

```js
let button = document.querySelector("button");

button.addEventListener("click", e=>{
    e.preventDefault();
})
```
