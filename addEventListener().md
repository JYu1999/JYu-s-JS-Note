window Object 和 element object 都能用 addEventListener

第一個 Parameter 是 event type，例如 resize the screen, scroll, click

第二個 parameter  是 callback function, 代表 event  發生時要執行的事情

```js
window.addEventListener("click", (e)=>{
    console.log(e);
});
```

這裡的 `e` 代表 event object -> javascript enents 都是 object

# Event Object Inheritance
![[JS+Event+Inheritance.png]]

[w3school: HTML DOM Event Objects](https://www.w3schools.com/jsref/obj_events.asp)

[w3school: HTML DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)

# Event Object
## Properties
- [[target]]
## Methods
- [[preventDefault()]]
- [[stopPropagation()]]

