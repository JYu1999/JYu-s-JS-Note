- Storage is a place to store data in browser. (This is not database.)
- key value pair. (Both have to be string. If the value is not string then it would be cast to string)
    - ==key==不能重複！ -> PK

# some methods
- setItem(key, value)
```js
localStorage.setItem("name", "Wilsen Ren");

console.log(localStorage);
```
這種方法可以看到存了什麼，但是不好看
直接在 inspect -> Application -> session storage 看
- getItem(key)
```js
localStorage.setItem("Gee", "long");

let myAddr = localStorage.getItem("Gee");
console.log(myAddr);
```
- removeItem(key)
- clear()

# Diff between local nad session
Session storage is destroyed once the user closes the browser, whereas, Local Storage stores data with no expiration date.（除非用 localStorage.clear() or removeItem())

# String storage
- storage can only store string
- key value pair. (Both have to be string. If the value is not string then it would be cast to string) -> 就算是很奇怪的 data type  也一樣(array)
```js
localStorage.setItem("Gee",25);

let myAddr = localStorage.getItem("Gee");
console.log(typeof myAddr);
```
## Storage with other data types
- JSON means Javascript Object Notation
- JSON.stringify()
- JSON.parse()
```js
//localStorage.clear();

//let friends = ["Josh", "Mike", "Doug"];

//localStorage.setItem("friends", JSON.stringify(friends));

let myFriends = JSON.parse(localStorage.getItem("friends"));

console.log(myFriends);
```

## Why do we put script tag at the bottom
- It takes long time to render JS code. (We want to show something to the user first)
- Browser has to read all HTML and CSS before using DOM -> 不然會讀不到