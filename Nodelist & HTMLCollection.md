# HTML Collection
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
    <h1 id="first">My First H1.</h1>
    <h1 class="second">My Second H1</h1>
    <p class="second">This is a paragraph.</p>
    <p class="second">This is another paragraph.</p>
</body>
<script src="./app.js"></script>
</html>
```

```js
let test = document.getElementsByClassName("second");
console.log(test);
```
    可以用 index，但跟 array 不一樣，沒辦法用 push, pop, shift, unshift

# Nodelist
```js
let test = document.querySelectorAll(".second");
console.log(test);
```

---

- Both of them have Length property
- Both of them have indices(indexs)
- ==Array and NodeList can use forEach method, but HTML Collection cannot.==
- 