在 HTML 中用 CSS Selector 作 query
querySelector() only return the first html element which match the css selector
```html
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

let test = document.querySelector("h1.second");
console.log(test);


let test1 = document.querySelector(".second");
console.log(test1);

let test2 = document.querySelectorAll(".second");
console.log(test2);
```
> [!note]
> nodeList 可以加 index，但它不是array!

[[querySelector()]] 和 querySelectorAll()，所有 HTML element object 也可以用
只會找到 childElement

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
    <section>
        <p class="blue">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam modi ad nam fugit mollitia consequatur sapiente at a, sunt quos!
        </p>
        <p class="blue">adfd</p>
    </section>
    <p class="blue">lorem aasd</p>
</body>
<script src="./app.js"></script>
</html>
```

```js
let section = document.querySelector("section");

let blueP = section.querySelectorAll("p.blue");

console.log(blueP);
```
