- Document is an Object. (Also a property of window object)
- Document means the HTML document.
- This **model** means all HTML elements are objects. (It means that they all have its properties and methods.) -> 每個 HTML tag 都是 object
![[Pasted image 20230208135102.png | 400]]
![[Pasted image 20230208135151.png|500]]
```js
console.log(document);
```
[JavaScript HTML DOM Document](https://www.w3schools.com/js/js_htmldom_document.asp)

- Different HTML element might have its own methods and properties.
- All HTML elements must have properties and methods from the following list:

## methods
>[!note]
>重要性由上往下遞減
- [[querySelector()]]
- [[querySelectorAll()]]
- [[addEventListener()]] -> 之後再說
- [[getElementById()]]
- [[getElemenstByClassName()]]
- [[createElement()]]
- [[appendChild]]
- [[getAttribute]]
- [[remove()]]
## properties
- [[children]] -> return HTML Collection，但還是比較常用
- [[childNode]] -> return NodeList
- [[parentElement]]
- [[innerHTML & innerText]]
- [[classList]]
- [[style object]]

# [[arrow function]]

# [[foreach function]]

# [[Nodelist & HTMLCollection]]

# Inheritance in DOM
- All HTML elements inherit properties and methods from "element object"
- But some of them have its own methods

[W3school: JavaScript and HTML DOM Reference](https://www.w3schools.com/jsref/default.asp) > HTML Element Objects Reference > Video

# [[JS Events]]