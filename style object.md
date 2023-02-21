- a property of element object
- an object that is controlling the CSS styling of an HTML element
- hyphen in JS is not allowd, therefore, CSS properties in JS are changed to camelCase.
    - CSS: `background-color: blue`
    - JS: `backgroundColor: blue`

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

console.log(button.style);
```

```js
let button = document.querySelector("button");

// button.style.backgroundColor = "black";

// button.style.color = "white";

button.style = "background-color: black; color: white;";
```

> Inline styling > id > class > ...

如果不要任何設定：
```js
let button = document.querySelector("button");

button.style = "background-color: black; color: white;";

button.style = "";
```